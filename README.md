# Aligned

### Güncelleme

```bash
sudo apt update -y && sudo apt upgrade -y
```

### Kanıtları test ağına göndermek için Aligned'ı indirip yükleyin:

```bash 
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/install_aligned.sh | bash
```

```bash
source /root/.bashrc
```

### Aşağıdakileri kullanarak ELF dosyasıyla birlikte örnek bir SP1 kanıt dosyasını indirin:

```bash
curl -L https://raw.githubusercontent.com/yetanotherco/aligned_layer/main/batcher/aligned/get_proof_test_files.sh | bash
```

### Kanıtı gönder:
```bash
rm -rf ~/aligned_verification_data/ &&
aligned submit \
--proving_system SP1 \
--proof ~/.aligned/test_files/sp1_fibonacci.proof \
--vm_program ~/.aligned/test_files/sp1_fibonacci-elf \
--aligned_verification_data_path ~/aligned_verification_data \
--conn wss://batcher.alignedlayer.com
```

### Zincir Üzerindeki Kanıtı Doğrulayın

```bash
aligned verify-proof-onchain \
--aligned-verification-data ~/aligned_verification_data/*.json \
--rpc https://ethereum-holesky-rpc.publicnode.com \
--chain holesky
```

### Sonuç :

Your proof was verified in Aligned and included in the batch!





