Role Name
=========

This role allows an operator of several .onion mirrors to comply with the Dark.Fail Onion Mirrors Guidelines specification (if the specification adopts RFC 8615).

Requirements
------------

None

Role Variables
--------------

The following variables should be changed;
    gpg_key_id: "gpg@example.onion"
    canary_line_one: An automated bot has confirmed this canary
    canary_line_two: An automated bot has control of this PGP key
    mirrors_list: []

These variables don't need to be changed depending on your requirements;
   canary_days: 14
   temp_dir: /tmp
   remote_dir: /var/www/htdocs

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: OnionMirrors
      force_handlers: true
      gather_facts: true
      vars:
	gpg_key_id: support@ablative.hosting
	canary_line_one: "I am the administrator of Ablative.Hosting"
	canary_line_two: "I have control of PGP key 0x000000000000"
	mirrors_list:
	 - https://ablative.hosting
         - https://hzwjmjimhr7bdmfv2doll4upibt5ojjmpo3pbp5ctwcg37n3hyk7qzid.onion
      roles:
         - omg

License
-------

BSD

Author Information
------------------

This role was create by Gareth L of [Ablative Hosting](https://Ablative.hosting). The author has no affiliation with Dark.Fail.
