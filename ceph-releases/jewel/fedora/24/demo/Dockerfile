# DOCKER-VERSION 1.0.0
#
# Ceph Demo AIO
#
# VERSION 0.0.1

FROM ceph/base:tag-build-master-jewel-fedora-24
MAINTAINER Sébastien Han "seb@redhat.com"

# Add bootstrap script and s3cfg
ADD s3cfg /root/.s3cfg
ADD entrypoint.sh /entrypoint.sh

# Add volumes for Ceph config and data
VOLUME ["/etc/ceph","/var/lib/ceph"]

# Expose the Ceph ports
EXPOSE 6789 6800 6801 6802 6803 6804 6805 80 5000

# Execute the entrypoint
ENTRYPOINT ["/entrypoint.sh"]
