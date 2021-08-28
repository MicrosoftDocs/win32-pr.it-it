---
description: Usato per identificare gli algoritmi di crittografia standard in varie funzioni e strutture CNG, ad esempio la struttura REG \_ dell'interfaccia CRYPT. \_
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: Identificatori dell'algoritmo CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e853d7cd0d1dd34104d3cffa20f301c11e45304c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481887"
---
# <a name="cng-algorithm-identifiers"></a>Identificatori dell'algoritmo CNG

Gli identificatori seguenti vengono usati per identificare gli algoritmi di crittografia standard in varie funzioni e strutture CNG, ad esempio la [**struttura REG dell'interfaccia \_ \_ CRYPT.**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) I provider di terze parti possono avere algoritmi aggiuntivi supportati.




| Costante/valore | Descrizione | 
|----------------|-------------|
| <span id="BCRYPT_3DES_ALGORITHM"></span><span id="bcrypt_3des_algorithm"></span><dl><dt><strong>BCRYPT_3DES_ALGORITHM</strong></dt><dt>"3DES"</dt></dl> | Algoritmo di crittografia simmetrica standard per la crittografia dei dati triplo.<br /> Standard: SP800-67, SP800-38A<br /> | 
| <span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl><dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt><dt>"3DES_112"</dt></dl> | Algoritmo di crittografia simmetrica standard di crittografia dei dati a 112 bit triplo.<br /> Standard: SP800-67, SP800-38A<br /> | 
| <span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl><dt><strong>BCRYPT_AES_ALGORITHM</strong></dt><dt>"AES"</dt></dl> | Algoritmo di crittografia simmetrica standard di crittografia avanzata.<br /> Standard: FIPS 197<br /> | 
| <span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl><dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt><dt>"AES-CMAC"</dt></dl> | Algoritmo di crittografia simmetrica AES (Advanced Encryption Standard) basato su codice CMAC (Cipher Authentication Code).<br /> Standard: SP 800-38B<br /><strong>Windows 8:</strong> Inizia il supporto per questo algoritmo.<br /><br /> | 
| <span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl><dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt><dt>"AES-GMAC"</dt></dl> | Algoritmo di crittografia simmetrica GMAC (Advanced Encryption Standard) Galgle Message Authentication Code (AES).<br /> Standard: SP800-38D<br /><strong>Windows Vista:</strong> Questo algoritmo è supportato a partire da Windows Vista con SP1.<br /> | 
| <span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl><dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt><dt>L"CAPI_KDF"</dt></dl> | Algoritmo della funzione di derivazione della chiave DELL'API crypto (CAPI). Usato dalle <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>funzioni BCryptKeyDerivation</strong></a> <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>e NCryptKeyDerivation.</strong></a><br /> | 
| <span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl><dt><strong>BCRYPT_DES_ALGORITHM</strong></dt><dt>"DES"</dt></dl> | Algoritmo di crittografia simmetrica standard di crittografia dei dati.<br /> Standard: FIPS 46-3, FIPS 81<br /> | 
| <span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl><dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt><dt>"DESX"</dt></dl> | Algoritmo di crittografia simmetrica standard di Crittografia dei dati estesa.<br /> Standard: Nessuno<br /> | 
| <span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl><dt><strong>BCRYPT_DH_ALGORITHM</strong></dt><dt>"DH"</dt></dl> | Algoritmo Diffie-Hellman scambio di chiavi.<br /> Standard: PKCS #3<br /> | 
| <span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl><dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt><dt>"DSA"</dt></dl> | Algoritmo di firma digitale.<br /> Standard: FIPS 186-2<br /><strong>Windows 8:</strong> A partire Windows 8, questo algoritmo supporta FIPS 186-3. Le chiavi minori o uguali a 1024 bit sono conformi a FIPS 186-2 e le chiavi maggiori di 1024 a FIPS 186-3.<br /> | 
| <span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt><dt>"ECDH_P256"</dt></dl> | La curva ellittica dei numeri primi a 256 bit Diffie-Hellman di scambio delle chiavi.<br /> Standard: SP800-56A<br /> | 
| <span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt><dt>"ECDH_P384"</dt></dl> | La curva ellittica dei numeri primi a 384 bit Diffie-Hellman di scambio delle chiavi.<br /> Standard: SP800-56A<br /> | 
| <span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt><dt>"ECDH_P521"</dt></dl> | La curva ellittica dei numeri primi a 521 bit Diffie-Hellman di scambio delle chiavi.<br /> Standard: SP800-56A<br /> | 
| <span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt><dt>"ECDSA_P256"</dt></dl> | Algoritmo di firma digitale a curva ellittica primi a 256 bit (FIPS 186-2).<br /> Standard: FIPS 186-2, X9.62<br /> | 
| <span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt><dt>"ECDSA_P384"</dt></dl> | Algoritmo di firma digitale a curva ellittica primi a 384 bit (FIPS 186-2).<br /> Standard: FIPS 186-2, X9.62<br /> | 
| <span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt><dt>"ECDSA_P521"</dt></dl> | Algoritmo di firma digitale a curva ellittica primi a 521 bit (FIPS 186-2).<br /> Standard: FIPS 186-2, X9.62<br /> | 
| <span id="BCRYPT_MD2_ALGORITHM"></span><span id="bcrypt_md2_algorithm"></span><dl><dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt><dt>"MD2"</dt></dl> | Algoritmo hash MD2.<br /> Standard: RFC 1319<br /> | 
| <span id="BCRYPT_MD4_ALGORITHM"></span><span id="bcrypt_md4_algorithm"></span><dl><dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt><dt>"MD4"</dt></dl> | Algoritmo hash MD4.<br /> Standard: RFC 1320<br /> | 
| <span id="BCRYPT_MD5_ALGORITHM"></span><span id="bcrypt_md5_algorithm"></span><dl><dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt><dt>"MD5"</dt></dl> | Algoritmo hash MD5.<br /> Standard: RFC 1321<br /> | 
| <span id="BCRYPT_RC2_ALGORITHM"></span><span id="bcrypt_rc2_algorithm"></span><dl><dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt><dt>"RC2"</dt></dl> | Algoritmo di crittografia simmetrica a blocchi RC2.<br /> Standard: RFC 2268<br /> | 
| <span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl><dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt><dt>"RC4"</dt></dl> | Algoritmo di crittografia simmetrica RC4.<br /> Standard: Vari<br /> | 
| <span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl><dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt><dt>"RNG"</dt></dl> | Algoritmo del generatore di numeri casuali.<br /> Standard: FIPS 186-2, FIPS 140-2, NIST SP 800-90<br /><blockquote>[!Note]<br />A partire da Windows Vista con SP1 e Windows Server 2008, il generatore di numeri casuali si basa sulla modalità del contatore AES specificata nello standard NIST SP 800-90.</blockquote><br /><strong>Windows Vista:</strong> Il generatore di numeri casuali è basato sul generatore di numeri casuali basato su hash specificato nello standard FIPS 186-2.<br /><strong>Windows 8:</strong> A partire Windows 8, l'algoritmo RNG supporta FIPS 186-3. Le chiavi minori o uguali a 1024 bit sono conformi a FIPS 186-2 e le chiavi maggiori di 1024 a FIPS 186-3.<br /> | 
| <span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl><dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt><dt>"DUALECRNG"</dt></dl> | Algoritmo di generazione di numeri casuali a doppia curva ellittica. <br /> Standard: SP800-90.<br /><strong>Windows 8:</strong> A partire Windows 8, l'algoritmo EC RNG supporta FIPS 186-3. Le chiavi minori o uguali a 1024 bit sono conformi a FIPS 186-2 e le chiavi maggiori di 1024 a FIPS 186-3.<br /><strong>Windows 10:</strong> A partire da Windows 10, l'algoritmo di generazione di numeri casuali a doppia curva ellittica è stato rimosso. Gli usi esistenti di questo algoritmo continueranno a funzionare. Tuttavia, il generatore di numeri casuali si basa sulla modalità del contatore AES specificata nello standard NIST SP 800-90. Il nuovo codice deve <strong>usare BCRYPT_RNG_ALGORITHM</strong>ed è consigliabile modificare il codice esistente per usare <strong>BCRYPT_RNG_ALGORITHM</strong>. <br /> | 
| <span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl><dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt><dt>"FIPS186DSARNG"</dt></dl> | Algoritmo di generazione di numeri casuali adatto per DSA (Digital Signature Algorithm). <br /> Standard: FIPS 186-2.<br /><strong>Windows 8:</strong> Inizia il supporto per FIPS 186-3.<br /> | 
| <span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl><dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt><dt>"RSA"</dt></dl> | Algoritmo a chiave pubblica RSA. <br /> Standard: PKCS #1 v1.5 e v2.0.<br /> | 
| <span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl><dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt><dt>"RSA_SIGN"</dt></dl> | Algoritmo di firma RSA. Questo algoritmo non è attualmente supportato. È possibile usare <strong>l'algoritmo BCRYPT_RSA_ALGORITHM</strong> per eseguire operazioni di firma RSA. <br /> Standard: PKCS #1 v1.5 e v2.0.<br /> | 
| <span id="BCRYPT_SHA1_ALGORITHM"></span><span id="bcrypt_sha1_algorithm"></span><dl><dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt><dt>"SHA1"</dt></dl> | Algoritmo hash sicuro a 160 bit. <br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA256_ALGORITHM"></span><span id="bcrypt_sha256_algorithm"></span><dl><dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt><dt>"SHA256"</dt></dl> | Algoritmo hash sicuro a 256 bit.<br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA384_ALGORITHM"></span><span id="bcrypt_sha384_algorithm"></span><dl><dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt><dt>"SHA384"</dt></dl> | Algoritmo hash sicuro a 384 bit. <br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA512_ALGORITHM"></span><span id="bcrypt_sha512_algorithm"></span><dl><dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt><dt>"SHA512"</dt></dl> | Algoritmo hash sicuro a 512 bit. <br /> Standard: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl><dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt><dt>L"SP800_108_CTR_HMAC"</dt></dl> | Modalità contatore, algoritmo della funzione di derivazione della chiave HMAC (Hash-Based Message Authentication Code). Usato dalle <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>funzioni BCryptKeyDerivation</strong></a> <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>e NCryptKeyDerivation.</strong></a><br /> | 
| <span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl><dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt><dt>L"SP800_56A_CONCAT"</dt></dl> | Algoritmo di funzione di derivazione della chiave SP800-56A. Usato dalle <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>funzioni BCryptKeyDerivation</strong></a> <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>e NCryptKeyDerivation.</strong></a><br /> | 
| <span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl><dt><strong>BCRYPT_PBKDF2_ALGORITHM</strong></dt><dt>L"PBKDF2"</dt></dl> | Algoritmo di derivazione della chiave basato su password 2 (PBKDF2). Usato dalle <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>funzioni BCryptKeyDerivation</strong></a> <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>e NCryptKeyDerivation.</strong></a><br /> | 
| <span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt><dt>"ECDSA"</dt></dl> | Algoritmo di firma digitale a curva ellittica primi generici (per <strong>altre</strong> informazioni, vedere Note). <br /> Standard: ANSI X9.62.<br /> | 
| <span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt><dt>"ECDH"</dt></dl> | Curva ellittica primaria generica Diffie-Hellman algoritmo di scambio delle chiavi (per <strong>altre</strong> informazioni, vedere Osservazioni). <br /> Standard: SP800-56A.<br /> | 
| <span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl><dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt><dt>"XTS-AES"</dt></dl> | Algoritmo di crittografia simmetrica standard avanzato in modalità XTS. <br /> Standard: SP-800-38E, IEEE Std 1619-2007.<br /><strong>Windows 10:</strong> Inizia il supporto per questo algoritmo.<br /> | 




## <a name="remarks"></a>Commenti

Per usare **BCRYPT \_ ECDSA \_ ALGORITM** o **BCRYPT \_ ECDH \_ ALGORITHM,** chiamare [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) con **BCRYPT \_ ECDSA \_ ALGORITHM** o **BCRYPT \_ ECDH \_ ALGORITHM** come *pszAlgId*. Usare quindi [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) per impostare la **proprietà BCRYPT \_ ECC CURVE \_ \_ NAME** su un algoritmo denominato elencato in Curve denominate CNG.

Per provider di parametri di curva ellittica definiti dall'utente direttamente, usare [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) per impostare la **proprietà \_ BCRYPT ECC \_ PARAMETERS.** Scaricare il [Windows 10 Cryptographic Provider Developer Kit (CPDK)](https://www.microsoft.com/download/details.aspx?id=30688) per altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Bcrypt.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




