---
description: I BLOB vengono usati con il provider RSA/Schannel per esportare e importare chiavi nel provider del servizio di crittografia (CSP).
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: BLOB di chiavi RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be8bfa8b87ee901317e220583ff7b08ea110e342a2d9dd9abb477053ffdf05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900536"
---
# <a name="rsaschannel-key-blobs"></a>BLOB di chiavi RSA/Schannel

[*I BLOB*](../secgloss/b-gly.md) vengono usati con il provider [*RSA*](../secgloss/r-gly.md)Schannel per esportare e importare chiavi nel provider del servizio di / [](../secgloss/s-gly.md) crittografia (CSP). [](../secgloss/c-gly.md)

-   [BLOB di chiave pubblica](#public-key-blobs)
-   [BLOB di chiave privata](#private-key-blobs)
-   [BLOB di chiavi semplici](#simple-key-blobs)

## <a name="public-key-blobs"></a>BLOB di chiave pubblica

[*I BLOB di chiave pubblica,*](../secgloss/p-gly.md)di **tipo PUBLICKEYBLOB,** vengono usati per archiviare [*le chiavi pubbliche*](../secgloss/p-gly.md). Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

La tabella seguente descrive ogni componente della chiave pubblica. Tutti i valori sono in [*formato little-endian.*](../secgloss/l-gly.md)



| Campo          | Descrizione                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulo        | Sequenza **BYTE.** I dati modulo della chiave pubblica si trovano direttamente dopo la **struttura RSAPUBKEY.** La lunghezza di questi dati varia a seconda della lunghezza della chiave pubblica. Il numero di byte può essere determinato dividendo il valore del membro **bitlen** di **RSAPUBKEY** per otto. |
| publickeystruc | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                              |
| rsapubkey      | Struttura [**RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Il **membro magic** deve essere impostato su 0x31415352. Questo valore esadecimale è la [*codifica ASCII*](../secgloss/a-gly.md) di RSA1.                                                                                      |



 

> [!Note]  
> I BLOB di chiave pubblica non sono crittografati. Contengono chiavi pubbliche in [*formato testo non*](../secgloss/p-gly.md) crittografato.

 

## <a name="private-key-blobs"></a>BLOB di chiave privata

[*I BLOB di chiavi private,*](../secgloss/p-gly.md)di **tipo PRIVATEKEYBLOB,** vengono usati per archiviare [*coppie di chiavi pubblica/privata*](../secgloss/p-gly.md). Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

Se il [*BLOB della chiave*](../secgloss/k-gly.md) è crittografato, vengono crittografati tutti gli elementi ad parte della parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB.

> [!Note]  
> L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata. È responsabilità dell'applicazione gestire queste informazioni.

 

La tabella seguente descrive ogni componente BLOB della chiave privata.

> [!Note]  
> Questi campi corrispondono ai campi descritti nella sezione 7.2 di [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1 con differenze minime.

 



| Campo           | Descrizione                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| esponente1       | Sequenza **BYTE.** Primo esponente. Ha un valore numerico di d mod (p - 1).                                                                                                                           |
| esponente2       | Sequenza **BYTE.** Secondo esponente. Ha un valore numerico di d mod (q - 1).                                                                                                                          |
| Coefficiente     | Sequenza **BYTE.** Coefficiente. Ha un valore numerico (inversa di q) mod p.                                                                                                                           |
| Modulus         | Sequenza **BYTE.** Modulo. Contiene una stringa che contiene *Prime1* \* *Prime2.* È spesso noto come n.                                                                                               |
| prime1          | Sequenza **BYTE.** Numero primo 1, spesso noto come p.                                                                                                                                                        |
| prime2          | Sequenza **BYTE.** Numero primo 2, spesso noto come q.                                                                                                                                                        |
| publickeystruc  | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                         |
| privateExponent | Sequenza **BYTE.** Esponente privato, spesso noto come d.                                                                                                                                                  |
| rsapubkey       | Struttura [**RSAPUBKEY.**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) Il **membro magic** deve essere impostato su 0x32415352. Questo valore esadecimale è la [*codifica ASCII*](../secgloss/a-gly.md) di RSA2. |



 

> [!Note]  
> I BLOB della chiave privata non vengono crittografati. Contengono chiavi private in formato testo non crittografato.

 

Quando si [**chiama CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)lo sviluppatore può scegliere se crittografare la chiave. **PRIVATEKEYBLOB viene** crittografato se il *parametro hExpKey* contiene un handle valido per una chiave di sessione. Tutti gli elementi, ad esempio [**publicKEYSTRUC,**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB vengono crittografati.

> [!Note]  
> L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata. L'applicazione deve gestire e archiviare queste informazioni. Se viene passato zero per *hExpKey*, la chiave privata verrà esportata senza crittografia.

 

> [!Caution]  
> È pericoloso esportare le chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da parte di entità non autorizzate.

 

## <a name="simple-key-blobs"></a>BLOB di chiavi semplici

[*I BLOB di chiavi semplici,*](../secgloss/s-gly.md)di tipo **SIMPLEBLOB,** vengono usati per archiviare e trasportare le chiavi della sessione. Questi vengono sempre crittografati con una [*chiave pubblica per lo scambio di chiavi.*](../secgloss/k-gly.md) Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

La tabella seguente descrive ogni componente BLOB semplice.



| Campo          | Descrizione                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | Struttura [**ALG \_ ID.**](alg-id.md) Specifica in genere l'algoritmo CALG RSA KEYX, che indica che i dati della chiave di sessione sono stati crittografati con una chiave pubblica per lo scambio di chiavi, usando \_ l'algoritmo \_ RSA a chiave [*pubblica*](../secgloss/r-gly.md). |
| Encryptedkey   | Sequenza **BYTE.** I dati della chiave di sessione crittografata sono nel formato di un blocco di crittografia PKCS \# 1 di tipo 2. Per informazioni su questo formato di dati, vedere public key cryptography standards (PKCS), pubblicato da RSA Data Security, Inc.                                                                                     |
| publickeystruc | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                         |



 

Questi dati hanno sempre le stesse dimensioni del modulo della chiave pubblica. Ad esempio, le chiavi pubbliche generate da Microsoft Base Cryptographic Provider hanno sempre una lunghezza di 512 bit (64 byte), quindi anche i dati della chiave della sessione crittografata sono sempre di 64 byte.

 

 
