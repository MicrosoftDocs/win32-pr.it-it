---
description: Utilizzato per identificare gli algoritmi di crittografia standard in varie funzioni e strutture CNG, ad esempio la \_ struttura del reg dell'interfaccia Crypt \_ .
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: Identificatori dell'algoritmo CNG (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba244f2a815933322793fdd572ed7a4e69256a0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305613"
---
# <a name="cng-algorithm-identifiers"></a>Identificatori dell'algoritmo CNG

Gli identificatori seguenti vengono usati per identificare gli algoritmi di crittografia standard in varie funzioni e strutture CNG, ad esempio la struttura del [**\_ \_ registro dell'interfaccia Crypt**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) . I provider di terze parti possono avere algoritmi aggiuntivi supportati.



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
<td style="text-align: left;"><span id="BCRYPT_3DES_ALGORITHM"></span><span id="bcrypt_3des_algorithm"></span><dl> <dt><strong></strong></dt> <dt> &quot; 3DES &quot; </dt> BCRYPT_3DES_ALGORITHM </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica Triple Data Encryption Standard.<br/> Standard: SP800-67, SP800-38A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl> <dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt> <dt> &quot; 3DES_112 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica standard a 112 bit di crittografia dei dati.<br/> Standard: SP800-67, SP800-38A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl> <dt><strong>BCRYPT_AES_ALGORITHM</strong></dt> <dt> &quot; AES &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica Advanced Encryption Standard.<br/> Standard: FIPS 197<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt> <dt> &quot; AES-CMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica CMAC (Advanced Encryption Standard) basato su crittografia AES.<br/> Standard: SP 800-38B<br/> <strong>Windows 8:</strong> Inizio del supporto per questo algoritmo.<br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl> <dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt> <dt> &quot; AES-GMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica AES (Advanced Encryption Standard) per il codice di autenticazione GMAC (AES).<br/> Standard: SP800-38D<br/> <strong>Windows Vista:</strong> Questo algoritmo è supportato a partire da Windows Vista con SP1.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl> <dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt> <dt>L &quot; CAPI_KDF &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo della funzione di derivazione della chiave dell'API Crypto (CAPI). Utilizzato dalle funzioni <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> e <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl> <dt><strong>BCRYPT_DES_ALGORITHM</strong></dt> <dt> &quot; des &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica standard di crittografia dei dati.<br/> Standard: FIPS 46-3, FIPS 81<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl> <dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt> <dt> &quot; DESX &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica standard di crittografia dei dati esteso.<br/> Standard: nessuna<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl> <dt><strong>BCRYPT_DH_ALGORITHM</strong></dt> <dt> &quot; DH &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di scambio delle chiavi Diffie-Hellman.<br/> Standard: PKCS #3<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl> <dt><strong></strong></dt> <dt> &quot; DSA &quot; </dt> BCRYPT_DSA_ALGORITHM </dl></td>
<td style="text-align: left;">Algoritmo di firma digitale.<br/> Standard: FIPS 186-2<br/> <strong>Windows 8:</strong> A partire da Windows 8, questo algoritmo supporta FIPS 186-3. Le chiavi minori o uguali a 1024 bit sono conformi a FIPS 186-2 e alle chiavi maggiori di 1024 a FIPS 186-3.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt> <dt> &quot; ECDH_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">Curva ellittica principale a 256 bit Diffie-Hellman algoritmo di scambio delle chiavi.<br/> Standard: SP800-56A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt> <dt> &quot; ECDH_P384 &quot; </dt> </dl></td>
<td style="text-align: left;">Curva ellittica principale a 384 bit Diffie-Hellman algoritmo di scambio delle chiavi.<br/> Standard: SP800-56A<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt> <dt> &quot; ECDH_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">Curva ellittica principale a 521 bit Diffie-Hellman algoritmo di scambio delle chiavi.<br/> Standard: SP800-56A<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P256 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di firma digitale per le prime ellittiche a 256 bit (FIPS 186-2).<br/> Standard: FIPS 186-2, X 9.62<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P384 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di firma digitale per le prime ellittiche a 384 bit (FIPS 186-2).<br/> Standard: FIPS 186-2, X 9.62<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt> <dt> &quot; ECDSA_P521 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di firma digitale per le prime ellittiche a 521 bit (FIPS 186-2).<br/> Standard: FIPS 186-2, X 9.62<br/></td>
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
<td style="text-align: left;">Algoritmo di crittografia simmetrica in blocchi RC2.<br/> Standard: RFC 2268<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl> <dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt> <dt> &quot; RC4 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica RC4.<br/> Standard: varie<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt> <dt> &quot; RNG &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo generatore di numeri casuali.<br/> Standard: FIPS 186-2, FIPS 140-2, NIST SP 800-90<br/>
<blockquote>
[!Note]<br />
A partire da Windows Vista con SP1 e Windows Server 2008, il generatore di numeri casuali è basato sulla modalità del contatore AES specificata nello standard NIST SP 800-90.
</blockquote>
<br/> <strong>Windows Vista:</strong> Il generatore di numeri casuali è basato sul generatore di numeri casuali basato su hash specificato nello standard FIPS 186-2.<br/> <strong>Windows 8:</strong> A partire da Windows 8, l'algoritmo RNG supporta FIPS 186-3. Le chiavi minori o uguali a 1024 bit sono conformi a FIPS 186-2 e alle chiavi maggiori di 1024 a FIPS 186-3.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt> <dt> &quot; DUALECRNG &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di generazione di numeri casuali a curva doppia ellittica. <br/> Standard: SP800-90.<br/> <strong>Windows 8:</strong> A partire da Windows 8, l'algoritmo EC RNG supporta FIPS 186-3. Le chiavi minori o uguali a 1024 bit sono conformi a FIPS 186-2 e alle chiavi maggiori di 1024 a FIPS 186-3.<br/> <strong>Windows 10:</strong> A partire da Windows 10, l'algoritmo di generazione di numeri casuali a curva doppia ellittica è stato rimosso. Gli utilizzi esistenti di questo algoritmo continueranno a funzionare. Tuttavia, il generatore di numeri casuali è basato sulla modalità del contatore AES specificata nello standard NIST SP 800-90. Il nuovo codice deve usare <strong>BCRYPT_RNG_ALGORITHM</strong>ed è consigliabile modificare il codice esistente per usare <strong>BCRYPT_RNG_ALGORITHM</strong>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl> <dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt> <dt> &quot; FIPS186DSARNG &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo generatore di numeri casuali adatto per DSA (Digital Signature Algorithm). <br/> Standard: FIPS 186-2.<br/> <strong>Windows 8:</strong> Viene avviato il supporto per FIPS 186-3.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl> <dt><strong></strong></dt> <dt> &quot; RSA &quot; </dt> BCRYPT_RSA_ALGORITHM </dl></td>
<td style="text-align: left;">Algoritmo di chiave pubblica RSA. <br/> Standard: PKCS #1 v 1.5 e v 2.0.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl> <dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt> <dt> &quot; RSA_SIGN &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di firma RSA. Questo algoritmo non è attualmente supportato. È possibile utilizzare l'algoritmo <strong>BCRYPT_RSA_ALGORITHM</strong> per eseguire operazioni di firma RSA. <br/> Standard: PKCS #1 v 1.5 e v 2.0.<br/></td>
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
<td style="text-align: left;"><span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl> <dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt> <dt>L &quot; SP800_108_CTR_HMAC &quot; </dt> </dl></td>
<td style="text-align: left;">Modalità contatore, algoritmo della funzione di derivazione della chiave HMAC (hash-based Message Authentication Code). Utilizzato dalle funzioni <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> e <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl> <dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt> <dt>L &quot; SP800_56A_CONCAT &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo della funzione di derivazione della chiave SP800-56A. Utilizzato dalle funzioni <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> e <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl> <dt> <strong>BCRYPT_PBKDF2_ALGORITHM</strong> </dt> <dt>L &quot; PBKDF2 &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo PBKDF2 (Key Derivation Function 2) basato su password. Utilizzato dalle funzioni <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>BCryptKeyDerivation</strong></a> e <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl> <dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt> <dt> &quot; ECDSA &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di firma digitale prime ellittiche generico (per ulteriori informazioni, vedere la <strong>sezione Osservazioni</strong> ). <br/> Standard: ANSI X 9.62.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl> <dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt> <dt> &quot; ECDH &quot; </dt> </dl></td>
<td style="text-align: left;">Curva ellittica principale generica Diffie-Hellman algoritmo di scambio delle chiavi. per ulteriori informazioni, vedere la <strong>sezione Osservazioni</strong> . <br/> Standard: SP800-56A.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl> <dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt> <dt> &quot; XTS-AES &quot; </dt> </dl></td>
<td style="text-align: left;">Algoritmo di crittografia simmetrica Advanced Encryption Standard in modalità XTS. <br/> Standard: SP-800-38E, IEEE STD 1619-2007.<br/> <strong>Windows 10:</strong> Inizio del supporto per questo algoritmo.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Per usare l'algoritmo **BCRYPT \_ ECDSA \_ algoritmo** o **BCRYPT \_ \_ ECDH**, chiamare [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) con **l'algoritmo BCRYPT ECDSA o BCRYPT \_ \_** ECDH come *pszAlgId*. **\_ \_** Usare quindi [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) per impostare la proprietà **BCRYPT \_ ecc \_ curve \_ Name** su un algoritmo denominato elencato nelle curve denominate di CNG.

Per impostare direttamente i parametri della curva ellittica definiti dall'utente, usare [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) per impostare la proprietà **BCRYPT \_ ecc \_ Parameters** . Scaricare [Windows 10 Cryptographic Provider Developer Kit (CPDK)](https://www.microsoft.com/download/details.aspx?id=30688) per ulteriori informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Bcrypt. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




