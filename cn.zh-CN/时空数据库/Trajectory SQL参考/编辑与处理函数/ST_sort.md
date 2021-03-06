# ST\_sort {#reference_ssh_rqp_3gb .reference}

轨迹按时间序列从小到大重新排序，并返回新的轨迹对象。

## 语法 {#section_og1_4hn_qfb .section}

```
trajectory ST_sort(trajectory traj);
```

## 参数 {#section_cxv_qhn_qfb .section}

|参数名称|描述|
|----|--|
|traj|轨迹对象。|

## 示例 {#section_lmw_qhn_qfb .section}

```
select st_sort(ST_makeTrajectory('STPOINT'::leaftype, 'LINESTRING(-179.48077 51.72814,-179.46731 51.74634,-179.46502 51.74934,-179.46183 51.75378,-179.45943 51.75736,-179.45560 51.76273,-179.44845 51.77186,-179.43419 51.78977,-179.41259 51.81643,-179.41001 51.81941,-179.40751 51.82223,-179.40497 51.82505,-179.40242 51.82796,-179.39981 51.83095,-179.39734 51.83398,-179.39499 51.83709)'::geometry, ARRAY['2017-01-15 09:06:39'::timestamp,'2017-01-15 09:14:48'::timestamp,'2017-01-15 09:13:39'::timestamp,'2017-01-15 09:16:28'::timestamp,'2017-01-15 09:19:48'::timestamp,'2017-01-15 09:17:48'::timestamp,'2017-01-15 09:23:19'::timestamp,'2017-01-15 09:34:40'::timestamp,'2017-01-15 09:30:28'::timestamp,'2017-01-15 09:36:59'::timestamp,'2017-01-15 09:38:09'::timestamp,'2017-01-15 09:39:18'::timestamp,'2017-01-15 09:40:40'::timestamp,'2017-01-15 09:47:38'::timestamp,'2017-01-15 21:18:30'::timestamp,'2017-01-15 09:48:49'::timestamp], '{"leafcount": 16, "attributes" : {"heading" : {"type": "integer", "length": 4, "nullable" : false,"value":[0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15]}}}' ));                                                               
                                                              st_sort                                                                                                              
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 {"trajectory":{"version":1,"type":"STPOINT","leafcount":16,"start_time":"2017-01-15 09:06:39","end_time":"2017-01-15 21:18:30","spatial":"LINESTRING(-179.48077 51.72814,-179.46502 51.7
4934,-179.46731 51.74634,-179.46183 51.75378,-179.4556 51.76273,-179.45943 51.75736,-179.44845 51.77186,-179.41259 51.81643,-179.43419 51.78977,-179.41001 51.81941,-179.40751 51.82223,-
179.40497 51.82505,-179.40242 51.82796,-179.39981 51.83095,-179.39499 51.83709,-179.39734 51.83398)","timeline":["2017-01-15 09:06:39","2017-01-15 09:13:39","2017-01-15 09:14:48","2017-
01-15 09:16:28","2017-01-15 09:17:48","2017-01-15 09:19:48","2017-01-15 09:23:19","2017-01-15 09:30:28","2017-01-15 09:34:40","2017-01-15 09:36:59","2017-01-15 09:38:09","2017-01-15 09:
39:18","2017-01-15 09:40:40","2017-01-15 09:47:38","2017-01-15 09:48:49","2017-01-15 21:18:30"],"attributes":{"leafcount":16,"heading":{"type":"integer","length":4,"nullable":false,"val
ue":[0,2,1,3,5,4,6,8,7,9,10,11,12,13,15,14]}}}}
(1 row)
```

