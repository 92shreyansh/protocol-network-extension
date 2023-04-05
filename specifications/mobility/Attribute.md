## Tags


| Attributes                                                       | Brief Description                                            | Sample Value                                                               | Technical Field``Specification |
| ---------------------------------------------------------------- | ------------------------------------------------------------ | -------------------------------------------------------------------------- | ------------------------------ |
| tags.groups/<group_#>/descriptor/name                            | name of tag group                                            | "Daytime Charges"                                                          | String                         |
| tags.groups/<group_#>/descriptor/code                            | code for the particular tag group                            | "fare_policy"                                                              | String                         |
| tags.groups/<group_#>/display                                    | should this be displayed to end User                         | "true"                                                                     | boolean (default: true)        |
| tags.groups/<group_#>/list/<list_serial_#>/descriptor/name       | name of the element in list for above tag group              | "Min Fare upto 2 km"                                                       | String                         |
| tags.groups/<group_#>/list/<list_serial_#>/descriptor/code       | code of the element in list for above tag group              | "extra_fare"                                                               | String                         |
| tags.groups/<group_#>/list/<list_serial_#>/descriptor/short_desc | short description of the element in list for above tag group | "Driver may quote extra to cover for traffic, chance of return trip, etc." | String                         |
| tags.groups/<group_#>/list/<list_serial_#>/value                 | value of element in list for above tag group                 | "₹15 / km"                                                                | String                         |


### Provider Tags

| list_code           | name                | sample values | Description |
| ------------------- | ------------------- | ------------- | ----------- |
| "rides_confirmed"   | "Rides confirmed"   | "0"           |             |
| "rides_in_progress" | "Rides In Progress" | "0"           |             |
| "rides_completed"   | "Rides Completed"   | "0"           |             |

### Item Tags

| list_code                          | name                         | sample values                                                    | Description                                                                    |
| ---------------------------------- | ---------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| "extra_fare"                       | "Min Fare upto 2 km"         | "₹15 / km"                                                      | extra fare along with currency value                                           |
| "pickup_charges"                   | "Driver Pickup Charges"      | "₹ 10"                                                          | Pick up charges by the driver along with currency value                        |
| "nominal_fare"                     | "Nominal Fare"               | "₹ 10"                                                          | Nominal Fare by the driver along with currency value                           |
| "waiting_charges"                  | "Waiting Charges"            | "₹ 0 / min"                                                     | Waiting charges along with currency value                                      |
| "night_charges"                    | "Night Charges"              | "1.5x of daytime charges applicable at night from 10 PM to 5 PM" | Night Charges conditions as String                                             |
| "night_shift_start_time"           | "Night Shift Start"          | "T22:00:00"                                                      | Night Shift start time using ISO8601 format can be exact time or range of time |
| "night_shift_end_time"             | "Night Shift End"            | "T05:00:00"                                                      | Night Shift End time using ISO8601 format can be exact time or range of time   |
|                                    |                              |                                                                  |                                                                                |
| "distance_to_nearest_driver"       | "Distance to nearest driver" | "661 m"                                                          | Distance to nearest driver with distance units                                 |
| "waiting_time_estimated_threshold" | "Wait time upto"             | "PT3M"                                                           | Wait time using ISO8601 format as duration                                     |

### Fulfilment Tags

| list_code          | name        | sample values                                                                                                                                           | Description                                                |
| ------------------ | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------- |
| "encoded_polyline" | "Path"      | "_p~iF~ps                                                                                                                                              | U_ulLnnqC_mqNvxq`@"                                        |
| "waypoints"        | "Waypoints" | "[{\"gps\":\"12.9099828, 77.6118226\"},{\"gps\":\"12.9099828, 77.6118226\"},{\"gps\":\"12.9099828, 77.6118226\"},{\"gps\":\"12.9099828, 77.6118226\"}]" | contains multiple gps points , being saved in encoded json |


### Customer/Person Tag

| list_code | name       | sample values | Description            |
| --------- | ---------- | ------------- | ---------------------- |
| "lang"    | "Language" | "en"          | follow ISO 639-1 codes |
