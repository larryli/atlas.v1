Update Ubuntu Atlas Box
=========================

update https://cloud-images.ubuntu.com/vagrant/ to https://atlas.hashicorp.com/larryli

Get:

	go get -ldflags "-s -w" github.com/larryli/atlas.v1/update-ubuntu-vagrant-box

Test:

	update-ubuntu-vagrant-box --username="yourname" --test

Update:

	update-ubuntu-vagrant-box --username="yourname" --token="--replace-your-access-token--"


