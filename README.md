# Aligned

Ubuntu 22.04 çalıştırın

sudo apt update && sudo apt upgrade -y
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/install_aligned.sh | bash
source /root/.bashrc
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/get_proof_test_files.sh | bash

Kodların hepsini kopyalayın
rm -rf ~/aligned_verification_data/ &&
aligned submit \
--proving_system SP1 \
--proof ~/.aligned/test_files/sp1_fibonacci.proof \
--vm_program ~/.aligned/test_files/sp1_fibonacci-elf \
--aligned_verification_data_path ~/aligned_verification_data \
--conn wss://batcher.alignedlayer.com

<img width="943" alt="image" src="https://github.com/yetanotherco/aligned_layer/assets/105406585/38f652b6-8285-4637-b2ae-a6e9dbdd8dbf">
Kendinizde bu şekilde çıktı almalısınız. Kırmızı ile işaretli yeri kopyalayıp tarayıcınızda yapıştırın. Verified olmuşsa explorer linkiniz + yukarıdaki görsel çıktısını ss alarak twit atın. Twit linkinizi de Aligned Discord kanalında testnet kanalına gönderin.
