# OpenVPN Client

- Setup OpenVPN Client

## Requirements

- Debian GNU/Linux 9

## Role Variables

see defaults/main.yml

## Dependencies

None.

## Example Playbook

    ---
    - hosts: all
      sudo: yes
      roles:
      - role: znz.openvpn-client
        openvpn_client:
        - name: "Example-Net"
          proto: "udp"
          host: "vpn.example.net"
          port: 1194
          cipher: "AES-256-CBC"
          auth: "SHA512"
          tls_cipher: "TLS-DHE-RSA-WITH-AES-256-GCM-SHA384:TLS-DHE-RSA-WITH-AES-128-GCM-SHA256:TLS-DHE-RSA-WITH-AES-256-CBC-SHA:TLS-DHE-RSA-WITH-CAMELLIA-256-CBC-SHA:TLS-DHE-RSA-WITH-AES-128-CBC-SHA:TLS-DHE-RSA-WITH-CAMELLIA-128-CBC-SHA"
          ca_crt: |
            -----BEGIN CERTIFICATE-----
            (Your CA cert)
            -----END CERTIFICATE-----
          ta_key: ""
          client_crt: |
            -----BEGIN CERTIFICATE-----
            (Your client cert)
            -----END CERTIFICATE-----
          client_key: |
            -----BEGIN RSA PRIVATE KEY-----
            (Your client private key)
            -----END RSA PRIVATE KEY-----


## License

MIT License
