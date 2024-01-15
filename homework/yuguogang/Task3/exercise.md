(base) ygg@MacBook-Air-2 Ownable-contract-snFoundry-main % starkli deploy 0x0585f86478c05aab66a1cb29496dfdb84fe8729a170a46f010af95574a1e5d5c 0x047333dacb25b076c21280c2ef4ba76b6f8d14b88892a4cd8c9abf670afc10cf
Enter keystore password: 
Deploying class 0x0585f86478c05aab66a1cb29496dfdb84fe8729a170a46f010af95574a1e5d5c with salt 0x071f4320daee49a059c10d0b2bcd2cd03d641ca9d9491e574c8d84282afe382a...
The contract will be deployed at address 0x07e7a4eb1d63354f67bb88b07556688817b86a85b5048660b3fc93375fc2edd3
Contract deployment transaction: 0x067f6c991b14546b5897885d6f528276856d904357b8c161e7e59d9c688e8259
Contract deployed:
0x07e7a4eb1d63354f67bb88b07556688817b86a85b5048660b3fc93375fc2edd3
(base) ygg@MacBook-Air-2 Ownable-contract-snFoundry-main % starkl
i call 0x07e7a4eb1d63354f67bb88b07556688817b86a85b5048660b3fc93375fc2edd3 read_owner
[
    "0x047333dacb25b076c21280c2ef4ba76b6f8d14b88892a4cd8c9abf670afc10cf"
]
(base) ygg@MacBook-Air-2 Ownable-contract-snFoundry-main % starkli call 0x07e7a4eb1d63354f67bb88b07556688817b86a85b5048660b3fc93375fc2edd3 get_data  
[
    "0x0000000000000000000000000000000000000000000000000000000000000001"
]
(base) ygg@MacBook-Air-2 Ownable-contract-snFoundry-main % starkli invoke 0x07e7a4eb1d63354f67bb88b07556688817b86a85b5048660b3fc93375fc2edd3 set_data 0x12345
Enter keystore password: 
Invoke transaction: 0x0413043072141ceab23402c0363f98cb8e6bf96947f98a16cdcc31e5bec19628
(base) ygg@MacBook-Air-2 Ownable-contract-snFoundry-main % starkli call 0x07e7a4eb1d63354f67bb88b07556688817b86a85b5048660b3fc93375fc2edd3 get_data 
[
    "0x0000000000000000000000000000000000000000000000000000000000012345"
]
(base) ygg@MacBook-Air-2 Ownable-contract-snFoundry-main % snforge test
   Compiling ownable_starknet v0.1.0 (/Users/ygg/vs/StarknetBootcamp/homework/yuguogang/Task3/Ownable-contract-snFoundry-main/Scarb.toml)
    Finished release target(s) in 2 seconds


Collected 4 test(s) from ownable_starknet package
Running 0 test(s) from src/
Running 4 test(s) from tests/
[PASS] tests::test_ownable::test_transfer_ownership, gas: ~13.71
[PASS] tests::test_ownable::test_transfer_ownership_bad_guy, gas: ~6.2
[PASS] tests::test_ownable::test_construct_with_admin, gas: ~7.140000000000001
[PASS] tests::test_ownable::test_data_mock_call_get_data, gas: ~13.32
Tests: 4 passed, 0 failed, 0 skipped, 0 ignored, 0 filtered out
(base) ygg@MacBook-Air-2 Ownable-contract-snFoundry-main % 

##deploy and interact with ownablecomponent
(base) ygg@MacBook-Air-2 ownable-components-main % starkli declare target/dev/ownable_project_ownable_contract.contract_class.json
Enter keystore password: 
Not declaring class as it's already declared. Class hash:
0x063104c93f7c749ff2e8baed06872e4cd541291fd0f7745e91566e0e3a835e1b
(base) ygg@MacBook-Air-2 ownable-components-main % starkli deploy 0x063104c93f7c749ff2e8baed06872e4cd541291fd0f7745e91566e0e3a835e1b 0x047333dacb25b076c21280c2ef4ba76b6f8d14b88892a4cd8c9abf670afc10cf
Enter keystore password: 
Deploying class 0x063104c93f7c749ff2e8baed06872e4cd541291fd0f7745e91566e0e3a835e1b with salt 0x066d8545431ef068c5f46b2fc15be561a5ab372ada56595f88b008d4329d1c17...
The contract will be deployed at address 0x05c7d913c56b61d3dba6d3669f37646b8c5ccf1c78228903ca0571b11bd1488c
Contract deployment transaction: 0x056498f28ae8129c6fe5dad8a27cca25f8fa6a21d5ac4d97aae2b13be08fd85d
Contract deployed:
0x05c7d913c56b61d3dba6d3669f37646b8c5ccf1c78228903ca0571b11bd1488c
(base) ygg@MacBook-Air-2 ownable-components-main % starkli call 0x05c7d913c56b61d3dba6d3669f37646b8c5ccf1c78228903ca0571b11bd1488c owner
[
    "0x047333dacb25b076c21280c2ef4ba76b6f8d14b88892a4cd8c9abf670afc10cf"
]
(base) ygg@MacBook-Air-2 ownable-components-main % starkli call 0x05c7d913c56b61d3dba6d3669f37646b8c5ccf1c78228903ca0571b11bd1488c get_data
[
    "0x0000000000000000000000000000000000000000000000000000000000000001"
]
(base) ygg@MacBook-Air-2 ownable-components-main % starkli invoke 0x05c7d913c56b61d3dba6d3669f37646b8c5ccf1c78228903ca0571b11bd1488c set_data 0x123456789
Enter keystore password: 
Invoke transaction: 0x07f08ce536be8e8d54093c7e1e3b33051f01dcc52a6a99faafdcd4481f7c0d97
(base) ygg@MacBook-Air-2 ownable-components-main % starkli call 0x05c7d913c56b61d3dba6d3669f37646b8c5ccf1c78228903ca0571b11bd1488c get_data              
[
    "0x0000000000000000000000000000000000000000000000000000000123456789"
]