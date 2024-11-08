# Terraform plans for deployment of Charmed HPC

Terraform for deploying a full Charmed HPC cluster using the Slurm workload manager.

The plans make use of the [Juju Terraform Provider](https://github.com/juju/terraform-provider-juju) to interact with a previously bootstrapped [Juju](https://juju.is) controller. A `justfile` is provided to simplify deployment through the [just](https://github.com/casey/just) command runner and [OpenTofu](https://opentofu.org/) infrastructure as code tool.

## ✨ Getting started

A Juju 3.x controller [bootstrapped](https://juju.is/docs/juju/bootstrapping) on your choice of cloud is required. Steps for deploying:

```shell
# Prerequisites
juju bootstrap <cloud name> <controller name>
sudo snap install --classic opentofu
sudo apt install just

# Deploy with a single command!
just deploy
```

## 🤔 What's next?

To learn more about the deployment and use of a Charmed HPC cluster, the following resources are available:

* [Charmed HPC Documentation](https://canonical-charmed-hpc.readthedocs-hosted.com/en/latest)
* [Open an issue](https://github.com/charmed-hpc/charmed-hpc-terraform/issues/new?title=ISSUE+TITLE&body=*Please+describe+your+issue*)
* [Ask a question on the Charmed HPC GitHub](https://github.com/orgs/charmed-hpc/discussions/categories/q-a)

## 🛠️ Development

A useful command to help while hacking on the plans is:

```shell
just check  # Checks file formatting and syntax are valid.
```

or equivalent [OpenTofu](https://opentofu.org/) commands:

```shell
tofu fmt -check -recursive      # Apply formatting standards to files.
tofu validate                   # Ensure files are syntactically valid.
```

If you're interested in contributing, take a look at our [contributing guidelines](./CONTRIBUTING.md).

## 🤝 Project and community

The Charmed HPC Terraform plans are a project of the [Ubuntu High-Performance Computing community](https://ubuntu.com/community/governance/teams/hpc). Interested in contributing bug fixes, patches, documentation, or feedback? Want to join the Ubuntu HPC community? You’ve come to the right place!

Here’s some links to help you get started with joining the community:

* [Ubuntu Code of Conduct](https://ubuntu.com/community/ethos/code-of-conduct)
* [Contributing guidelines](./CONTRIBUTING.md)
* [Join the conversation on Matrix](https://matrix.to/#/#hpc:ubuntu.com)
* [Get the latest news on Discourse](https://discourse.ubuntu.com/c/hpc/151)
* [Ask and answer questions on GitHub](https://github.com/orgs/charmed-hpc/discussions/categories/q-a)

## 📋 License

The Charmed HPC Terraform plans are free software, distributed under the Apache Software License, version 2.0.
See the [Apache-2.0 LICENSE](./LICENSE) file for further details.
