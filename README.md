Sample implementation of a role that has extra controller-side code

To test, run:

```
  ansible-playbook 28770.yml
```

To generate the local_helpers-1.0.tar.gz file, do something like:

```
  cd local_helpers
  python2 setup.py sdist
  mv dist/local_helpers-1.0.tar.gz roles/new_role/files/local_helpers-1.0.tar.gz
```

This sample keeps all code in the same repository, does not require modifying
PYTHONPATH, and should let a user simply git checkout the role and start using
it in their playbook.
