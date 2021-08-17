---
description: I BLOB vengono usati con il provider Diffie-Hellman/Schannel per esportare le chiavi dal provider del servizio di crittografia (CSP) e importare le chiavi in .
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: BLOB delle chiavi Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c653e26f53611e8b00a1dae4e49df7084e6dc655d67f11550a430860fab12d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767695"
---
# <a name="diffie-hellmanschannel-key-blobs"></a>BLOB delle chiavi Diffie-Hellman/Schannel

[*I BLOB*](../secgloss/b-gly.md) vengono usati con il provider [*Schannel Diffie-Hellman*](../secgloss/d-gly.md)per esportare le chiavi dal provider del servizio di crittografia / [](../secgloss/s-gly.md) (CSP) e importare le chiavi in . [](../secgloss/c-gly.md)

-   [BLOB di chiave pubblica](#public-key-blobs)
-   [BLOB di chiave privata](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOB di chiave pubblica

Diffie-Hellman BLOB con [*chiave*](../secgloss/p-gly.md)pubblica, digitare **PUBLICKEYBLOB**, vengono usati per scambiare il valore (G^X) mod P in uno scambio Diffie-Hellman chiave. Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

Nella tabella seguente viene descritto ogni componente del [*BLOB della chiave.*](../secgloss/k-gly.md)



| Campo          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Struttura [**DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) Il **membro magic** deve essere impostato su 0x31484400. Questo valore esadecimale è la [*codifica ASCII*](../secgloss/a-gly.md) di DH1.                                                                                                                                                                                                                                                                                                                                                      |
| publickeystruc | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| y              | Sequenza **BYTE.** Il valore y, (G^X) mod P, si trova direttamente dopo la [**struttura DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) La lunghezza, in byte, della sequenza è il membro **bitlen** di **DHPUBKEY** diviso per otto. Se la lunghezza dei dati risultanti dal calcolo di (G^X) mod P è di uno o più byte più corta di P divisa per otto, i dati devono essere riempiti con i byte necessari (valore zero) per rendere i dati di lunghezza desiderata [*(formato little-endian).*](../secgloss/l-gly.md) |



 

## <a name="private-key-blobs"></a>BLOB di chiave privata

I BLOB della [*chiave privata*](../secgloss/p-gly.md)D-H, di tipo **PRIVATEKEYBLOB,** vengono usati per esportare e importare informazioni private di una chiave D-H. Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

La tabella seguente descrive ogni componente del BLOB della chiave.



| Campo          | Descrizione                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Struttura [**DHPUBKEY.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) Il **membro magic** deve essere impostato su 0x32484400. Questo valore esadecimale è la [*codifica ASCII*](../secgloss/a-gly.md) di DH2. |
| generatore      | Sequenza **BYTE.** Generatore G.                                                                                                                                                                      |
| publickeystruc | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                      |
| Primo          | Sequenza **BYTE.** Modulo primo, P. Questi dati devono avere sempre il bit più significativo del byte più significativo impostato su uno.                                                                    |
| secret         | Sequenza **BYTE.** Esponente segreto X.                                                                                                                                                                |



 

> [!Note]  
> I valori primi, generatori e segreti devono avere sempre la stessa lunghezza, in byte. Se un valore è di un byte o più breve degli altri, deve essere riempito con il numero necessario di zero byte per renderli uguali. Il primo, il generatore e il segreto sono in [*formato little-endian.*](../secgloss/l-gly.md)

 

 

 
