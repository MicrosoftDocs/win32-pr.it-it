---
description: I BLOB vengono usati con il provider Diffie-Hellman per esportare e importare chiavi nel provider del servizio di crittografia (CSP).
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: Diffie-Hellman BLOB delle chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e993daf5b9ec0509ae6fa01df4edc06bafec733bb80f7b014921026fbc35ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767715"
---
# <a name="diffie-hellman-key-blobs"></a>Diffie-Hellman BLOB delle chiavi

[*I BLOB*](../secgloss/b-gly.md) vengono usati con il provider [*Diffie-Hellman*](../secgloss/d-gly.md) per esportare e importare chiavi nel [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP).

-   [BLOB di chiave pubblica](#public-key-blobs)
-   [BLOB di chiave privata](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOB di chiave pubblica

Diffie-Hellman [*BLOB*](../secgloss/p-gly.md)di chiave pubblica, tipo **PUBLICKEYBLOB**, vengono usati per scambiare il valore (G^X) mod P in uno scambio Diffie-Hellman chiave. Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

Nella tabella seguente vengono descritti i singoli componenti della [*chiave BLOB.*](../secgloss/k-gly.md)



| Campo          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Struttura [**DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) Il **membro magic** deve essere impostato su 0x31484400. Questo valore esadecimale è la [*codifica ASCII*](../secgloss/a-gly.md) di "DH1".                                                                                                                                                                                                                                                                                                                                                                 |
| publickeystruc | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| y              | Sequenza **BYTE.** Il valore Y, (G^X) mod P, si trova direttamente dopo la struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) e deve essere sempre la lunghezza, in byte, del campo **di bitlen DHPUBKEY** (lunghezza in bit di P) divisa per otto. Se la lunghezza dei dati risultanti dal calcolo di (G^X) mod P è minore di uno o più byte rispetto a P diviso per otto, è necessario aggiungere i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata [*(formato little-endian).*](../secgloss/l-gly.md) |



 

## <a name="private-key-blobs"></a>BLOB di chiave privata

Diffie-Hellman [*BLOB di chiave privata,*](../secgloss/p-gly.md)digitare **PRIVATEKEYBLOB**, vengono usati per archiviare le informazioni pubbliche/private di una Diffie-Hellman chiave. Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

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
| dhpubkey       | Struttura [**DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) Il **membro magic** deve essere impostato su 0x32484400. Questo valore esadecimale è la [*codifica ASCII*](../secgloss/a-gly.md) di "DH2". |
| generatore      | Sequenza **BYTE.** Il generatore, G.                                                                                                                                                                       |
| publickeystruc | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                        |
| Primo          | Sequenza **BYTE.** Modulo primo, P. Questi dati devono sempre avere il bit più significativo del byte più significativo impostato su uno.                                                                      |
| secret         | Sequenza **BYTE.** Esponente segreto, X.                                                                                                                                                                 |



 

> [!Note]  
> Il generatore e il segreto devono avere sempre la stessa lunghezza, in byte. Se è un byte o più breve dell'altro, deve essere riempito con il numero necessario di byte con valore zero per renderli uguali. Sia il generatore che il segreto sono in [*formato little endian.*](../secgloss/l-gly.md)

 

 

 
