Role Name
=========

An Ansible role to generate and test the Torbutton extension against a given Tor Browser Bundle.

Requirements
------------

This role has been tested with Ansible version 2.2.1.0

Role Variables
--------------

	dirpath: "~/"
	repo_name: "torbutton"

	git_repo: "https://git.torproject.org/{{ repo_name }}.git"
	git_tag: "master"

	patch: "" # Path to the patch
	patched_version: "" # Version of the patched Torbutton, to locate the generated XPI
	tor_browser_bundle_path: "" # Path to the Tor Browser Bundle, to move the patched XPI to it

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: parmegv.ansible-torbutton, patch: "~/torbutton_patch", patched_version: "1.9.6.1", tor_browser_bundle_patch: "~/tor-browser_en-US" }

License
-------

BSD

Author Information
------------------

Rafael Gálvez Vizcaíno
Ph.D. student at ESAT/COSIC KU Leuven
