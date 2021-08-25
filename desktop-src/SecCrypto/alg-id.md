---
description: Specifica un identificatore di algoritmo.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82f4b6c476a8ea6e61785a096abf33c357d9b024
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482397"
---
# <a name="alg_id"></a>ALG_ID

Il **tipo ALG_ID** dati specifica un identificatore di algoritmo. I parametri di questo tipo di dati vengono passati alla maggior parte delle funzioni in CryptoAPI.


```C++
typedef unsigned int ALG_ID;
```



Nella tabella seguente sono elencati gli identificatori di algoritmo attualmente definiti. Gli autori di [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) personalizzati possono definire nuovi valori. Inoltre, i **ALG_ID** usati dai provider di servizi  di configurazione personalizzati per le specifiche AT_KEYEXCHANGE e **AT_SIGNATURE** dipendono dal provider. I mapping correnti seguono la tabella .




| Identificatore | valore | Descrizione | 
|------------|-------|-------------|
| CALG_3DES | 0x00006603 | <a href="/windows/desktop/SecGloss/t-gly"><em>Algoritmo di crittografia Triple DES.</em></a> | 
| CALG_3DES_112 | 0x00006609 | Crittografia DES <a href="/windows/desktop/SecGloss/t-gly"><em>tripla</em></a> a due chiavi con lunghezza effettiva della chiave uguale a 112 bit. | 
| CALG_AES | 0x00006611 | Advanced Encryption Standard (AES). Questo algoritmo è supportato dal provider <a href="microsoft-aes-cryptographic-provider.md">del servizio di crittografia Microsoft AES.</a> | 
| CALG_AES_128 | 0x0000660e | AES a 128 bit. Questo algoritmo è supportato dal provider <a href="microsoft-aes-cryptographic-provider.md">del servizio di crittografia Microsoft AES.</a> | 
| CALG_AES_192 | 0x0000660f | AES a 192 bit. Questo algoritmo è supportato dal provider <a href="microsoft-aes-cryptographic-provider.md">del servizio di crittografia Microsoft AES.</a> | 
| CALG_AES_256 | 0x00006610 | AES a 256 bit. Questo algoritmo è supportato dal provider <a href="microsoft-aes-cryptographic-provider.md">del servizio di crittografia Microsoft AES.</a> | 
| CALG_AGREEDKEY_ANY | 0x0000aa03 | Identificatore temporaneo dell'algoritmo per gli handle delle chiavi Diffie-Hellman concordate. | 
| CALG_CYLINK_MEK | 0x0000660c | Algoritmo per creare una chiave DES a 40 bit con bit di parità e bit di chiave azzerato per ottenere la lunghezza della chiave a 64 bit. Questo algoritmo è supportato da <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider.</a> | 
| CALG_DES | 0x00006601 | Algoritmo di crittografia DES. | 
| CALG_DESX | 0x00006604 | Algoritmo di crittografia DESX. | 
| CALG_DH_EPHEM | 0x0000aa02 | Diffie-Hellman algoritmo di scambio delle chiavi ffemero. | 
| CALG_DH_SF | 0x0000aa01 | Diffie-Hellman l'algoritmo di scambio delle chiavi di archiviazione e inoltro. | 
| CALG_DSS_SIGN | 0x00002200 | Algoritmo di firma <a href="/windows/desktop/SecGloss/p-gly"><em>a chiave pubblica</em></a> DSA. | 
| CALG_ECDH | 0x0000aa05 | Curva ellittica Diffie-Hellman di scambio delle chiavi.<blockquote>[!Note]<br />Questo algoritmo è supportato solo tramite <a href="/windows/desktop/SecCNG/cng-portal">l'API di crittografia: Next Generation.</a></blockquote><br /><strong>Windows Server 2003 e Windows XP:</strong> Questo algoritmo non è supportato.<br /> | 
| CALG_ECDH_EPHEM | 0x0000ae06 | Curva ellittica effimera Diffie-Hellman di scambio delle chiavi.<blockquote>[!Note]<br />Questo algoritmo è supportato solo tramite <a href="/windows/desktop/SecCNG/cng-portal">l'API di crittografia: Next Generation.</a></blockquote><br /><strong>Windows Server 2003 e Windows XP:</strong> Questo algoritmo non è supportato.<br /> | 
| CALG_ECDSA | 0x00002203 | Algoritmo di firma digitale a curva ellittica.<blockquote>[!Note]<br />Questo algoritmo è supportato solo tramite <a href="/windows/desktop/SecCNG/cng-portal">l'API di crittografia: Next Generation.</a></blockquote><br /><strong>Windows Server 2003 e Windows XP:</strong> Questo algoritmo non è supportato.<br /> | 
| CALG_ECMQV | 0x0000a001 | Algoritmo di scambio di chiavi Menezes, Qu e Vanstone (MQV) a curva ellittica. Questo algoritmo non è supportato. | 
| CALG_HASH_REPLACE_OWF | 0x0000800b | Algoritmo hash di funzione unidirezione. | 
| CALG_HUGHES_MD5 | 0x0000a003 | Algoritmo hash Hughes MD5. | 
| CALG_HMAC | 0x00008009 | Algoritmo hash con chiave HMAC. Questo algoritmo è supportato da <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider.</a> | 
| CALG_KEA_KEYX | 0x0000aa04 | ALGORITMO KEA per lo scambio di chiavi (FORGLE). Questo algoritmo non è supportato. | 
| CALG_MAC | 0x00008005 | <a href="/windows/desktop/SecGloss/m-gly"><em>Algoritmo</em></a> hash mac con chiave. Questo algoritmo è supportato da <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider.</a> | 
| CALG_MD2 | 0x00008001 | Algoritmo di hash MD2. Questo algoritmo è supportato da <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider.</a> | 
| CALG_MD4 | 0x00008002 | Algoritmo di hash MD4. | 
| CALG_MD5 | 0x00008003 | Algoritmo di hash MD5. Questo algoritmo è supportato da <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider.</a> | 
| CALG_NO_SIGN | 0x00002000 | Nessun algoritmo di firma. | 
| CALG_OID_INFO_CNG_ONLY | 0xffffffff | L'algoritmo viene implementato solo in CNG. La macro, IS_SPECIAL_OID_INFO_ALGID, può essere usata per determinare se un algoritmo di crittografia è supportato solo tramite le funzioni CNG. | 
| CALG_OID_INFO_PARAMETERS | 0xfffffffe | L'algoritmo è definito nei parametri codificati. L'algoritmo è supportato solo tramite CNG. La macro, IS_SPECIAL_OID_INFO_ALGID, può essere usata per determinare se un algoritmo di crittografia è supportato solo tramite le funzioni CNG. | 
| CALG_PCT1_MASTER | 0x00004c04 | Usato dal sistema Schannel.dll operativo. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni. | 
| CALG_RC2 | 0x00006602 | Algoritmo di crittografia a blocchi RC2. Questo algoritmo è supportato da <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider.</a> | 
| CALG_RC4 | 0x00006801 | Algoritmo di crittografia del flusso RC4. Questo algoritmo è supportato da <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider.</a> | 
| CALG_RC5 | 0x0000660d | Algoritmo di crittografia a blocchi RC5. | 
| CALG_RSA_KEYX | 0x0000a400 | Algoritmo di scambio di chiavi pubbliche RSA. Questo algoritmo è supportato da <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider.</a> | 
| CALG_RSA_SIGN | 0x00002400 | Algoritmo di firma a chiave pubblica RSA. Questo algoritmo è supportato da <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider.</a> | 
| CALG_SCHANNEL_ENC_KEY | 0x00004c07 | Usato dal sistema Schannel.dll operativo. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni. | 
| CALG_SCHANNEL_MAC_KEY | 0x00004c03 | Usato dal sistema Schannel.dll operativo. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni. | 
| CALG_SCHANNEL_MASTER_HASH | 0x00004c02 | Usato dal sistema Schannel.dll operativo. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni. | 
| CALG_SEAL | 0x00006802 | Algoritmo di crittografia SEAL. Questo algoritmo non è supportato. | 
| CALG_SHA | 0x00008004 | Algoritmo di hash SHA. Questo algoritmo è supportato da <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider.</a> | 
| CALG_SHA1 | 0x00008004 | Uguale a <strong>CALG_SHA</strong>. Questo algoritmo è supportato da <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider.</a> | 
| CALG_SHA_256 | 0x0000800c | Algoritmo hash SHA a 256 bit. Questo algoritmo è supportato da Microsoft Enhanced RSA e dal provider di crittografia AES. <strong>Windows XP con SP3:</strong> Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider (Prototype).<br /><strong>Windows XP con SP2, Windows XP con SP1 e Windows XP:</strong> Questo algoritmo non è supportato.<br /> | 
| CALG_SHA_384 | 0x0000800d | Algoritmo hash SHA a 384 bit. Questo algoritmo è supportato da Microsoft Enhanced RSA e dal provider di crittografia AES. <strong>Windows XP con SP3:</strong> Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider (Prototype).<br /><strong>Windows XP con SP2, Windows XP con SP1 e Windows XP:</strong> Questo algoritmo non è supportato.<br /> | 
| CALG_SHA_512 | 0x0000800e | Algoritmo hash SHA a 512 bit. Questo algoritmo è supportato da Microsoft Enhanced RSA e dal provider di crittografia AES. <strong>Windows XP con SP3:</strong> Questo algoritmo è supportato da Microsoft Enhanced RSA e AES Cryptographic Provider (Prototype).<br /><strong>Windows XP con SP2, Windows XP con SP1 e Windows XP:</strong> Questo algoritmo non è supportato.<br /> | 
| CALG_SKIPJACK | 0x0000660a | Algoritmo di crittografia a blocchi Skipjack (FORTEZZA). Questo algoritmo non è supportato. | 
| CALG_SSL2_MASTER | 0x00004c05 | Usato dal sistema Schannel.dll operativo. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni. | 
| CALG_SSL3_MASTER | 0x00004c01 | Usato dal sistema Schannel.dll operativo. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni. | 
| CALG_SSL3_SHAMD5 | 0x00008008 | Usato dal sistema Schannel.dll operativo. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni. | 
| CALG_TEK | 0x0000660b | TEK (FORTEZZA). Questo algoritmo non è supportato. | 
| CALG_TLS1_MASTER | 0x00004c06 | Usato dal Schannel.dll operativo. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni. | 
| CALG_TLS1PRF | 0x0000800a | Usato dal Schannel.dll operativo. Questo <strong>ALG_ID</strong> non deve essere usato dalle applicazioni. | 




 

Per [Microsoft Base Cryptographic Provider,](microsoft-base-cryptographic-provider.md) [Microsoft Strong Cryptographic Provider](microsoft-strong-cryptographic-provider.md)e Microsoft [Enhanced Cryptographic Provider,](microsoft-enhanced-cryptographic-provider.md)il **ALG_IDs** usato per le specifiche delle chiavi **AT_KEYEXCHANGE** **e AT_SIGNATURE** sono i seguenti:

-   **CALG_RSA_KEYX** viene usato **per** AT_KEYEXCHANGE .
-   **CALG_RSA_SIGN** viene usato **per** AT_SIGNATURE .

Per [Microsoft Base DSS](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)e Diffie-Hellman Cryptographic Provider , il **ALG_IDs** usato per le specifiche delle chiavi AT_KEYEXCHANGE **e** **AT_SIGNATURE** sono i seguenti:

-   **CALG_DH_SF** viene usato **per** AT_KEYEXCHANGE .
-   **CALG_DSS_SIGN** viene usato **per** AT_SIGNATURE .

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Wincrypt.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni di crittografia](cryptography-functions.md)
</dt> <dt>

[**CRYPT_ALGORITHM_IDENTIFIER**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
