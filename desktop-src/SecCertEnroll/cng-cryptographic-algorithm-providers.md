---
description: "A differenza dell'API Cryptography (CryptoAPI), Cryptography API: Next Generation (CNG) separa i provider di crittografia dai provider di archiviazione chiavi."
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: Provider di algoritmi di crittografia CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc64926236157e581ce6406d95681bd8d4add14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315410"
---
# <a name="cng-cryptographic-algorithm-providers"></a>Provider di algoritmi di crittografia CNG

A differenza dell'API Cryptography (CryptoAPI), Cryptography API: Next Generation (CNG) separa i provider di crittografia dai provider di archiviazione chiavi. Le operazioni di base sugli algoritmi di crittografia, ad esempio l'hashing e la firma, sono denominate operazioni primitive o semplici primitive. CNG include un provider che implementa gli algoritmi seguenti.

-   [Algoritmi simmetrici](#symmetric-algorithms)
-   [Algoritmi asimmetrici](#asymmetric-algorithms)
-   [Algoritmi di hashing](#hashing-algorithms)
-   [Algoritmi di scambio di chiave](#key-exchange-algorithms)
-   [Argomenti correlati](#related-topics)

## <a name="symmetric-algorithms"></a>Algoritmi simmetrici



| Nome                                   | Modalità supportate                                                                                                                                                                                                 | Dimensione della chiave in bit (predefinita/min/max) |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| Advanced Encryption Standard (AES)     | BCE, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, wrapping della chiave AES, XTS<br/> **Windows 8:** Viene avviato il supporto per le modalità CFB128 e CMAC.<br/> **Windows 10:** Viene avviato il supporto per la modalità XTS-AES.<br/> | 128/192/256                        |
| Data Encryption Standard (DES)         | BCE, CBC, CFB8, CFB64<br/> **Windows 8:** Viene avviato il supporto per la modalità CFB64.<br/>                                                                                                                   | 56/56/56                           |
| Data Encryption Standard XORed (DESX)   | BCE, CBC, CFB8, CFB64 <br/> **Windows 8:** Viene avviato il supporto per la modalità CFB64.<br/>                                                                                                                  | 192/192/192                        |
| 3DES (Triple Data Encryption Standard) | BCE, CBC, CFB8, CFB64 <br/> **Windows 8:** Viene avviato il supporto per la modalità CFB64.<br/>                                                                                                                  | 112/168                            |
| RSA Data Security 2 (RC2)              | Sono supportate le modalità BCE, CBC, CFB8 e CFB64.<br/> **Windows 8:** Viene avviato il supporto per la modalità CFB64.<br/>                                                                                              | da 16 a 128 in incrementi di 8 bit      |
| RSA Data Security 4 (RC4)              |                                                                                                                                                                                                                 | da 8 a 512, in incrementi a 8 bit      |



 

## <a name="asymmetric-algorithms"></a>Algoritmi asimmetrici



| Nome                              | Note                                                                                                                                                                             | Dimensione della chiave in bit (predefinita/min/max)                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Algoritmo di firma digitale (DSA) | L'implementazione è conforme a FIPS 186-3 per le dimensioni delle chiavi comprese tra 1024 e 3072 bit. <br/> L'implementazione è conforme a FIPS 186-2 per le dimensioni delle chiavi da 512 a 1024 bit.<br/> | da 512 a 3072, in incrementi di 64 bit<br/> **Windows 8:** Viene avviato il supporto per la chiave a 3072 bit.<br/> |
| RSA                               | Include algoritmi RSA che usano la codifica o la spaziatura interna PKCS1, Optimal Encryption Encryption Padding (OAEP) o la spaziatura in testo non crittografato (PSS Signature Scheme)               | da 512 a 16384, in incrementi di 64 bit                                                                            |



 

## <a name="hashing-algorithms"></a>Algoritmi di hashing



| Nome                               | Note               | Dimensione della chiave in bit (predefinita/min/max) |
|------------------------------------|---------------------|------------------------------------|
| Secure Hash Algorithm 1 (SHA1)     | Include HmacSha1   | 160/160/160                        |
| Algoritmo Secure Hash Algorithm 256 (SHA256) | Include HmacSha256 | 256/256/256                        |
| Algoritmo Secure Hash Algorithm 384 (SHA384) | Include HmacSha384 | 384/384/384                        |
| Algoritmo Secure Hash Algorithm 512 (SHA512) | Include HmacSha512 | 512/512/512                        |
| Messaggio digest 2 (MD2)             | Include HmacMd2    | 128/128/128                        |
| Digest del messaggio 4 (MD4)             | Include HmacMd4    | 128/128/128                        |
| Digest del messaggio 5 (MD5)             | Include HmacMd5    | 128/128/128                        |



 

## <a name="key-exchange-algorithms"></a>Algoritmi di scambio di chiave



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome algoritmo</th>
<th>Note</th>
<th>Dimensione della chiave in bit (predefinita/min/max)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Algoritmo di scambio delle chiavi Diffie-Hellman</td>

<td>da 512 a 4096, in incrementi di 64 bit</td>
</tr>
<tr class="even">
<td>Diffie-Hellman a curva ellittica (ECDH)</td>
<td>Include le curve che usano le chiavi pubbliche 256, 384 e 521 bit, come specificato in SP800-56A.</td>
<td>256/384/521</td>
</tr>
<tr class="odd">
<td>Algoritmo di firma digitale a curva ellittica (ECDSA)</td>
<td>Include le curve che usano le chiavi pubbliche 256, 384 e 521 bit, come specificato in FIPS 186-3.
<blockquote>
[!Note]<br />
Per visualizzare tutte le curve ellittiche denominate, utilizzare <strong>certutil displayEccCurve</strong>.
</blockquote>
<br/></td>
<td>256/384/521</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Identificatori dell'algoritmo CNG**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Funzioni primitive di crittografia CNG](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[Informazioni sui provider di crittografia](understanding-cryptographic-providers.md)
</dt> </dl>

 

