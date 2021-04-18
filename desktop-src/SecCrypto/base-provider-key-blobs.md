---
description: Il provider di base e il provider esteso utilizzano gli stessi BLOB di chiavi.
ms.assetid: b4592036-0fa3-4b7e-beed-78cf1d2f39a9
title: BLOB di chiavi del provider di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c763f97fe6e7868246e0bce30ee2a741e8bd212f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307697"
---
# <a name="base-provider-key-blobs"></a>BLOB di chiavi del provider di base

Il provider di base e il provider esteso utilizzano gli stessi [*BLOB di chiavi*](../secgloss/k-gly.md).

-   [BLOB di chiavi pubbliche](#public-key-blobs)
-   [BLOB di chiavi private](#private-key-blobs)
-   [BLOB di chiavi semplici](#simple-key-blobs)

## <a name="public-key-blobs"></a>BLOB di chiavi pubbliche

I [*BLOB di chiave pubblica*](../secgloss/p-gly.md), digitare **PublicKeyBlob**, vengono usati per archiviare le [*chiavi pubbliche*](../secgloss/p-gly.md) all'esterno di un [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP). I BLOB di chiavi pubbliche del provider di base hanno il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

Nella tabella seguente viene descritto ogni componente di chiave pubblica. Tutti i valori sono in formato [*Little-Endian*](../secgloss/l-gly.md) .



| Campo          | Descrizione                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulo        | I dati del modulo della chiave pubblica si trovano immediatamente dopo la struttura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . Le dimensioni di questi dati variano a seconda delle dimensioni della chiave pubblica. Il numero di byte può essere determinato dividendo il valore del campo **RSAPUBKEY bitlen** di otto. |
| publickeystruc | Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                 |
| rsapubkey      | Struttura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . Il membro **Magic** deve essere impostato su 0x31415352. Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di rsa1.                                                                         |



 

> [!Note]  
> I BLOB di chiavi pubbliche non sono crittografati. Contengono chiavi pubbliche in formato [*testo non crittografato*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>BLOB di chiavi private

I [*BLOB di chiavi private*](../secgloss/p-gly.md), digitare **PRIVATEKEYBLOB**, vengono usati per archiviare [*chiavi private*](../secgloss/p-gly.md) all'esterno di un CSP. I BLOB di chiavi private del provider di base hanno il formato seguente.

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
> Questi campi corrispondono ai campi descritti nella sezione 7,2 di [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1 con differenze minime.

 



| Campo           | Descrizione                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| coefficiente     | Coefficiente. Il valore numerico è (inverso di q) mod p.                                                                                                                                                |
| exponent1       | Esponente 1. Il valore numerico è d mod (p-1).                                                                                                                                                        |
| exponent2       | Esponente 2. Il valore numerico è d mod (q-1).                                                                                                                                                        |
| Modulus         | Modulo. Il valore è *Prime1*×*prime2* ed è spesso noto come n.                                                                                                                                   |
| prime1          | Numero primo 1, spesso noto come p.                                                                                                                                                                             |
| prime2          | Numero primo 2, spesso noto come q.                                                                                                                                                                             |
| privateExponent | Esponente privato, spesso noto come d.                                                                                                                                                                           |
| publickeystruc  | Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                         |
| rsapubkey       | Struttura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . Il membro **Magic** deve essere impostato su 0x32415352. Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di rsa2. |



 

> [!Note]  
> I BLOB di chiavi private non sono crittografati. Contengono chiavi private in formato testo non crittografato.

 

Quando si chiama [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), lo sviluppatore può scegliere se crittografare la chiave. **PRIVATEKEYBLOB** viene crittografato se il parametro *hExpKey* contiene un handle valido per una chiave di sessione. Tutto tranne la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB è crittografata.

> [!Note]  
> L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata. L'applicazione deve gestire e archiviare queste informazioni. Se viene passato zero per *hExpKey*, la chiave privata verrà esportata senza crittografia.

 

> [!Caution]  
> È pericoloso esportare le chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da entità non autorizzate.

 

## <a name="simple-key-blobs"></a>BLOB di chiavi semplici

I [*BLOB di chiavi semplici*](../secgloss/s-gly.md), digitare **SIMPLEBLOB**, vengono usati per archiviare e trasportare chiavi di sessione all'esterno di un CSP. I BLOB di chiavi semplici del provider di base sono sempre crittografati con una [*chiave pubblica di scambio delle chiavi*](../secgloss/k-gly.md). Il membro **pbData** di **SIMPLEBLOB** è una sequenza di byte nel formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

Nella tabella seguente viene descritto ogni componente del membro **pbData** di **SIMPLEBLOB**.



| Campo          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algido          | Struttura [**di \_ ID ALG**](alg-id.md) che specifica l'algoritmo di crittografia utilizzato per crittografare i dati della chiave della sessione. Questo ha in genere il valore CALG \_ RSA \_ KEYX, che indica che i dati della chiave della sessione sono stati crittografati con una chiave pubblica di scambio delle chiavi usando l' [*algoritmo di chiave pubblica RSA*](../secgloss/r-gly.md).                                                                                                                           |
| EncryptedKey   | Sequenza di **byte** che rappresenta i dati della chiave della sessione crittografata sotto forma di un \# blocco di crittografia PKCS 1, Type 2. Per informazioni su questo formato dati, vedere la pagina relativa a Public Key Cryptography Standards (PKCS) \# 1, pubblicata da RSA Data Security, Inc. Questi dati hanno sempre le stesse dimensioni del modulo della chiave pubblica. Ad esempio, le chiavi pubbliche generate dal provider di base Microsoft RSA possono avere una lunghezza di 512 bit (64 byte), quindi anche i dati della chiave della sessione crittografata sono sempre 512 bit (64 byte).<br/> |
| publickeystruc | Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

 

 
