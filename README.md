# tunnel-plugin-kubectl
A [Tunnel](https://github.com/khulnasoft/tunnel) plugin that scans the images of a kubernetes resource

## Install

```
$ tunnel plugin install github.com/khulnasoft/tunnel-plugin-kubectl
$ tunnel kubectl -h
Usage: tunnel kubectl [-h,--help] TYPE NAME [TUNNEL OPTION]
 A Tunnel plugin that scans the images of a kubernetes resource.

Options:
  -h, --help    Show usage.

Examples:
  # Scan a Pod
  tunnel kubectl pod mypod

  # Scan a Deployment
  tunnel kubectl deployment mydeployment -n mynamespace

  # Scan a Job and filter by severity
  tunnel kubectl job myjob -n mynamespace -- --severity CRITICAL
```

## Usage
Tunnel's options need to be passed after `--`.

```
# Scan a Pod
$ tunnel kubectl pod mypod

# Scan a Deployment
$ tunnel kubectl deployment mydeployment -n mynamespace

# Scan a Job and filter by severity
$ tunnel kubectl job myjob -n mynamespace -- --severity CRITICAL
```
