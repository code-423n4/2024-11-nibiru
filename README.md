

# Scope

*See [scope.txt](https://github.com/code-423n4/2024-11-nibiru/blob/main/scope.txt)*

### Files in scope


| File   | Logic Contracts | Interfaces | nSLOC | Purpose | Libraries used |
| ------ | --------------- | ---------- | ----- | -----   | ------------ |

| **Totals** | **** | **** | **undefined** | | |

### Files out of scope

*See [out_of_scope.txt](https://github.com/code-423n4/2024-11-nibiru/blob/main/out_of_scope.txt)*

| File         |
| ------------ |
| ./app/ante/auth_grard_test.go |
| ./app/ante/authz_guard.go |
| ./app/ante/commission.go |
| ./app/ante/commission_test.go |
| ./app/ante/errors.go |
| ./app/ante/fixed_gas.go |
| ./app/ante/fixed_gas_test.go |
| ./app/ante/gas.go |
| ./app/ante/gas_wanted.go |
| ./app/ante/gas_wanted_test.go |
| ./app/ante/handler_opts.go |
| ./app/ante/reject_ethereum_tx_msgs.go |
| ./app/ante/reject_ethereum_tx_msgs_test.go |
| ./app/ante/testutil_test.go |
| ./app/ante.go |
| ./app/app.go |
| ./app/appconst/appconst.go |
| ./app/appconst/appconst_test.go |
| ./app/appconst/consensus_config.go |
| ./app/appconst/pebbledb.go |
| ./app/codec/codec.go |
| ./app/encoding.go |
| ./app/evmante/evmante_can_transfer_test.go |
| ./app/evmante/evmante_emit_event_test.go |
| ./app/evmante/evmante_gas_consume_test.go |
| ./app/evmante/evmante_handler_test.go |
| ./app/evmante/evmante_increment_sender_seq_test.go |
| ./app/evmante/evmante_mempool_fees_test.go |
| ./app/evmante/evmante_setup_ctx_test.go |
| ./app/evmante/evmante_sigverify_test.go |
| ./app/evmante/evmante_validate_basic_test.go |
| ./app/evmante/evmante_verify_eth_acc_test.go |
| ./app/evmante/suite_test.go |
| ./app/export.go |
| ./app/genesis.go |
| ./app/ibc_test.go |
| ./app/keepers/all_keepers.go |
| ./app/keepers.go |
| ./app/modules.go |
| ./app/modules_test.go |
| ./app/prefix.go |
| ./app/server/config/server_config.go |
| ./app/server/evm_tx_indexer_cli.go |
| ./app/server/evm_tx_indexer_service.go |
| ./app/server/flags.go |
| ./app/server/json_rpc.go |
| ./app/server/start.go |
| ./app/server/util.go |
| ./app/sim/config.go |
| ./app/upgrades/types.go |
| ./app/upgrades/v1_1_0/constants.go |
| ./app/upgrades/v1_2_0/constants.go |
| ./app/upgrades/v1_3_0/constants.go |
| ./app/upgrades/v1_4_0/constants.go |
| ./app/upgrades/v2_1_0/constants.go |
| ./app/upgrades.go |
| ./app/wasmext/stargate_query.go |
| ./app/wasmext/stargate_query_test.go |
| ./app/wasmext/wasm.go |
| ./app/wasmext/wasm_cli_test/cli_test.go |
| ./cmd/nibid/cmd/base64.go |
| ./cmd/nibid/cmd/decode_base64.go |
| ./cmd/nibid/cmd/decode_base64_test.go |
| ./cmd/nibid/cmd/genaccounts.go |
| ./cmd/nibid/cmd/genaccounts_test.go |
| ./cmd/nibid/cmd/init.go |
| ./cmd/nibid/cmd/root.go |
| ./cmd/nibid/cmd/root_test.go |
| ./cmd/nibid/cmd/testnet.go |
| ./cmd/nibid/cmd/testnet_test.go |
| ./cmd/nibid/main.go |
| ./eth/account.pb.go |
| ./eth/assert.go |
| ./eth/assert_test.go |
| ./eth/chain_id.go |
| ./eth/chain_id_test.go |
| ./eth/codec.go |
| ./eth/codec_test.go |
| ./eth/crypto/codec/amino.go |
| ./eth/crypto/codec/codec.go |
| ./eth/crypto/ethsecp256k1/benchmark_test.go |
| ./eth/crypto/ethsecp256k1/ethsecp256k1.go |
| ./eth/crypto/ethsecp256k1/ethsecp256k1_test.go |
| ./eth/crypto/ethsecp256k1/keys.pb.go |
| ./eth/crypto/hd/algorithm.go |
| ./eth/crypto/hd/algorithm_test.go |
| ./eth/crypto/hd/benchmark_test.go |
| ./eth/crypto/hd/utils_test.go |
| ./eth/crypto/keyring/options.go |
| ./eth/crypto/secp256r1/verify.go |
| ./eth/eip55.go |
| ./eth/eip55_test.go |
| ./eth/eip712/domain.go |
| ./eth/eip712/eip712.go |
| ./eth/eip712/eip712_fuzzer_test.go |
| ./eth/eip712/eip712_legacy.go |
| ./eth/eip712/eip712_test.go |
| ./eth/eip712/encoding.go |
| ./eth/eip712/encoding_legacy.go |
| ./eth/eip712/message.go |
| ./eth/eip712/types.go |
| ./eth/encoding/codec/codec.go |
| ./eth/encoding/config.go |
| ./eth/encoding/config_test.go |
| ./eth/errors.go |
| ./eth/eth_account.go |
| ./eth/eth_account_test.go |
| ./eth/gas_limit.go |
| ./eth/gas_limit_test.go |
| ./eth/hdpath.go |
| ./eth/indexer/evm_tx_indexer.go |
| ./eth/indexer/evm_tx_indexer_test.go |
| ./eth/indexer.go |
| ./eth/indexer.pb.go |
| ./eth/rpc/addrlocker.go |
| ./eth/rpc/addrlocker_test.go |
| ./eth/rpc/backend/account_info_test.go |
| ./eth/rpc/backend/backend_suite_test.go |
| ./eth/rpc/backend/blocks_test.go |
| ./eth/rpc/backend/call_tx_test.go |
| ./eth/rpc/backend/chain_info_test.go |
| ./eth/rpc/backend/client_test.go |
| ./eth/rpc/backend/node_info_test.go |
| ./eth/rpc/backend/tracing_test.go |
| ./eth/rpc/backend/tx_info_test.go |
| ./eth/rpc/backend/utils_test.go |
| ./eth/rpc/block.go |
| ./eth/rpc/block_test.go |
| ./eth/rpc/events_parser.go |
| ./eth/rpc/events_parser_test.go |
| ./eth/rpc/pubsub/pubsub.go |
| ./eth/rpc/pubsub/pubsub_test.go |
| ./eth/rpc/query_client.go |
| ./eth/rpc/rpc.go |
| ./eth/rpc/rpc_test.go |
| ./eth/rpc/rpcapi/apis.go |
| ./eth/rpc/rpcapi/debugapi/api.go |
| ./eth/rpc/rpcapi/debugapi/trace.go |
| ./eth/rpc/rpcapi/debugapi/trace_fallback.go |
| ./eth/rpc/rpcapi/debugapi/utils.go |
| ./eth/rpc/rpcapi/eth_api_test.go |
| ./eth/rpc/rpcapi/eth_filters_api.go |
| ./eth/rpc/rpcapi/event_subscriber.go |
| ./eth/rpc/rpcapi/event_subscriber_test.go |
| ./eth/rpc/rpcapi/filter_utils.go |
| ./eth/rpc/rpcapi/filters.go |
| ./eth/rpc/rpcapi/net_api.go |
| ./eth/rpc/rpcapi/net_api_test.go |
| ./eth/rpc/rpcapi/subscription.go |
| ./eth/rpc/rpcapi/txpool_api.go |
| ./eth/rpc/rpcapi/web3_api.go |
| ./eth/rpc/rpcapi/websockets.go |
| ./eth/rpc/types.go |
| ./eth/safe_math.go |
| ./eth/safe_math_test.go |
| ./eth/state_encoder.go |
| ./eth/state_encoder_test.go |
| ./eth/stringify.go |
| ./eth/stringify_test.go |
| ./evm-e2e/contracts/EventsEmitter.sol |
| ./evm-e2e/contracts/InfiniteLoopGas.sol |
| ./evm-e2e/contracts/SendReceiveNibi.sol |
| ./evm-e2e/contracts/TestERC20.sol |
| ./evm-e2e/contracts/TransactionReverter.sol |
| ./evm-forge/script/Base.s.sol |
| ./evm-forge/script/Deploy.s.sol |
| ./evm-forge/src/Foo.sol |
| ./evm-forge/test/Foo.t.sol |
| ./gosdk/broadcast.go |
| ./gosdk/clientctx.go |
| ./gosdk/export_test.go |
| ./gosdk/gosdk.go |
| ./gosdk/gosdk_test.go |
| ./gosdk/grpc.go |
| ./gosdk/keys.go |
| ./gosdk/keys_test.go |
| ./gosdk/netinfo.go |
| ./gosdk/querier.go |
| ./gosdk/rpc.go |
| ./simapp/sim_test.go |
| ./simapp/state_test.go |
| ./tools/tools.go |
| ./x/common/address.go |
| ./x/common/address_test.go |
| ./x/common/asset/pair.go |
| ./x/common/asset/pair_test.go |
| ./x/common/asset/registry.go |
| ./x/common/asset/registry_test.go |
| ./x/common/codec.go |
| ./x/common/constants.go |
| ./x/common/dec.go |
| ./x/common/dec_test.go |
| ./x/common/denoms/denoms.go |
| ./x/common/error.go |
| ./x/common/error_test.go |
| ./x/common/ewma/ewma.go |
| ./x/common/ewma/ewma_test.go |
| ./x/common/omap/impl.go |
| ./x/common/omap/omap.go |
| ./x/common/omap/omap_test.go |
| ./x/common/paginate.go |
| ./x/common/paginate_test.go |
| ./x/common/set/set.go |
| ./x/common/set/set_test.go |
| ./x/common/testutil/action/account.go |
| ./x/common/testutil/action/block.go |
| ./x/common/testutil/action/testcase.go |
| ./x/common/testutil/assertion/balances.go |
| ./x/common/testutil/assertion/gas.go |
| ./x/common/testutil/cases.go |
| ./x/common/testutil/cases_test.go |
| ./x/common/testutil/client_ctx.go |
| ./x/common/testutil/const.go |
| ./x/common/testutil/events.go |
| ./x/common/testutil/events_test.go |
| ./x/common/testutil/genesis/genesis.go |
| ./x/common/testutil/genesis/oracle_genesis.go |
| ./x/common/testutil/genesis/sudo_genesis.go |
| ./x/common/testutil/mock/mocks.go |
| ./x/common/testutil/nullify.go |
| ./x/common/testutil/path.go |
| ./x/common/testutil/sample.go |
| ./x/common/testutil/testapp/test_util.go |
| ./x/common/testutil/testapp/testapp.go |
| ./x/common/testutil/testnetwork/doc.go |
| ./x/common/testutil/testnetwork/logger.go |
| ./x/common/testutil/testnetwork/network.go |
| ./x/common/testutil/testnetwork/network_config.go |
| ./x/common/testutil/testnetwork/network_test.go |
| ./x/common/testutil/testnetwork/query.go |
| ./x/common/testutil/testnetwork/start_node.go |
| ./x/common/testutil/testnetwork/tx.go |
| ./x/common/testutil/testnetwork/tx_test.go |
| ./x/common/testutil/testnetwork/util.go |
| ./x/common/testutil/testnetwork/validator_node.go |
| ./x/common/testutil/testutil_test.go |
| ./x/devgas/v1/ante/ante.go |
| ./x/devgas/v1/ante/ante_test.go |
| ./x/devgas/v1/ante/expected_keepers.go |
| ./x/devgas/v1/client/cli/cli_test.go |
| ./x/devgas/v1/client/cli/query.go |
| ./x/devgas/v1/client/cli/tx.go |
| ./x/devgas/v1/exported/exported.go |
| ./x/devgas/v1/genesis.go |
| ./x/devgas/v1/genesis_test.go |
| ./x/devgas/v1/keeper/feeshare.go |
| ./x/devgas/v1/keeper/grpc_query.go |
| ./x/devgas/v1/keeper/grpc_query_test.go |
| ./x/devgas/v1/keeper/keeper.go |
| ./x/devgas/v1/keeper/keeper_test.go |
| ./x/devgas/v1/keeper/msg_server.go |
| ./x/devgas/v1/keeper/msg_server_test.go |
| ./x/devgas/v1/keeper/params.go |
| ./x/devgas/v1/keeper/store.go |
| ./x/devgas/v1/module.go |
| ./x/devgas/v1/module_test.go |
| ./x/devgas/v1/simulation/genesis.go |
| ./x/devgas/v1/types/codec.go |
| ./x/devgas/v1/types/codec_test.go |
| ./x/devgas/v1/types/devgas.go |
| ./x/devgas/v1/types/devgas.pb.go |
| ./x/devgas/v1/types/devgas_test.go |
| ./x/devgas/v1/types/errors.go |
| ./x/devgas/v1/types/event.pb.go |
| ./x/devgas/v1/types/expected_keepers.go |
| ./x/devgas/v1/types/export.go |
| ./x/devgas/v1/types/genesis.go |
| ./x/devgas/v1/types/genesis.pb.go |
| ./x/devgas/v1/types/genesis_test.go |
| ./x/devgas/v1/types/keys.go |
| ./x/devgas/v1/types/msg.go |
| ./x/devgas/v1/types/msg_test.go |
| ./x/devgas/v1/types/params.go |
| ./x/devgas/v1/types/params_legacy.go |
| ./x/devgas/v1/types/params_legacy_test.go |
| ./x/devgas/v1/types/params_test.go |
| ./x/devgas/v1/types/query.go |
| ./x/devgas/v1/types/query.pb.go |
| ./x/devgas/v1/types/query.pb.gw.go |
| ./x/devgas/v1/types/tx.pb.go |
| ./x/devgas/v1/types/tx.pb.gw.go |
| ./x/epochs/abci.go |
| ./x/epochs/abci_test.go |
| ./x/epochs/client/cli/query.go |
| ./x/epochs/client/cli/tx.go |
| ./x/epochs/client/rest/rest.go |
| ./x/epochs/genesis.go |
| ./x/epochs/genesis_test.go |
| ./x/epochs/integration/action/epoch.go |
| ./x/epochs/keeper/epoch.go |
| ./x/epochs/keeper/grpc_query.go |
| ./x/epochs/keeper/grpc_query_test.go |
| ./x/epochs/keeper/hooks.go |
| ./x/epochs/keeper/hooks_test.go |
| ./x/epochs/keeper/keeper.go |
| ./x/epochs/keeper/keeper_test.go |
| ./x/epochs/module.go |
| ./x/epochs/simulation/genesis.go |
| ./x/epochs/types/epochinfo.go |
| ./x/epochs/types/epochinfo_test.go |
| ./x/epochs/types/errors.go |
| ./x/epochs/types/event.pb.go |
| ./x/epochs/types/export.go |
| ./x/epochs/types/genesis.go |
| ./x/epochs/types/genesis.pb.go |
| ./x/epochs/types/genesis_test.go |
| ./x/epochs/types/hooks.go |
| ./x/epochs/types/hooks_test.go |
| ./x/epochs/types/identifier.go |
| ./x/epochs/types/identifier_test.go |
| ./x/epochs/types/keys.go |
| ./x/epochs/types/query.pb.go |
| ./x/epochs/types/query.pb.gw.go |
| ./x/epochs/types/state.pb.go |
| ./x/evm/chain_config.go |
| ./x/evm/chain_config_test.go |
| ./x/evm/cli/cli_setup_test.go |
| ./x/evm/cli/cli_test.go |
| ./x/evm/cli/query.go |
| ./x/evm/cli/tx.go |
| ./x/evm/codec.go |
| ./x/evm/const.go |
| ./x/evm/deps.go |
| ./x/evm/embeds/contracts/ERC20Minter.sol |
| ./x/evm/embeds/contracts/IFunToken.sol |
| ./x/evm/embeds/contracts/IOracle.sol |
| ./x/evm/embeds/contracts/TestERC20.sol |
| ./x/evm/embeds/contracts/TestERC20MaliciousName.sol |
| ./x/evm/embeds/contracts/TestERC20MaliciousTransfer.sol |
| ./x/evm/embeds/contracts/TestERC20TransferThenPrecompileSend.sol |
| ./x/evm/embeds/contracts/TestFunTokenPrecompileLocalGas.sol |
| ./x/evm/embeds/contracts/TestNativeSendThenPrecompileSend.sol |
| ./x/evm/embeds/contracts/TestPrecompileSelfCallRevert.sol |
| ./x/evm/embeds/contracts/Wasm.sol |
| ./x/evm/embeds/embeds.go |
| ./x/evm/embeds/embeds_test.go |
| ./x/evm/errors.go |
| ./x/evm/events.go |
| ./x/evm/events.pb.go |
| ./x/evm/evm.go |
| ./x/evm/evm.pb.go |
| ./x/evm/evm_test.go |
| ./x/evm/evmmodule/genesis.go |
| ./x/evm/evmmodule/genesis_test.go |
| ./x/evm/evmmodule/module.go |
| ./x/evm/evmtest/erc20.go |
| ./x/evm/evmtest/eth.go |
| ./x/evm/evmtest/eth_test.go |
| ./x/evm/evmtest/evmante.go |
| ./x/evm/evmtest/signer.go |
| ./x/evm/evmtest/smart_contract.go |
| ./x/evm/evmtest/smart_contract_test.go |
| ./x/evm/evmtest/test_deps.go |
| ./x/evm/evmtest/tx.go |
| ./x/evm/evmtest/tx_test.go |
| ./x/evm/genesis.go |
| ./x/evm/genesis.pb.go |
| ./x/evm/genesis_test.go |
| ./x/evm/json_tx_args.go |
| ./x/evm/json_tx_args_test.go |
| ./x/evm/keeper/erc20_test.go |
| ./x/evm/keeper/funtoken_from_coin_test.go |
| ./x/evm/keeper/funtoken_from_erc20_test.go |
| ./x/evm/keeper/funtoken_state_test.go |
| ./x/evm/keeper/gas_fees_test.go |
| ./x/evm/keeper/grpc_query_test.go |
| ./x/evm/keeper/keeper_test.go |
| ./x/evm/keeper/msg_ethereum_tx_test.go |
| ./x/evm/keeper/statedb_test.go |
| ./x/evm/logs.go |
| ./x/evm/logs_test.go |
| ./x/evm/msg.go |
| ./x/evm/msg_test.go |
| ./x/evm/params.go |
| ./x/evm/precompile/funtoken_test.go |
| ./x/evm/precompile/oracle_test.go |
| ./x/evm/precompile/test/export.go |
| ./x/evm/precompile/wasm_test.go |
| ./x/evm/query.go |
| ./x/evm/query.pb.go |
| ./x/evm/query.pb.gw.go |
| ./x/evm/state.go |
| ./x/evm/state_test.go |
| ./x/evm/statedb/journal_test.go |
| ./x/evm/statedb/statedb_test.go |
| ./x/evm/tx.go |
| ./x/evm/tx.pb.go |
| ./x/evm/tx.pb.gw.go |
| ./x/evm/tx_data.go |
| ./x/evm/tx_data_access_list.go |
| ./x/evm/tx_data_access_list_test.go |
| ./x/evm/tx_data_dynamic_fee.go |
| ./x/evm/tx_data_dynamic_fee_test.go |
| ./x/evm/tx_data_legacy.go |
| ./x/evm/tx_data_legacy_test.go |
| ./x/evm/tx_data_test.go |
| ./x/evm/tx_test.go |
| ./x/evm/vmtracer.go |
| ./x/genmsg/genesis.go |
| ./x/genmsg/genesis_test.go |
| ./x/genmsg/integration_test.go |
| ./x/genmsg/module.go |
| ./x/genmsg/v1/genmsg.pb.go |
| ./x/inflation/client/cli/query.go |
| ./x/inflation/client/cli/tx.go |
| ./x/inflation/doc.go |
| ./x/inflation/genesis.go |
| ./x/inflation/keeper/grpc_query.go |
| ./x/inflation/keeper/grpc_query_test.go |
| ./x/inflation/keeper/hooks.go |
| ./x/inflation/keeper/hooks_test.go |
| ./x/inflation/keeper/inflation.go |
| ./x/inflation/keeper/inflation_test.go |
| ./x/inflation/keeper/keeper.go |
| ./x/inflation/keeper/keeper_test.go |
| ./x/inflation/keeper/msg_server.go |
| ./x/inflation/keeper/msg_server_test.go |
| ./x/inflation/keeper/params.go |
| ./x/inflation/keeper/sudo.go |
| ./x/inflation/keeper/sudo_test.go |
| ./x/inflation/module.go |
| ./x/inflation/simulation/genesis.go |
| ./x/inflation/types/codec.go |
| ./x/inflation/types/event.pb.go |
| ./x/inflation/types/events.go |
| ./x/inflation/types/export.go |
| ./x/inflation/types/genesis.go |
| ./x/inflation/types/genesis.pb.go |
| ./x/inflation/types/genesis_test.go |
| ./x/inflation/types/inflation.pb.go |
| ./x/inflation/types/inflation_calculation.go |
| ./x/inflation/types/inflation_calculation_test.go |
| ./x/inflation/types/interfaces.go |
| ./x/inflation/types/keys.go |
| ./x/inflation/types/msgs.go |
| ./x/inflation/types/params.go |
| ./x/inflation/types/params_test.go |
| ./x/inflation/types/query.pb.go |
| ./x/inflation/types/query.pb.gw.go |
| ./x/inflation/types/tx.pb.go |
| ./x/inflation/types/tx.pb.gw.go |
| ./x/oracle/abci.go |
| ./x/oracle/abci_test.go |
| ./x/oracle/cli/gen_pricefeeder_delegation.go |
| ./x/oracle/cli/gen_pricefeeder_delegation_test.go |
| ./x/oracle/cli/query.go |
| ./x/oracle/cli/tx.go |
| ./x/oracle/genesis.go |
| ./x/oracle/genesis_test.go |
| ./x/oracle/keeper/app_test.go |
| ./x/oracle/keeper/ballot.go |
| ./x/oracle/keeper/ballot_test.go |
| ./x/oracle/keeper/hooks.go |
| ./x/oracle/keeper/keeper.go |
| ./x/oracle/keeper/keeper_test.go |
| ./x/oracle/keeper/msg_server.go |
| ./x/oracle/keeper/msg_server_test.go |
| ./x/oracle/keeper/params.go |
| ./x/oracle/keeper/params_test.go |
| ./x/oracle/keeper/querier.go |
| ./x/oracle/keeper/querier_test.go |
| ./x/oracle/keeper/reward.go |
| ./x/oracle/keeper/reward_test.go |
| ./x/oracle/keeper/slash.go |
| ./x/oracle/keeper/slash_test.go |
| ./x/oracle/keeper/sudo.go |
| ./x/oracle/keeper/sudo_test.go |
| ./x/oracle/keeper/test_utils.go |
| ./x/oracle/keeper/update_exchange_rates.go |
| ./x/oracle/keeper/update_exchange_rates_test.go |
| ./x/oracle/keeper/whitelist.go |
| ./x/oracle/keeper/whitelist_test.go |
| ./x/oracle/module.go |
| ./x/oracle/simulation/decoder.go |
| ./x/oracle/simulation/decoder_test.go |
| ./x/oracle/simulation/genesis.go |
| ./x/oracle/simulation/operations.go |
| ./x/oracle/types/ballot.go |
| ./x/oracle/types/ballot_test.go |
| ./x/oracle/types/codec.go |
| ./x/oracle/types/core.go |
| ./x/oracle/types/errors.go |
| ./x/oracle/types/event.pb.go |
| ./x/oracle/types/expected_keeper.go |
| ./x/oracle/types/export.go |
| ./x/oracle/types/genesis.go |
| ./x/oracle/types/genesis.pb.go |
| ./x/oracle/types/genesis_test.go |
| ./x/oracle/types/hash.go |
| ./x/oracle/types/hash_test.go |
| ./x/oracle/types/keys.go |
| ./x/oracle/types/msgs.go |
| ./x/oracle/types/msgs_test.go |
| ./x/oracle/types/oracle.pb.go |
| ./x/oracle/types/params.go |
| ./x/oracle/types/params_test.go |
| ./x/oracle/types/query.pb.go |
| ./x/oracle/types/query.pb.gw.go |
| ./x/oracle/types/state.pb.go |
| ./x/oracle/types/test_utils.go |
| ./x/oracle/types/tx.pb.go |
| ./x/oracle/types/tx.pb.gw.go |
| ./x/oracle/types/vote.go |
| ./x/oracle/types/vote_test.go |
| ./x/sudo/cli/cli.go |
| ./x/sudo/cli/cli_test.go |
| ./x/sudo/cli/gen_root.go |
| ./x/sudo/cli/gen_root_test.go |
| ./x/sudo/doc.go |
| ./x/sudo/genesis.go |
| ./x/sudo/keeper/keeper.go |
| ./x/sudo/keeper/keeper_test.go |
| ./x/sudo/keeper/msg_server.go |
| ./x/sudo/keeper/msg_server_test.go |
| ./x/sudo/keeper/querier.go |
| ./x/sudo/keeper/querier_test.go |
| ./x/sudo/module.go |
| ./x/sudo/simulation/genesis.go |
| ./x/sudo/types/actions.go |
| ./x/sudo/types/codec.go |
| ./x/sudo/types/errors.go |
| ./x/sudo/types/event.pb.go |
| ./x/sudo/types/export.go |
| ./x/sudo/types/genesis.go |
| ./x/sudo/types/keys.go |
| ./x/sudo/types/msgs.go |
| ./x/sudo/types/query.pb.go |
| ./x/sudo/types/query.pb.gw.go |
| ./x/sudo/types/state.go |
| ./x/sudo/types/state.pb.go |
| ./x/sudo/types/tx.pb.go |
| ./x/sudo/types/tx.pb.gw.go |
| ./x/tokenfactory/cli/cli_test.go |
| ./x/tokenfactory/cli/query.go |
| ./x/tokenfactory/cli/tx.go |
| ./x/tokenfactory/fixture/fixture.go |
| ./x/tokenfactory/keeper/genesis.go |
| ./x/tokenfactory/keeper/genesis_test.go |
| ./x/tokenfactory/keeper/grpc_query.go |
| ./x/tokenfactory/keeper/grpc_query_test.go |
| ./x/tokenfactory/keeper/keeper.go |
| ./x/tokenfactory/keeper/keeper_test.go |
| ./x/tokenfactory/keeper/msg_server.go |
| ./x/tokenfactory/keeper/msg_server_test.go |
| ./x/tokenfactory/keeper/store.go |
| ./x/tokenfactory/keeper/store_test.go |
| ./x/tokenfactory/keeper/wasm_test.go |
| ./x/tokenfactory/module.go |
| ./x/tokenfactory/module_test.go |
| ./x/tokenfactory/simulation/genesis.go |
| ./x/tokenfactory/types/codec.go |
| ./x/tokenfactory/types/codec_test.go |
| ./x/tokenfactory/types/errors.go |
| ./x/tokenfactory/types/event.pb.go |
| ./x/tokenfactory/types/expected_keepers.go |
| ./x/tokenfactory/types/export.go |
| ./x/tokenfactory/types/genesis.go |
| ./x/tokenfactory/types/keys.go |
| ./x/tokenfactory/types/query.pb.go |
| ./x/tokenfactory/types/query.pb.gw.go |
| ./x/tokenfactory/types/state.go |
| ./x/tokenfactory/types/state.pb.go |
| ./x/tokenfactory/types/state_test.go |
| ./x/tokenfactory/types/tx.pb.go |
| ./x/tokenfactory/types/tx_msgs.go |
| ./x/tokenfactory/types/tx_msgs_test.go |
| Totals: 566 |

