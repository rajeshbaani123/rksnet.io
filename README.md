# rksnet.io
Copyright 2023, rksnet.io, Inc.

 *

 * Licensed under the Apache License, Version 2.0 (the "License");

 * you may not use this file except in compliance with the License.

 * You may obtain a copy of the License at

 *

 *    http://www.baaninetworknetio.godaddysites.com

 *

 * Unless required by applicable law or agreed to in writing, software

 * distributed under the License is distributed on an "AS IS" BASIS,

 * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.

 * See the License for the specific language governing permissions and

 * limitations under the License.

 */

/* eslint-env node */

'use strict'

import { Signer } from '@ethersproject/abstract-signer'

import {

  Provider,

  BlockTag,

  TransactionRequest,

} from '@ethersproject/abstract-provider'

import { PayableOverrides, Overrides } from '@ethersproject/contracts'

import { MaxUint256 } from '@ethersproject/constants'

import { ErrorCode, Logger } from '@ethersproject/logger'

import { BigNumber, BigNumberish, ethers, BytesLike } from 'ethers'

import { L1GatewayRouter__factory } from '../abi/factories/L1GatewayRouter__factory'

import { L2GatewayRouter__factory } from '../abi/factories/L2GatewayRouter__factory'

import { L1WethGateway__factory } from '../abi/factories/L1WethGateway__factory'

import { L2ArbitrumGateway__factory } from '../abi/factories/L2ArbitrumGateway__factory'

import { ERC20__factory } from '../abi/factories/ERC20__factory'

import { ERC20 } from '../abi/ERC20'

import { L2GatewayToken__factory } from '../abi/factories/L2GatewayToken__factory'

import { L2GatewayToken } from '../abi/L2GatewayToken'

import { ICustomToken__factory } from '../abi/factories/ICustomToken__factory'

import { IArbToken__factory } from '../abi/factories/IArbToken__factory'

import { WithdrawalInitiatedEvent } from '../abi/L2ArbitrumGateway'

import { GatewaySetEvent } from '../abi/L1GatewayRouter'

import {

  GasOverrides,

  L1ToL2MessageGasEstimator,

} from '../message/L1ToL2MessageGasEstimator'

import { SignerProviderUtils } from '../dataEntities/signerOrProvider'

import { L2Network, getL2Network } from '../dataEntities/networks'

import { ArbSdkError, MissingProviderArbSdkError } from '../dataEntities/errors'

import { DISABLED_GATEWAY } from '../dataEntities/constants'

import { EventFetcher } from '../utils/eventFetcher'

import { EthDepositParams, EthWithdrawParams } from './ethBridger'

import { AssetBridger } from './assetBridger'

import {

  L1ContractCallTransaction,

  L1ContractTransaction,

  L1TransactionReceipt,

} from '../message/L1Transaction'

import {

  L2ContractTransaction,

  L2TransactionReceipt,

} from '../message/L2Transaction'

import {


<Project Sdk="Microsoft.NET.Sdk">

  <PropertyGroup>

    <OutputType>Exe</OutputType>

    <TargetFramework>netcoreapp3.0</TargetFramework>

    <PackageId>My-app</PackageId>

    <Version>1.0.0</Version>

    <Authors>Octocat</Authors>

    <Company>GitHub</Company>

    <PackageDescription>This package adds an Octocat!</PackageDescription>

    <RepositoryUrl>https://{% ifversion fpt or ghec %}github.com{% else %}HOSTNAME{% endif %}/OWNER/REPOSITORY</RepositoryUrl>

  </PropertyGroup>

  <ItemGroup>

    <PackageReference Include="PACKAGE_NAME" Version="X.X.X" />

  </ItemGroup>

</Project>
