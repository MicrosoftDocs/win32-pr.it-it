---
description: Usato per identificare gli algoritmi di crittografia standard in varie funzioni e strutture CNG, ad esempio la struttura CRYPT \_ INTERFACE \_ REG.
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: Identificatori dell'algoritmo CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1f2f9539f9fc446d0c313d32117890bc3b1eff4ed8261a815e41acdda13cbe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908917"
---
# <a name="cng-algorithm-identifiers"></a>Identificatori di algoritmi CNG

Gli identificatori seguenti vengono usati per identificare gli algoritmi di crittografia standard in varie strutture e funzioni CNG, ad esempio la [**struttura CRYPT \_ INTERFACE \_ REG.**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) I provider di terze parti possono avere algoritmi aggiuntivi supportati.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante/valore</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_3DES_ALGORITHM"></span><span id="bcrypt_3des_algorithm"></span><dl> <dt><strong>BCRYPT_3DES_ALGORITHM</strong></dt> <dt> &quot; 3DES &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica standard di crittografia dei dati triplo.<br/> Standard: SP800-67, SP800-38A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl> <dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt> <dt> &quot; 3DES_112 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica standard di crittografia dei dati a 112 bit.<br/> Standard: SP800-67, SP800-38A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl> <dt><strong>BCRYPT_AES_ALGORITHM</strong></dt> <dt> &quot; AES &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica standard di crittografia avanzata.<br/> Standard: FIPS 197<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt> <dt> &quot; AES-CMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica AES (Cipher Based Message Authentication Code) avanzato.<br/> Standard: SP 800-38B<br/> <strong>Windows 8:</strong> Inizia il supporto per questo algoritmo.<br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt> <dt> &quot; AES-GMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica GMAC (Advanced Encryption Standard) Galois Message Authentication Code (GMAC).<br/> Standard: SP800-38D<br/> <strong>Windows Vista:</strong> Questo algoritmo è supportato a partire da Windows Vista con SP1.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl> <dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt> <dt>L &quot; &quot; CAPI_KDF</dt> </dl></td>
<td style="text-align: left;">Algoritmo di funzione di derivazione della chiave API crypto (CAPI). Usato dalle <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>funzioni BCryptKeyDerivation</strong></a> <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>e NCryptKeyDerivation.</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl> <dt><strong>BCRYPT_DES_ALGORITHM</strong></dt> <dt> &quot; DES &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica standard di crittografia dei dati.<br/> Standard: FIPS 46-3, FIPS 81<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl> <dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt> <dt> &quot; DESX &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica standard della crittografia dei dati estesa.<br/> Standard: Nessuno<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl> <dt><strong>BCRYPT_DH_ALGORITHM</strong></dt> <dt> &quot; DH &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo Diffie-Hellman scambio di chiavi.<br/> Standard: PKCS #3<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt> <dt> &quot; DSA &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di firma digitale.<br/> Standard: FIPS 186-2<br/> <strong>Windows 8:</strong> A partire Windows 8, questo algoritmo supporta FIPS 186-3. Le chiavi minori o uguali a 1024 bit sono conformi a FIPS 186-2 e le chiavi maggiori di 1024 a FIPS 186-3.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt> <dt> &quot; ECDH_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">La curva ellittica primaria a 256 bit Diffie-Hellman di scambio delle chiavi.<br/> Standard: SP800-56A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt> <dt> &quot; &quot; ECDH_P384</dt> </dl></td>
<td style="text-align: left;">La curva ellittica primaria a 384 bit Diffie-Hellman algoritmo di scambio delle chiavi.<br/> Standard: SP800-56A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt> <dt> &quot; &quot; ECDH_P521</dt> </dl></td>
<td style="text-align: left;">La curva ellittica primaria a 521 bit Diffie-Hellman algoritmo di scambio delle chiavi.<br/> Standard: SP800-56A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di firma digitale a curva ellittica primi a 256 bit (FIPS 186-2).<br/> Standard: FIPS 186-2, X9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt> <dt> &quot; &quot; ECDSA_P384</dt> </dl></td>
<td style="text-align: left;">Algoritmo di firma digitale a curva ellittica primi a 384 bit (FIPS 186-2).<br/> Standard: FIPS 186-2, X9.62<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di firma digitale a curva ellittica primi a 521 bit (FIPS 186-2).<br/> Standard: FIPS 186-2, X9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD2_ALGORITHM"></span><span id="bcrypt_md2_algorithm"></span><dl> <dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt> <dt> &quot; MD2 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo hash MD2.<br/> Standard: RFC 1319<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_MD4_ALGORITHM"></span><span id="bcrypt_md4_algorithm"></span><dl> <dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt> <dt> &quot; MD4 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo hash MD4.<br/> Standard: RFC 1320<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_MD5_ALGORITHM"></span><span id="bcrypt_md5_algorithm"></span><dl> <dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt> <dt> &quot; MD5 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo hash MD5.<br/> Standard: RFC 1321<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RC2_ALGORITHM"></span><span id="bcrypt_rc2_algorithm"></span><dl> <dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt> <dt> &quot; RC2 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica a blocchi RC2.<br/> Standard: RFC 2268<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl> <dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt> <dt> &quot; RC4 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica RC4.<br/> Standard: Vari<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt> <dt> &quot; RNG &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo del generatore di numeri casuali.<br/> Standard: FIPS 186-2, FIPS 140-2, NIST SP 800-90<br/>
<blockquote>
[!Note]<br />
A partire da Windows Vista con SP1 e Windows Server 2008, il generatore di numeri casuali è basato sulla modalità contatore AES specificata nello standard NIST SP 800-90.
</blockquote>
<br/> <strong>Windows Vista:</strong> Il generatore di numeri casuali si basa sul generatore di numeri casuali basato su hash specificato nello standard FIPS 186-2.<br/> <strong>Windows 8:</strong> A partire Windows 8, l'algoritmo RNG supporta FIPS 186-3. Le chiavi minori o uguali a 1024 bit sono conformi a FIPS 186-2 e le chiavi maggiori di 1024 a FIPS 186-3.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt> <dt> &quot; DUALECRNG &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo del generatore di numeri casuali a doppia curva ellittica. <br/> Standard: SP800-90.<br/> <strong>Windows 8:</strong> A partire Windows 8, l'algoritmo EC RNG supporta FIPS 186-3. Le chiavi minori o uguali a 1024 bit sono conformi a FIPS 186-2 e le chiavi maggiori di 1024 a FIPS 186-3.<br/> <strong>Windows 10:</strong> A partire da Windows 10, l'algoritmo del generatore di numeri casuali a doppia curva ellittica è stato rimosso. Gli usi esistenti di questo algoritmo continueranno a funzionare. Tuttavia, il generatore di numeri casuali si basa sulla modalità contatore AES specificata nello standard NIST SP 800-90. Il nuovo codice deve <strong>BCRYPT_RNG_ALGORITHM</strong>, ed è consigliabile modificare il codice esistente per usare <strong>BCRYPT_RNG_ALGORITHM</strong>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt> <dt> &quot; FIPS186DSARNG &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo del generatore di numeri casuali adatto per DSA (Digital Signature Algorithm). <br/> Standard: FIPS 186-2.<br/> <strong>Windows 8:</strong> Inizia il supporto per FIPS 186-3.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt> <dt> &quot; RSA &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo a chiave pubblica RSA. <br/> Standard: PKCS #1 v1.5 e v2.0.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt> <dt> &quot; RSA_SIGN &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di firma RSA. Questo algoritmo non è attualmente supportato. È possibile usare <strong>l'algoritmo BCRYPT_RSA_ALGORITHM</strong> per eseguire operazioni di firma RSA. <br/> Standard: PKCS #1 v1.5 e v2.0.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA1_ALGORITHM"></span><span id="bcrypt_sha1_algorithm"></span><dl> <dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt> <dt> &quot; SHA1 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo hash sicuro a 160 bit. <br/> Standard: FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA256_ALGORITHM"></span><span id="bcrypt_sha256_algorithm"></span><dl> <dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt> <dt> &quot; SHA256 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo hash sicuro a 256 bit.<br/> Standard: FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SHA384_ALGORITHM"></span><span id="bcrypt_sha384_algorithm"></span><dl> <dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt> <dt> &quot; SHA384 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo hash sicuro a 384 bit. <br/> Standard: FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SHA512_ALGORITHM"></span><span id="bcrypt_sha512_algorithm"></span><dl> <dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt> <dt> &quot; SHA512 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo hash sicuro a 512 bit. <br/> Standard: FIPS 180-2, FIPS 198.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl> <dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt> <dt>L SP800_108_CTR_HMAC &quot; &quot; </dt> </dl></td>
<td style="text-align: left;">Modalità contatore, algoritmo della funzione di derivazione della chiave HMAC (Hash-Based Message Authentication Code). Usato dalle <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>funzioni BCryptKeyDerivation</strong></a> <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>e NCryptKeyDerivation.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl> <dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt> <dt>L &quot; SP800_56A_CONCAT &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo della funzione di derivazione della chiave SP800-56A. Usato dalle <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>funzioni BCryptKeyDerivation</strong></a> <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>e NCryptKeyDerivation.</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl> <dt> <strong>BCRYPT_PBKDF2_ALGORITHM</strong> </dt> <dt>L &quot; PBKDF2 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo PBKDF2 (Password-Based Key Derivation Function 2). Usato dalle <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>funzioni BCryptKeyDerivation</strong></a> <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>e NCryptKeyDerivation.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt> <dt> &quot; ECDSA &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di firma digitale a curva ellittica prime generico (per <strong>altre informazioni, vedere</strong> la sezione Osservazioni). <br/> Standard: ANSI X9.62.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt> <dt> &quot; ECDH &quot; </dt> </dl></td>
<td style="text-align: left;">Curva ellittica generica Diffie-Hellman algoritmo di scambio delle chiavi (vedere <strong>la sezione</strong> Osservazioni per altre informazioni). <br/> Standard: SP800-56A.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl> <dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt> <dt> &quot; XTS-AES &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica standard di crittografia avanzata in modalità XTS. <br/> Standard: SP-800-38E, IEEE Std 1619-2007.<br/> <strong>Windows 10:</strong> Inizia il supporto per questo algoritmo.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Per usare **BCRYPT \_ ECDSA \_ ALGORITM** o **BCRYPT \_ ECDH \_ ALGORITHM,** chiamare [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) con **BCRYPT \_ ECDSA \_ ALGORITHM** o **BCRYPT \_ ECDH \_ ALGORITHM** come *pszAlgId*. Usare quindi [**BCryptSetProperty per**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) impostare la **proprietà BCRYPT ECC CURVE \_ \_ \_ NAME** su un algoritmo denominato elencato in Curve denominate CNG.

Per provider di parametri a curva ellittica definiti dall'utente direttamente, usare [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) per impostare la **proprietà \_ BCRYPT ECC \_ PARAMETERS.** Scaricare il [Windows 10 Cryptographic Provider Developer Kit (CPDK)](https://www.microsoft.com/download/details.aspx?id=30688) per altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Bcrypt.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




