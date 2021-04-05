---
description: I BLOB vengono utilizzati con il provider Diffie-Hellman/SChannel per esportare le chiavi da e importare le chiavi in, il provider del servizio di crittografia (CSP).
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: BLOB di chiavi Diffie-Hellman/SChannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a76869c6c6239e17a5ae14921805a076c9381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756536"
---
# <a name="diffie-hellmanschannel-key-blobs"></a>BLOB di chiavi Diffie-Hellman/SChannel

I [*BLOB*](../secgloss/b-gly.md) vengono utilizzati con il provider Schannel [*Diffie-Hellman*](../secgloss/d-gly.md) / [](../secgloss/s-gly.md) per esportare chiavi da e importare chiavi in, il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).

-   [BLOB di chiavi pubbliche](#public-key-blobs)
-   [BLOB di chiavi private](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOB di chiavi pubbliche

Diffie-Hellman [*BLOB di chiave pubblica*](../secgloss/p-gly.md), digitare **PublicKeyBlob**, vengono usati per scambiare il valore (G ^ X) mod P in uno scambio di chiave Diffie-Hellman. Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

La tabella seguente descrive ogni componente del [*BLOB della chiave*](../secgloss/k-gly.md).



| Campo          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | Struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . Il membro **Magic** deve essere impostato su 0x31484400. Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di DH1.                                                                                                                                                                                                                                                                                                                                                      |
| publickeystruc | Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| y              | Sequenza di **byte** . Il valore y, (G ^ X) mod P, si trova immediatamente dopo la struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . La lunghezza, in byte, della sequenza è il membro **bitlen** di **DHPUBKEY** diviso 8. Se la lunghezza dei dati risultante dal calcolo di (G ^ X) mod P è uno o più byte inferiori a P diviso 8, i dati devono essere riempiti con i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata (formato [*Little Endian*](../secgloss/l-gly.md) ). |



 

## <a name="private-key-blobs"></a>BLOB di chiavi private

I BLOB di [*chiavi private*](../secgloss/p-gly.md)d-h, digitare **PRIVATEKEYBLOB**, vengono usati per esportare e importare informazioni private di una chiave D-h. Queste chiavi vengono esportate e importate come sequenza di byte con il formato seguente.

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
| dhpubkey       | Struttura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) . Il membro **Magic** deve essere impostato su 0x32484400. Questo valore esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di DH2. |
| generatore      | Sequenza di **byte** . Il generatore G.                                                                                                                                                                      |
| publickeystruc | Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                      |
| primo          | Sequenza di **byte** . Il modulo principale, P. Questi dati devono sempre avere il bit più significativo del set di byte più significativo su uno.                                                                    |
| secret         | Sequenza di **byte** . Esponente del segreto X.                                                                                                                                                                |



 

> [!Note]  
> I valori primo, generatore e segreto devono sempre avere la stessa lunghezza, in byte. Se un valore è un byte o più più breve di quello degli altri, deve essere riempito con il numero necessario di zero byte per renderli uguali. Il primo, il generatore e il segreto sono in formato [*Little-Endian*](../secgloss/l-gly.md) .

 

 

 
