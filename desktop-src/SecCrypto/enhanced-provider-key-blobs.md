---
description: Il provider di base, il provider sicuro e il provider avanzato usano gli stessi BLOB delle chiavi.
ms.assetid: f1bd347b-33bd-40bc-9a9b-c06f264f1af4
title: BLOB delle chiavi del provider avanzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1098ec45f73183f31cb91d15e2957dcc5964591bd8c6de4e30616df0808ade6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874441"
---
# <a name="enhanced-provider-key-blobs"></a>BLOB delle chiavi del provider avanzato

Il provider di base, il provider sicuro e il provider avanzato usano gli stessi [*BLOB delle chiavi.*](../secgloss/k-gly.md)

-   [BLOB di chiave pubblica](#public-key-blobs)
-   [BLOB di chiave privata](#private-key-blobs)
-   [BLOB di chiavi semplici](#simple-key-blobs)

## <a name="public-key-blobs"></a>BLOB di chiave pubblica

[*I BLOB con chiave pubblica,*](../secgloss/p-gly.md)di tipo **PUBLICKEYBLOB,** vengono usati per archiviare le chiavi pubbliche all'esterno di un [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP). [](../secgloss/p-gly.md) I BLOB con chiave pubblica del provider esteso hanno il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

Nella tabella seguente viene descritto ogni componente di chiave pubblica. Tutti i valori sono in [*formato little-endian.*](../secgloss/l-gly.md)



| Campo          | Descrizione                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulo        | I dati del modulo di chiave pubblica si trovano direttamente dopo la [**struttura RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Le dimensioni di questi dati variano a seconda delle dimensioni della chiave pubblica. Il numero di byte può essere determinato dividendo il valore del **campo bitlen RSAPUBKEY** per otto. |
| publickeystruc | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                 |
| rsapubkey      | Struttura [**RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Il **membro magic** deve essere impostato su 0x31415352. Questo valore esadecimale è la [*codifica ASCII*](../secgloss/a-gly.md) di RSA1.                                                                         |



 

> [!Note]  
> I BLOB con chiave pubblica non vengono crittografati. Contengono chiavi pubbliche in [*formato testo non*](../secgloss/p-gly.md) crittografato.

 

## <a name="private-key-blobs"></a>BLOB di chiave privata

[*I BLOB della chiave privata,*](../secgloss/p-gly.md)di tipo **PRIVATEKEYBLOB,** vengono usati per [*archiviare le chiavi private*](../secgloss/p-gly.md) all'esterno di un provider di servizi di configurazione. I BLOB con chiave privata del provider esteso hanno il formato seguente.

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
| Coefficiente     | Coefficiente. Ha un valore numerico (inverso di q) mod p.                                                                                                                                                |
| esponente1       | Esponente 1. Il valore numerico è d mod (p - 1).                                                                                                                                                        |
| esponente2       | Esponente 2. Il valore numerico è d mod (q - 1).                                                                                                                                                        |
| Modulus         | Modulo. Il valore è *Prime1*×*Prime2* ed è spesso noto come n.                                                                                                                                   |
| prime1          | Numero primo 1, spesso noto come p.                                                                                                                                                                             |
| prime2          | Numero primo 2, spesso noto come q.                                                                                                                                                                             |
| privateExponent | Esponente privato, spesso noto come d.                                                                                                                                                                           |
| publickeystruc  | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                         |
| rsapubkey       | Struttura [**RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Il **membro magic** deve essere impostato su 0x32415352. Questo valore esadecimale è la [*codifica ASCII*](../secgloss/a-gly.md) di RSA2. |



 

> [!Note]  
> I BLOB della chiave privata non vengono crittografati. Contengono chiavi private in formato testo non crittografato.

 

Quando si [**chiama CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)lo sviluppatore può scegliere se crittografare la chiave. **PRIVATEKEYBLOB viene** crittografato se il *parametro hExpKey* contiene un handle valido per una chiave di sessione. Tutti gli elementi, a parte la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB, sono crittografati.

> [!Note]  
> L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata. L'applicazione deve gestire e archiviare queste informazioni. Se per *hExpKey* viene passato zero, la chiave privata verrà esportata senza crittografia.

 

> [!Caution]  
> È pericoloso esportare chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da parte di entità non autorizzate.

 

## <a name="simple-key-blobs"></a>BLOB di chiavi semplici

[*I BLOB di chiavi semplici,*](../secgloss/s-gly.md)di tipo **SIMPLEBLOB,** vengono usati per archiviare e trasportare le chiavi di sessione all'esterno di un provider di servizi di configurazione. I BLOB con chiave semplice del provider esteso vengono sempre crittografati con una [*chiave pubblica di scambio di chiave*](../secgloss/k-gly.md). Il **membro pbData** di **SIMPLEBLOB** è una sequenza di byte nel formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

Nella tabella seguente viene descritto ogni componente del **membro pbData** di **SIMPLEBLOB.**



| Campo          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Struttura [**ID ALG \_**](alg-id.md) che specifica l'algoritmo di crittografia usato per crittografare i dati della chiave di sessione. In genere il valore è CALG RSA KEYX, che indica che i dati della chiave di sessione sono stati crittografati con una chiave pubblica di scambio di chiave usando \_ \_ [*l'algoritmo RSA Public Key*](../secgloss/r-gly.md).                                                                                                                           |
| Encryptedkey   | Sequenza **BYTE** che rappresenta i dati della chiave di sessione crittografati sotto forma di blocco di crittografia PKCS \# 1 di tipo 2. Per informazioni su questo formato di dati, vedere Public Key Cryptography Standards (PKCS) \# 1, pubblicato da RSA Data Security, Inc. Questi dati hanno sempre le stesse dimensioni del modulo della chiave pubblica. Ad esempio, le chiavi pubbliche generate dal provider microsoft RSA Base possono avere una lunghezza di 512 bit (64 byte), quindi anche i dati della chiave di sessione crittografati sono sempre a 512 bit (64 byte).<br/> |
| publickeystruc | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Per informazioni sui BLOB delle chiavi del provider di base e del provider esteso, vedere BLOB delle [chiavi del provider di base](base-provider-key-blobs.md).

 

 
