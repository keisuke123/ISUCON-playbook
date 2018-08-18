# 概要
ISUCONするときに便利そうなものをあつめたAnsibleのplaybookです.

# ディレクトリ構成
```
.
├── Vagrantfile
├── group_vars/  # empty
├── host_vars/   # empty
├── hosts        # 対象ホストを記載
├── isucon.yaml  
├── roles/
│   └── ISUCON/
│       ├── defaults/
│       ├── files/
│       ├── handlers/
│       ├── meta/
│       ├── tasks/
│       │   └── main.yaml
│       ├── templates/
│       └── vars/
│           └── main.yaml
└── setup.yaml
```

# 使い方
1. hostsに対象のホストを書きます. 
    ```
    <ip addr> ansible_ssh_user=<sshユーザ> ansible_ssh_private_key_file=<キーの指定>
    ```

1. 実行します
    ```bash
    $ ansible-playbook -i hosts setup.yaml
    ```

# 諸注意
- keisuke123/ISUCON-configにめちゃくちゃ依存してます