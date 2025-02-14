# Snowflake

Cloud: https://app.snowflake.com/

# Schema

## blocks.parquet

| Column            | Type     |
|-------------------|----------|
| number            | BIGINT   |
| hash              | VARCHAR  |
| parent_hash       | VARCHAR  |
| nonce             | VARCHAR  |
| sha3_uncles       | VARCHAR  |
| logs_bloom        | VARCHAR  |
| transactions_root | VARCHAR  |
| state_root        | VARCHAR  |
| receipts_root     | VARCHAR  |
| difficulty        | VARCHAR  |
| total_difficulty  | VARCHAR  |
| size              | BIGINT   |
| extra_data        | VARCHAR  |
| gas_limit         | BIGINT   |
| gas_used          | BIGINT   |
| timestamp         | BIGINT   |
| transaction_count | BIGINT   |
| base_fee_per_gas  | BIGINT   |


## transactions.parquet

| Column                   | Type       |
|--------------------------|------------|
| hash                     | VARCHAR    |
| nonce                    | VARCHAR    |
| transaction_index        | BIGINT     |
| from_address             | VARCHAR    |
| to_address               | VARCHAR    |
| value                    | DOUBLE     |
| gas                      | BIGINT     |
| method_id                | VARCHAR    |
| input                    | VARCHAR    |
| max_fee_per_gas          | BIGINT     |
| max_priority_fee_per_gas | BIGINT     |
| transaction_type         | BIGINT     |
| block_hash               | VARCHAR    |
| block_number             | BIGINT     |
| block_timestamp          | BIGINT     |

## logs.parquet

| Column            | Type              |
|-------------------|-------------------|
| log_index         | BIGINT            |
| transaction_hash  | VARCHAR           |
| transaction_index | BIGINT            |
| block_hash        | VARCHAR           |
| block_number      | BIGINT            |
| contract_address  | VARCHAR           |
| event_address     | VARCHAR           |
| data              | VARCHAR           |
| topics            | VARCHAR           |


## receipts.parquet

| Column               | Type           |
|----------------------|----------------|
| transaction_hash     | VARCHAR        |
| transaction_index    | BIGINT         |
| block_hash           | VARCHAR        |
| block_number         | BIGINT         |
| cumulative_gas_used  | BIGINT         |
| gas_used             | BIGINT         |
| contract_address     | VARCHAR        |
| root                 | VARCHAR        |
| status               | BIGINT         |
| effective_gas_price  | BIGINT         |

## token_transfers.parquet

| Column             | Type             |
|--------------------|------------------|
| token_address      | VARCHAR          |
| from_address       | VARCHAR          |
| to_address         | VARCHAR          |
| token_id           | VARCHAR          |
| value              | VARCHAR          |
| erc_standard       | VARCHAR          |
| transaction_hash   | VARCHAR          |
| log_index          | BIGINT           |
| block_number       | BIGINT           |

## ens.parquet

| Column             | Type             |
|--------------------|------------------|
| name               | VARCHAR          |
| cost               | DOUBLE           |
| expires            | BIGINT           |
| owner              | VARCHAR          |
| transaction_hash   | VARCHAR          |
| block_number       | BIGINT           |
