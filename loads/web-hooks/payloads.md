# Webhook Payloads

## Load Activated `load.activated`

```
{
    "when": "2017-03-23T08:32:10.069287Z",
    "where": [ 0, 0 ],
    "load_id": "string",
    "reference": "string",
    "requested_date": "2017-03-23T08:30:50.2078258Z",
    "allocation": {
    "driver": {
        "id": "string",
        "name": "string",
        "reference": "string"
    },
    "vehicle": {
        "id": "string",
        "reference": "string",
        "registration": "string",
        "fleet_number": "string"
    },
    "assets": [],
    "accessories": {
        "pallet_jack": null,
        "load_lock_rails": 0,
        "fuel_card": null
    }
}
```

## Pickup Strated `load.pickup.started`

```
```

## Pickup Completed `load.pickup.completed`

```
```

## Dropoff Started `load.dropoff.started`

```
```

## Dropoff Completed `load.dropoff.completed`

```
```
