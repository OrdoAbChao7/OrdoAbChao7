# deploy-clash-node

��ȫ�� Ubuntu 24.04 x64 �������ϣ�һ������� **VLESS + Reality** �ڵ㣬������������ Clash Verge Rev / Mihomo �� HTTPS �������ӡ�

## һ������

���������й��� IPv4����ƽ̨����ǽ����� TCP `80`��`443`��`8443`������ `sudo` Ȩ�޵��û���¼�����������У�

```bash
curl -fsSLo deploy-clash-node.sh https://raw.githubusercontent.com/OrdoAbChao7/OrdoAbChao7/105892a6e14f9f5457401f43f42babcac870eb0e/skills/deploy-clash-node/scripts/deploy.sh && sudo bash deploy-clash-node.sh
```

�ű����Զ����ɶ����� UUID��Reality ��Կ�Ͷ������·������ɺ󽫴�ӡ���� URL���� URL ճ���� Clash Verge Rev �ġ����ġ�ҳ�浼�롣URL Ҳ�����ڷ������� `/root/clash-node/access.txt`��

�繫������ IP ���������� IP ��ͬ����ָ����� IP��

```bash
sudo NODE_IP=203.0.113.10 bash deploy-clash-node.sh
```

`REALITY_SNI` Ĭ���� `www.cloudflare.com`��`LE_EMAIL` ��ѡ������ Let's Encrypt �˻�֪ͨ��

## ������

| ��Ŀ | λ�û�˿� |
| --- | --- |
| Xray �ڵ� | TCP `443`���������� |
| HTTPS ���� | TCP `8443`����� URL |
| ֤����֤ | TCP `80`�����Զ�����ʹ�� |
| Clash ���� | `/root/clash-node/profile.yaml` |
| Xray ���� | `/usr/local/etc/xray/config.json` |

Ĭ�Ϸ���ֻ�� `GEOIP,CN,DIRECT` �� `MATCH,PROXY`�����Ҫ�������� Clash �ĸ��ӹ���ʹ�òֿ��е� [Codex Skill](SKILL.md) ��鵱ǰ�������ò��ϲ����򣻲�Ҫ�����ϴ����ڵ�ƾ�ݵĶ����ļ���

�ű�������ȫ�·���������⵽���� Xray������Ŀ¼�� `80/443/8443` �˿ڱ�ռ��ʱ��ֹͣ�������Ḳ�����нڵ㡣IP ��ַ֤����Ч�ڽ϶̣��ű��ᰲװ�Զ���������ִ������������

## Codex Skill

[SKILL.md](SKILL.md) ��¼�˲���ǰ��顢ƾ�ݴ��������й���Ǩ�ƺͶ˵�����֤���̡��ɽ��ֿ���Ϊ�Զ��� Skill ��װ��һ���ű�λ�� [scripts/deploy.sh](scripts/deploy.sh)��

## ����

- [Xray �ٷ� Reality ����ʾ��](https://github.com/XTLS/Xray-examples/blob/main/VLESS-TCP-XTLS-Vision-REALITY/config_server.jsonc)
- [Xray �ٷ���װ�ű�](https://github.com/XTLS/Xray-install)
- [Let's Encrypt �� IP ��ַ֤��˵��](https://letsencrypt.org/2026/03/11/shorter-certs-certbot.html)
