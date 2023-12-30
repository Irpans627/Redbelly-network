#  Cara deploy Smart contract Redbelly-network
![alt text](https://github.com/Irpans627/Redbelly-network/blob/main/redbelly%20banner%201.png?raw=true)

 
  ### 1.Persiapkan Wallet Metamask  
  Pertama tama kamu harus Menambahkan RPC redbelly secara Manual Ke metamaskmu Yang Tentuka Kamu Harus mempunyai Token **RBNT**
  - Network Name: Devnet Redbelly
  * RPC URL: https://rbn-gcp-australia-southeast1-a-0-b-v2.devnet.redbelly.network:8545
  * ChainID: 152
  * Currency Symbol: **RBNT**
  * Block explorer URL: https://explorer.devnet.redbelly.network
  * Seperti Ini Contohnya
   ![Screenshot (624)](https://github.com/Irpans627/Redbelly-network/assets/121398277/61e39f92-9c4a-4336-8b31-ca205a7ef166)

Setelah menambahkan Redbelly Devnet secara manual, Anda memerlukan Token RBNT,anda bisa mengambil faucet ke Redbelly Discord: https://discord.gg/redbelly 
Dan tempelkan dompet Anda di #devnet-faucet.

Setelah anda mendapatkan faucet anda bisa langsung lanjut ke step berikutnya dengan mengunjungi web https://remix.ethereum.org/
tampilannya seperti ini 
![Screenshot (625)](https://github.com/Irpans627/Redbelly-network/assets/121398277/ee08dcfa-0014-43da-bebe-2cd77e15ae53)
Klik buat file baru dengan name `` Smartcontract.sol ``
![Screenshot (625)](https://github.com/Irpans627/Redbelly-network/assets/121398277/c53a2a5e-c8a3-4e4e-84ea-5575b862358a)
Setelah membuat file bernama ``Smartcontract.sol`` copy script di bawah

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.4;
contract FunctionTypes{
 uint256 public number = 5;
 
 constructor() payable {}

 function add() external{
 number = number + 1;
 }
 function addPure(uint256 _number) external pure returns(uint256 new_number){
 new_number = _number+1;
 }
 
 function addView() external view returns(uint256 new_number) {
 new_number = number + 1;
 }
 function minus() internal {
 number = number - 1;
 }
 function minusCall() external {
 minus();
 }
 function minusPayable() external payable returns(uint256 balance) {
 minus(); 
 balance = address(this).balance;
 }
}
```
![Screenshot (626)](https://github.com/Irpans627/Redbelly-network/assets/121398277/f640c35d-3f08-4393-91bc-39e527bd672c)
lalu compile sampai muncul notif Ceklis Hijau seperti pada gambar 
![Screenshot (627)](https://github.com/Irpans627/Redbelly-network/assets/121398277/4f1ed07c-9fe6-419b-abb6-b44e1cd6aa60)
sekarang step terakir arahkan Ke bawah dan ikuti gambar dan arahkan ke wallet ``Injected Provider - MetaMask``





