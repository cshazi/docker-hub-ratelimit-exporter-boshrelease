# BOSH release for docker-hub-ratelimit-exporter

This BOSH release and deployment manifest deploy a cluster of docker-hub-ratelimit-exporter.

## Usage

This repository includes base manifests and operator files. They can be used for initial deployments and subsequently used for updating your deployments:

```plain
export BOSH_ENVIRONMENT=<bosh-alias>
export BOSH_DEPLOYMENT=docker-hub-ratelimit-exporter
git clone https://github.com/cloudfoundry-community/docker-hub-ratelimit-exporter-boshrelease.git
bosh deploy docker-hub-ratelimit-exporter-boshrelease/manifests/docker-hub-ratelimit-exporter.yml
```

If your BOSH does not have Credhub/Config Server, then remember `--vars-store` to allow generation of passwords and certificates.

### Update

When new versions of `docker-hub-ratelimit-exporter-boshrelease` are released the `manifests/docker-hub-ratelimit-exporter.yml` file will be updated. This means you can easily `git pull` and `bosh deploy` to upgrade.

```plain
export BOSH_ENVIRONMENT=<bosh-alias>
export BOSH_DEPLOYMENT=docker-hub-ratelimit-exporter
cd docker-hub-ratelimit-exporter-boshrelease
git pull
cd -
bosh deploy docker-hub-ratelimit-exporter-boshrelease/manifests/docker-hub-ratelimit-exporter.yml
```
