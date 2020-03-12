FROM debian:latest

# To avoid bricked workspaces (https://github.com/gitpod-io/gitpod/issues/1171)
ENV DEBIAN_FRONTEND=noninteractive

ENV LANG=en_US.UTF-8
ENV LC_ALL=C

# FIXME: Get end-user name
ENV myUser="kreypod"

USER root

# Add end-user
RUN useradd \
	--uid 33333 \
	--create-home --home-dir "$HOME/$myUser" \
	--shell /bin/bash \
	--password "$kreypod" \
	"$kreypod" || exit 1

# FIXME: Build dockerfile based on specified packages in .kreypod.yml