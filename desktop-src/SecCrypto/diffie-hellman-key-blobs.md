---
description: I BLOB vengono utilizzati con il provider di Diffie-Hellman per esportare chiavi da e importare chiavi in, il provider del servizio di crittografia (CSP).
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: BLOB di chiavi di Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9194a9c12542fc0acf36aa0064a2f3e304e25f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311929"
---
# <a name="diffie-hellman-key-blobs"></a>BLOB di chiavi di Diffie-Hellman

I [*BLOB*](../secgloss/b-gly.md) vengono usati con il provider [*Diffie-Hellman*](../secgloss/d-gly.md) per esportare le chiavi da e importare le chiavi in, il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).

-   [BLOB di chiavi pubbliche](#public-key-blobs)
-   [BLOB di chiavi private](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOB di chiavi pubbliche

Diffie-Hellman [*BLOB di chiave pubblica*](../secgloss/p-gly.md), digitare **PublicKeyBlob**, vengono usati per scambiare il valore (G ^ X) mod P in uno scambio di chiave Diffie-Hellman. Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

La tabella seguente descrive ogni componente del [*BLOB della chiave*](../secgloss/k-gly.md).



| Campo          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . Il membro **Magic** deve essere impostato su 0x31484400. Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) "DH1".                                                                                                                                                                                                                                                                                                                                                                 |
| publickeystruc | Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| y              | Sequenza di **byte** . Il valore Y, (G ^ X) mod P, si trova immediatamente dopo la struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) e deve essere sempre la lunghezza, in byte, del campo **bitlen DHPUBKEY** (lunghezza in bit di P) divisa per otto. Se la lunghezza dei dati risultante dal calcolo di (G ^ X) mod P è uno o più byte inferiori a P diviso 8, i dati devono essere riempiti con i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata (formato [*Little Endian*](../secgloss/l-gly.md) ). |



 

## <a name="private-key-blobs"></a>BLOB di chiavi private

Diffie-Hellman [*BLOB di chiavi private*](../secgloss/p-gly.md), digitare **PRIVATEKEYBLOB**, per archiviare le informazioni pubbliche/private di una chiave di Diffie-Hellman. Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

La tabella seguente descrive ogni componente del BLOB della chiave.



| Campo          | Descrizione                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . Il membro **Magic** deve essere impostato su 0x32484400. Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) "DH2". |
| generatore      | Sequenza di **byte** . Il generatore, G.                                                                                                                                                                       |
| publickeystruc | Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                        |
| primo          | Sequenza di **byte** . Il modulo principale, P. Questi dati devono sempre avere il bit più significativo del set di byte più significativo su uno.                                                                      |
| secret         | Sequenza di **byte** . Esponente del segreto, X.                                                                                                                                                                 |



 

> [!Note]  
> Il generatore e il segreto devono avere sempre la stessa lunghezza, in byte. Se il valore di è uno o più più breve dell'altro, deve essere riempito con il numero necessario di byte di valore pari a zero per renderli uguali. Il generatore e il segreto sono in formato [*Little-Endian*](../secgloss/l-gly.md) .

 

 

 
