## EKS CDK Blueprint Example

[Reference](https://catalog.workshops.aws/eks-blueprints-for-cdk/en-US)

## Prereq

* CDK
  * `npm install -g aws-cdk@2.86.0`
* [Bootstrapping](https://docs.aws.amazon.com/cdk/v2/guide/bootstrapping.html)
  * [Link](https://catalog.workshops.aws/eks-blueprints-for-cdk/en-US/020-setup/self-paced/8-bootstrap-cdk)

## Instructions

Create a CDK Project

```sh
git clone git@github.com:hemanth-avs/eks-cdk-example.git
cd eks-cdk-example

mkdir my-eks-blueprints
cd my-eks-blueprints
cdk init app --language typescript
```

Install Blueprints module

```sh
npm i @aws-quickstart/eks-blueprints@1.10.0
```

Create Platform and Application Team user

```sh
aws iam create-user --user-name platform
aws iam create-user --user-name application
```

