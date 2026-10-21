# Asset


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**asset_id** | **int** |  | 
**symbol** | **str** |  | 
**l1_decimals** | **int** | Token decimals, present only when canonical_domain is 1 (L1). Linking a wrapper never adds evm_decimals: the wrapper uses these decimals. | [optional] 
**evm_decimals** | **int** | Token decimals, present only when canonical_domain is 3 (EVM). Linking a wrapper never adds l1_decimals: the wrapper uses these decimals. Zero is a valid precision. | [optional] 
**canonical_domain** | **int** | Asset origin: 0 not registered, 1 L1, 2 Core, 3 EVM. Selects which decimals field is present; Core-native and unregistered assets have neither. Omitted by older API versions. | [optional] 
**evm_token** | **str** | Linked EVM token or wrapper address. The zero address means unlinked; older API versions omit this field. | [optional] 
**decimals** | **int** |  | 
**min_transfer_amount** | **str** |  | 
**min_withdrawal_amount** | **str** |  | 
**margin_mode** | **str** |  | 
**index_price** | **str** |  | 
**l1_address** | **str** |  | 
**global_supply_cap** | **str** |  | 
**liquidation_fee** | **str** |  | 
**liquidation_threshold** | **str** |  | 
**loan_to_value** | **str** |  | 
**price_decimals** | **int** |  | 
**total_supplied** | **str** |  | 
**user_supply_cap** | **str** |  | 
**liquidation_factor** | **str** |  | 
**multiplier** | **str** |  | 

## Example

```python
from lighter.models.asset import Asset

# TODO update the JSON string below
json = "{}"
# create an instance of Asset from a JSON string
asset_instance = Asset.from_json(json)
# print the JSON string representation of the object
print(Asset.to_json())

# convert the object into a dict
asset_dict = asset_instance.to_dict()
# create an instance of Asset from a dict
asset_from_dict = Asset.from_dict(asset_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


