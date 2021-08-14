---
description: Il provider di base e il provider esteso usano gli stessi BLOB di chiavi.
ms.assetid: b4592036-0fa3-4b7e-beed-78cf1d2f39a9
title: BLOB della chiave del provider di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d95eaeaa1b6438045ebba55d2bb45785e4068154ff51818e937bc434dff7fb29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773043"
---
# <a name="base-provider-key-blobs"></a>BLOB della chiave del provider di base

Il provider di base e il provider esteso usano gli [*stessi OGGETTI BLOB di chiave.*](../secgloss/k-gly.md)

-   [BLOB di chiave pubblica](#public-key-blobs)
-   [BLOB di chiave privata](#private-key-blobs)
-   [BLOB di chiavi semplici](#simple-key-blobs)

## <a name="public-key-blobs"></a>BLOB di chiave pubblica

[*I BLOB di chiave pubblica,*](../secgloss/p-gly.md)di tipo **PUBLICKEYBLOB,** vengono usati per archiviare le chiavi pubbliche all'esterno di un provider del [*servizio*](../secgloss/c-gly.md) di crittografia (CSP). [](../secgloss/p-gly.md) I BLOB della chiave pubblica del provider di base hanno il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

La tabella seguente descrive ogni componente della chiave pubblica. Tutti i valori sono in [*formato little-endian.*](../secgloss/l-gly.md)



| Campo          | Descrizione                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulo        | I dati modulo della chiave pubblica si trovano direttamente dopo la [**struttura RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Le dimensioni di questi dati variano a seconda delle dimensioni della chiave pubblica. Il numero di byte può essere determinato dividendo il valore del campo **bitlen RSAPUBKEY** per otto. |
| publickeystruc | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                 |
| rsapubkey      | Struttura [**RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Il **membro magic** deve essere impostato su 0x31415352. Questo valore esadecimale è la [*codifica ASCII*](../secgloss/a-gly.md) di RSA1.                                                                         |



 

> [!Note]  
> I BLOB di chiave pubblica non sono crittografati. Contengono chiavi pubbliche in [*formato testo non*](../secgloss/p-gly.md) crittografato.

 

## <a name="private-key-blobs"></a>BLOB di chiave privata

[*I BLOB di chiavi private,*](../secgloss/p-gly.md)di **tipo PRIVATEKEYBLOB,** vengono usati per [*archiviare le chiavi private*](../secgloss/p-gly.md) all'esterno di un CSP. I BLOB della chiave privata del provider di base hanno il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

Nella tabella seguente viene descritto il componente BLOB della chiave privata.

> [!Note]  
> Questi campi corrispondono ai campi descritti nella sezione 7.2 di [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1 con differenze minime.

 



| Campo           | Descrizione                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Coefficiente     | Coefficiente. Ha un valore numerico (inversa di q) mod p.                                                                                                                                                |
| esponente1       | Esponente 1. Ha un valore numerico di d mod (p - 1).                                                                                                                                                        |
| esponente2       | Esponente 2. Ha un valore numerico di d mod (q - 1).                                                                                                                                                        |
| Modulus         | Modulo. Il valore è *Prime1*×*Prime2* ed è spesso noto come n.                                                                                                                                   |
| prime1          | Numero primo 1, spesso noto come p.                                                                                                                                                                             |
| prime2          | Numero primo 2, spesso noto come q.                                                                                                                                                                             |
| privateExponent | Esponente privato, spesso noto come d.                                                                                                                                                                           |
| publickeystruc  | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                         |
| rsapubkey       | Struttura [**RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Il **membro magic** deve essere impostato su 0x32415352. Questo valore esadecimale è la [*codifica ASCII*](../secgloss/a-gly.md) di RSA2. |



 

> [!Note]  
> I BLOB della chiave privata non vengono crittografati. Contengono chiavi private in formato testo non crittografato.

 

Quando si [**chiama CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)lo sviluppatore può scegliere se crittografare la chiave. **PRIVATEKEYBLOB viene** crittografato se il *parametro hExpKey* contiene un handle valido per una chiave di sessione. Tutti gli elementi, ad esempio [**publicKEYSTRUC,**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB vengono crittografati.

> [!Note]  
> L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata. L'applicazione deve gestire e archiviare queste informazioni. Se viene passato zero per *hExpKey*, la chiave privata verrà esportata senza crittografia.

 

> [!Caution]  
> È pericoloso esportare le chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da parte di entità non autorizzate.

 

## <a name="simple-key-blobs"></a>BLOB di chiavi semplici

[*I BLOB di chiavi semplici,*](../secgloss/s-gly.md)di tipo **SIMPLEBLOB,** vengono usati per archiviare e trasportare le chiavi di sessione all'esterno di un provider di servizi di configurazione. I BLOB con chiave semplice del provider di base vengono sempre crittografati con una [*chiave pubblica di scambio delle chiavi.*](../secgloss/k-gly.md) Il **membro pbData** di **SIMPLEBLOB** è una sequenza di byte nel formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

La tabella seguente descrive ogni componente del **membro pbData** di **SIMPLEBLOB.**



| Campo          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Struttura [**ALG \_ ID**](alg-id.md) che specifica l'algoritmo di crittografia usato per crittografare i dati della chiave di sessione. In genere ha un valore CALG RSA KEYX, che indica che i dati della chiave di sessione sono stati crittografati con una chiave pubblica di scambio di chiave usando \_ \_ [*l'algoritmo rsa a chiave pubblica*](../secgloss/r-gly.md).                                                                                                                           |
| Encryptedkey   | Sequenza **BYTE** che rappresenta i dati crittografati della chiave di sessione sotto forma di blocco di crittografia PKCS \# 1 di tipo 2. Per informazioni su questo formato di dati, vedere public key cryptography standards (PKCS) \# 1, pubblicato da RSA Data Security, Inc. Questi dati hanno sempre le stesse dimensioni del modulo della chiave pubblica. Ad esempio, le chiavi pubbliche generate dal provider di base Microsoft RSA possono avere una lunghezza di 512 bit (64 byte), quindi anche i dati della chiave di sessione crittografata sono sempre a 512 bit (64 byte).<br/> |
| publickeystruc | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

 

 
