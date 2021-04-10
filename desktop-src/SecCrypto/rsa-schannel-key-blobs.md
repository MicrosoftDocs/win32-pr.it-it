---
description: I BLOB vengono utilizzati con il provider RSA/SChannel per esportare chiavi da e importare chiavi in, il provider del servizio di crittografia (CSP).
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: BLOB di chiavi RSA/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea26a98e9c2925442166eb28245ebc471b1749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879474"
---
# <a name="rsaschannel-key-blobs"></a>BLOB di chiavi RSA/SChannel

I [*BLOB*](../secgloss/b-gly.md) vengono utilizzati con [](../secgloss/r-gly.md)il / provider [*Schannel*](../secgloss/s-gly.md) RSA per esportare chiavi da e importare chiavi in, il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).

-   [BLOB di chiavi pubbliche](#public-key-blobs)
-   [BLOB di chiavi private](#private-key-blobs)
-   [BLOB di chiavi semplici](#simple-key-blobs)

## <a name="public-key-blobs"></a>BLOB di chiavi pubbliche

I [*BLOB di chiave pubblica*](../secgloss/p-gly.md), digitare **PublicKeyBlob**, vengono usati per archiviare le [*chiavi pubbliche*](../secgloss/p-gly.md). Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

Nella tabella seguente viene descritto ogni componente di chiave pubblica. Tutti i valori sono in formato [*Little-Endian*](../secgloss/l-gly.md) .



| Campo          | Descrizione                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| modulo        | Sequenza di **byte** . I dati del modulo della chiave pubblica si trovano immediatamente dopo la struttura **RSAPUBKEY** . La lunghezza di questi dati varia a seconda della lunghezza della chiave pubblica. Il numero di byte può essere determinato dividendo il valore del membro **bitlen** di **RSAPUBKEY** di otto. |
| publickeystruc | Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                              |
| rsapubkey      | Struttura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . Il membro **Magic** deve essere impostato su 0x31415352. Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di rsa1.                                                                                      |



 

> [!Note]  
> I BLOB di chiavi pubbliche non sono crittografati. Contengono chiavi pubbliche in formato [*testo non crittografato*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>BLOB di chiavi private

I [*BLOB di chiavi private*](../secgloss/p-gly.md), digitare **PRIVATEKEYBLOB**, vengono usati per archiviare [*coppie di chiavi pubbliche/private*](../secgloss/p-gly.md). Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

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

Se il [*BLOB della chiave*](../secgloss/k-gly.md) è crittografato, tutti gli elementi tranne la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB vengono crittografati.

> [!Note]  
> L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata. È responsabilità dell'applicazione gestire queste informazioni.

 

Nella tabella seguente viene descritto ogni componente BLOB della chiave privata.

> [!Note]  
> Questi campi corrispondono ai campi descritti nella sezione 7,2 di [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \# 1 con differenze minime.

 



| Campo           | Descrizione                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| exponent1       | Sequenza di **byte** . Primo esponente. Il valore numerico è d mod (p-1).                                                                                                                           |
| exponent2       | Sequenza di **byte** . Secondo esponente. Il valore numerico è d mod (q-1).                                                                                                                          |
| coefficiente     | Sequenza di **byte** . Coefficiente. Il valore numerico è (inverso di q) mod p.                                                                                                                           |
| Modulus         | Sequenza di **byte** . Modulo. Contiene una stringa che contiene *Prime1* \* *prime2*. Spesso è noto come n.                                                                                               |
| prime1          | Sequenza di **byte** . Numero primo 1, spesso noto come p.                                                                                                                                                        |
| prime2          | Sequenza di **byte** . Numero primo 2, spesso noto come q.                                                                                                                                                        |
| publickeystruc  | Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                         |
| privateExponent | Sequenza di **byte** . Esponente privato, spesso noto come d.                                                                                                                                                  |
| rsapubkey       | Struttura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) . Il membro **Magic** deve essere impostato su 0x32415352. Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di rsa2. |



 

> [!Note]  
> I BLOB di chiavi private non sono crittografati. Contengono chiavi private in formato testo non crittografato.

 

Quando si chiama [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), lo sviluppatore può scegliere se crittografare la chiave. **PRIVATEKEYBLOB** viene crittografato se il parametro *hExpKey* contiene un handle valido per una chiave di sessione. Tutto tranne la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB è crittografata.

> [!Note]  
> L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata. L'applicazione deve gestire e archiviare queste informazioni. Se viene passato zero per *hExpKey*, la chiave privata verrà esportata senza crittografia.

 

> [!Caution]  
> È pericoloso esportare le chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da entità non autorizzate.

 

## <a name="simple-key-blobs"></a>BLOB di chiavi semplici

I [*BLOB di chiavi semplici*](../secgloss/s-gly.md), digitare **SIMPLEBLOB**, vengono usati per archiviare e trasportare le chiavi della sessione. Sono sempre crittografati con una chiave [*pubblica di scambio delle chiavi*](../secgloss/k-gly.md). Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

Nella tabella seguente vengono descritti i singoli componenti BLOB semplici.



| Campo          | Descrizione                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algido          | Struttura [**di \_ ID ALG**](alg-id.md) . In genere viene specificato l' \_ algoritmo CALG RSA \_ KEYX, che indica che i dati della chiave della sessione sono stati crittografati con una chiave pubblica di scambio delle chiavi, usando l' [*algoritmo di chiave pubblica RSA*](../secgloss/r-gly.md). |
| EncryptedKey   | Sequenza di **byte** . I dati della chiave della sessione crittografata hanno il formato di un \# blocco di crittografia PKCS 1, Type 2. Per informazioni su questo formato dati, vedere la pagina relativa a Public Key Cryptography Standards (PKCS), pubblicata da RSA Data Security, Inc.                                                                                     |
| publickeystruc | Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                         |



 

Questi dati hanno sempre le stesse dimensioni del modulo della chiave pubblica. Ad esempio, le chiavi pubbliche generate dal provider di crittografia di base Microsoft sono sempre di 512 bit (64 byte), quindi anche i dati della chiave della sessione crittografata sono sempre 64 byte.

 

 
