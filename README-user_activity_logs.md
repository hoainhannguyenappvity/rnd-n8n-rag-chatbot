# User Activity Logs Collection Query

```bash
db.user_activity_logs.find({})
db.user_activity_logs.find({}).map((item)=> `_id:${item._id} ~ timestamp:${item.timestamp} ~ user_id:${item.user_id} ~ activity_type:${item.activity_type} ~ ip_address:${item.ip_address} ~ device: ${item.device} ~ browser: ${item.browser} ~ status: ${item.status} ~ duration_seconds: ${item.duration_seconds} ~ page_url: ${item.page_url}`)
```
