# homelab-nvr

[Frigate](https://frigate.video) NVR for three RTSP cameras on a 4-thread Intel i3
(Skylake): object detection runs on the iGPU with OpenVINO, video decode uses VAAPI.

- Recordings: `${RECORDINGS}` (on the storage pool), motion 14 days, alerts 30 days, detections 14 days.
- Config: copy `config/config.example.yml` to `${APPDATA}/frigate/config.yml`. Camera logins
  and IPs are filled from `FRIGATE_*` variables in `.env`; Frigate substitutes `{FRIGATE_*}` itself.

```bash
cp .env.example .env
docker compose up -d
```

Web UI: `https://<host>:8971`.
