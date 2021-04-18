---
description: Specifica un identificatore di algoritmo.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319368"
---
# <a name="alg_id"></a>ALG_ID

Il tipo di dati **ALG_ID** specifica un identificatore di algoritmo. I parametri di questo tipo di dati vengono passati alla maggior parte delle funzioni in CryptoAPI.


```C++
typedef unsigned int ALG_ID;
```



Nella tabella seguente sono elencati gli identificatori degli algoritmi attualmente definiti. Gli autori di [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) personalizzati possono definire nuovi valori. Inoltre, le **ALG_ID** utilizzate da DSN personalizzati per le specifiche chiave **AT_KEYEXCHANGE** e **AT_SIGNATURE** sono dipendenti dal provider. I mapping correnti seguono la tabella.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Identificatore</th>
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CALG_3DES</td>
<td>0x00006603</td>
<td>Algoritmo di crittografia <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> .</td>
</tr>
<tr class="even">
<td>CALG_3DES_112</td>
<td>0x00006609</td>
<td>Crittografia <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> a due chiavi con lunghezza chiave effettiva uguale a 112 bit.</td>
</tr>
<tr class="odd">
<td>CALG_AES</td>
<td>0x00006611</td>
<td>Advanced Encryption Standard (AES). Questo algoritmo è supportato dal <a href="microsoft-aes-cryptographic-provider.md">provider di crittografia Microsoft AES</a>.</td>
</tr>
<tr class="even">
<td>CALG_AES_128</td>
<td>0x0000660e</td>
<td>AES a 128 bit. Questo algoritmo è supportato dal <a href="microsoft-aes-cryptographic-provider.md">provider di crittografia Microsoft AES</a>.</td>
</tr>
<tr class="odd">
<td>CALG_AES_192</td>
<td>0x0000660f</td>
<td>AES a 192 bit. Questo algoritmo è supportato dal <a href="microsoft-aes-cryptographic-provider.md">provider di crittografia Microsoft AES</a>.</td>
</tr>
<tr class="even">
<td>CALG_AES_256</td>
<td>0x00006610</td>
<td>AES a 256 bit. Questo algoritmo è supportato dal <a href="microsoft-aes-cryptographic-provider.md">provider di crittografia Microsoft AES</a>.</td>
</tr>
<tr class="odd">
<td>CALG_AGREEDKEY_ANY</td>
<td>0x0000aa03</td>
<td>Identificatore di algoritmo temporaneo per gli handle delle chiavi concordate Diffie-Hellman.</td>
</tr>
<tr class="even">
<td>CALG_CYLINK_MEK</td>
<td>0x0000660c</td>
<td>Algoritmo per la creazione di una chiave DES a 40 bit con bit di parità e bit di chiave zero per ottenere la lunghezza della chiave 64 bit. Questo algoritmo è supportato dal <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_DES</td>
<td>0x00006601</td>
<td>Algoritmo di crittografia DES.</td>
</tr>
<tr class="even">
<td>CALG_DESX</td>
<td>0x00006604</td>
<td>Algoritmo di crittografia DESX.</td>
</tr>
<tr class="odd">
<td>CALG_DH_EPHEM</td>
<td>0x0000aa02</td>
<td>Diffie-Hellman algoritmo di scambio di chiave temporaneo.</td>
</tr>
<tr class="even">
<td>CALG_DH_SF</td>
<td>0x0000aa01</td>
<td>Diffie-Hellman archiviare e inviare l'algoritmo di scambio di chiave.</td>
</tr>
<tr class="odd">
<td>CALG_DSS_SIGN</td>
<td>0x00002200</td>
<td>Algoritmo di firma della <a href="/windows/desktop/SecGloss/p-gly"><em>chiave pubblica</em></a> DSA.</td>
</tr>
<tr class="even">
<td>CALG_ECDH</td>
<td>0x0000aa05</td>
<td>Curva ellittica Diffie-Hellman algoritmo di scambio delle chiavi.
<blockquote>
[!Note]<br />
Questo algoritmo è supportato solo tramite l' <a href="/windows/desktop/SecCNG/cng-portal">API di crittografia: Next Generation</a>.
</blockquote>
<br/> <strong>Windows Server 2003 e Windows XP:</strong> Questo algoritmo non è supportato.<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECDH_EPHEM</td>
<td>0x0000ae06</td>
<td>Curva ellittica temporanea Diffie-Hellman algoritmo di scambio delle chiavi.
<blockquote>
[!Note]<br />
Questo algoritmo è supportato solo tramite l' <a href="/windows/desktop/SecCNG/cng-portal">API di crittografia: Next Generation</a>.
</blockquote>
<br/> <strong>Windows Server 2003 e Windows XP:</strong> Questo algoritmo non è supportato.<br/></td>
</tr>
<tr class="even">
<td>CALG_ECDSA</td>
<td>0x00002203</td>
<td>Algoritmo di firma digitale a curva ellittica.
<blockquote>
[!Note]<br />
Questo algoritmo è supportato solo tramite l' <a href="/windows/desktop/SecCNG/cng-portal">API di crittografia: Next Generation</a>.
</blockquote>
<br/> <strong>Windows Server 2003 e Windows XP:</strong> Questo algoritmo non è supportato.<br/></td>
</tr>
<tr class="odd">
<td>CALG_ECMQV</td>
<td>0x0000a001</td>
<td>Algoritmo di scambio delle chiavi Menezes, qu e Vanstone (MQV) a curva ellittica. Questo algoritmo non è supportato.</td>
</tr>
<tr class="even">
<td>CALG_HASH_REPLACE_OWF</td>
<td>0x0000800b</td>
<td>Algoritmo di hashing della funzione unidirezionale.</td>
</tr>
<tr class="odd">
<td>CALG_HUGHES_MD5</td>
<td>0x0000a003</td>
<td>Algoritmo di hash MD5 Hughes.</td>
</tr>
<tr class="even">
<td>CALG_HMAC</td>
<td>0x00008009</td>
<td>Algoritmo hash con chiave HMAC. Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_KEA_KEYX</td>
<td>0x0000aa04</td>
<td>Algoritmo di scambio delle chiavi di KEA (FORTEZZA). Questo algoritmo non è supportato.</td>
</tr>
<tr class="even">
<td>CALG_MAC</td>
<td>0x00008005</td>
<td>Algoritmo hash con chiave <a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> . Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_MD2</td>
<td>0x00008001</td>
<td>Algoritmo di hash MD2. Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_MD4</td>
<td>0x00008002</td>
<td>Algoritmo di hash MD4.</td>
</tr>
<tr class="odd">
<td>CALG_MD5</td>
<td>0x00008003</td>
<td>Algoritmo di hash MD5. Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_NO_SIGN</td>
<td>0x00002000</td>
<td>Nessun algoritmo di firma.</td>
</tr>
<tr class="odd">
<td>CALG_OID_INFO_CNG_ONLY</td>
<td>0xFFFFFFFF</td>
<td>L'algoritmo viene implementato solo in CNG. La macro, IS_SPECIAL_OID_INFO_ALGID, può essere utilizzata per determinare se un algoritmo di crittografia è supportato solo tramite le funzioni CNG.</td>
</tr>
<tr class="even">
<td>CALG_OID_INFO_PARAMETERS</td>
<td>0xfffffffe</td>
<td>L'algoritmo viene definito nei parametri codificati. L'algoritmo è supportato solo mediante CNG. La macro, IS_SPECIAL_OID_INFO_ALGID, può essere utilizzata per determinare se un algoritmo di crittografia è supportato solo tramite le funzioni CNG.</td>
</tr>
<tr class="odd">
<td>CALG_PCT1_MASTER</td>
<td>0x00004c04</td>
<td>Utilizzato dal sistema operativo Schannel.dll. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</td>
</tr>
<tr class="even">
<td>CALG_RC2</td>
<td>0x00006602</td>
<td>Algoritmo di crittografia a blocchi RC2. Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_RC4</td>
<td>0x00006801</td>
<td>Algoritmo di crittografia del flusso RC4. Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_RC5</td>
<td>0x0000660d</td>
<td>Algoritmo di crittografia a blocchi RC5.</td>
</tr>
<tr class="odd">
<td>CALG_RSA_KEYX</td>
<td>0x0000a400</td>
<td>Algoritmo di scambio di chiave pubblica RSA. Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_RSA_SIGN</td>
<td>0x00002400</td>
<td>Algoritmo di firma della chiave pubblica RSA. Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_ENC_KEY</td>
<td>0x00004c07</td>
<td>Utilizzato dal sistema operativo Schannel.dll. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</td>
</tr>
<tr class="even">
<td>CALG_SCHANNEL_MAC_KEY</td>
<td>0x00004c03</td>
<td>Utilizzato dal sistema operativo Schannel.dll. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</td>
</tr>
<tr class="odd">
<td>CALG_SCHANNEL_MASTER_HASH</td>
<td>0x00004c02</td>
<td>Utilizzato dal sistema operativo Schannel.dll. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</td>
</tr>
<tr class="even">
<td>CALG_SEAL</td>
<td>0x00006802</td>
<td>Algoritmo di crittografia SEAL. Questo algoritmo non è supportato.</td>
</tr>
<tr class="odd">
<td>CALG_SHA</td>
<td>0x00008004</td>
<td>Algoritmo di hash SHA. Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</td>
</tr>
<tr class="even">
<td>CALG_SHA1</td>
<td>0x00008004</td>
<td>Uguale a <strong>CALG_SHA</strong>. Questo algoritmo è supportato dal <a href="microsoft-base-cryptographic-provider.md">provider di crittografia di base Microsoft</a>.</td>
</tr>
<tr class="odd">
<td>CALG_SHA_256</td>
<td>0x0000800c</td>
<td>algoritmo di hash SHA a 256 bit. Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider. <strong>Windows XP con SP3:</strong> Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider (prototipo).<br/> <strong>Windows XP con SP2, Windows XP con SP1 e Windows XP:</strong> Questo algoritmo non è supportato.<br/></td>
</tr>
<tr class="even">
<td>CALG_SHA_384</td>
<td>0x0000800d</td>
<td>algoritmo di hash SHA a 384 bit. Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider. <strong>Windows XP con SP3:</strong> Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider (prototipo).<br/> <strong>Windows XP con SP2, Windows XP con SP1 e Windows XP:</strong> Questo algoritmo non è supportato.<br/></td>
</tr>
<tr class="odd">
<td>CALG_SHA_512</td>
<td>0x0000800e</td>
<td>algoritmo di hash SHA a 512 bit. Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider. <strong>Windows XP con SP3:</strong> Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider (prototipo).<br/> <strong>Windows XP con SP2, Windows XP con SP1 e Windows XP:</strong> Questo algoritmo non è supportato.<br/></td>
</tr>
<tr class="even">
<td>CALG_SKIPJACK</td>
<td>0x0000660a</td>
<td>Skipjack Block Encryption Algorithm (FORTEZZA). Questo algoritmo non è supportato.</td>
</tr>
<tr class="odd">
<td>CALG_SSL2_MASTER</td>
<td>0x00004c05</td>
<td>Utilizzato dal sistema operativo Schannel.dll. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</td>
</tr>
<tr class="even">
<td>CALG_SSL3_MASTER</td>
<td>0x00004c01</td>
<td>Utilizzato dal sistema operativo Schannel.dll. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</td>
</tr>
<tr class="odd">
<td>CALG_SSL3_SHAMD5</td>
<td>0x00008008</td>
<td>Utilizzato dal sistema operativo Schannel.dll. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</td>
</tr>
<tr class="even">
<td>CALG_TEK</td>
<td>0x0000660b</td>
<td>TEK (FORTEZZA). Questo algoritmo non è supportato.</td>
</tr>
<tr class="odd">
<td>CALG_TLS1_MASTER</td>
<td>0x00004c06</td>
<td>Utilizzato dal sistema operativo Schannel.dll. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</td>
</tr>
<tr class="even">
<td>CALG_TLS1PRF</td>
<td>0x0000800a</td>
<td>Utilizzato dal sistema operativo Schannel.dll. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni.</td>
</tr>
</tbody>
</table>



 

Per [Microsoft Base Cryptographic](microsoft-base-cryptographic-provider.md)provider, [Microsoft Strong Cryptographic](microsoft-strong-cryptographic-provider.md)provider e [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md), le **ALG_IDs** utilizzate per le specifiche principali **AT_KEYEXCHANGE** e **AT_SIGNATURE** sono le seguenti:

-   **CALG_RSA_KEYX** viene utilizzato per **AT_KEYEXCHANGE**.
-   **CALG_RSA_SIGN** viene utilizzato per **AT_SIGNATURE**.

Per [Microsoft Base DSS e Diffie-Hellman provider di crittografia](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), i **ALG_IDs** usati per le specifiche principali **AT_KEYEXCHANGE** e **AT_SIGNATURE** sono i seguenti:

-   **CALG_DH_SF** viene utilizzato per **AT_KEYEXCHANGE**.
-   **CALG_DSS_SIGN** viene utilizzato per **AT_SIGNATURE**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di crittografia](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
