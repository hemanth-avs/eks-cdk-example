## EKS CDK Blueprint Example

* [Reference](https://catalog.workshops.aws/eks-blueprints-for-cdk/en-US)
* [CDK EKS Blueprints](https://aws-quickstart.github.io/cdk-eks-blueprints/)
* []

## Prereq

* CDK
  * `npm install -g aws-cdk@2.86.0`
* [Bootstrapping](https://docs.aws.amazon.com/cdk/v2/guide/bootstrapping.html)
  * [Link](https://catalog.workshops.aws/eks-blueprints-for-cdk/en-US/020-setup/self-paced/8-bootstrap-cdk)
* [Team Teams](https://aws-quickstart.github.io/cdk-eks-blueprints/teams/teams/)

## Instructions

Create a CDK Project

```sh
git clone git@github.com:hemanth-avs/eks-cdk-example.git
cd eks-cdk-example

mkdir my-eks-blueprints
cd my-eks-blueprints
cdk init app --language typescript

cp ../code/my-eks-blueprints-stack.ts lib/
cp ../code/my-eks-blueprints.ts bin/
cp -r ../code/teamscode/teams .
```

Create Platform and Application Team user

```sh
aws iam create-user --user-name platform
aws iam create-user --user-name application
```

Install Blueprints module

```sh
npm i @aws-quickstart/eks-blueprints@1.10.0
```

Create Cloud formation template

Translate / create the AWS CloudFormation template from defined resources

```sh
cdk synth cluster-stack
```

Review Cloud Formation Template

```sh
ls -lrta cdk.out/*template*
```

Deploy the Stack

```sh
cdk deploy cluster-stack
```
