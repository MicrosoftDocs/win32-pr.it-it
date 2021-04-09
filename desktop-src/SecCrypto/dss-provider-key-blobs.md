---
description: Usato con il provider Digital Signature Standard (DSS) per esportare chiavi da e importare chiavi in, il provider del servizio di crittografia (CSP).
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: BLOB di chiavi del provider DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966590"
---
# <a name="dss-provider-key-blobs"></a>BLOB di chiavi del provider DSS

I [*BLOB*](../secgloss/b-gly.md) vengono utilizzati con il provider [*Digital Signature Standard*](../secgloss/d-gly.md) (DSS) per esportare chiavi da e importare chiavi in, il [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP).

-   [BLOB di chiavi pubbliche](#public-key-blobs)
-   [BLOB di chiavi private](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOB di chiavi pubbliche

Una [*chiave pubblica*](../secgloss/p-gly.md) DSS viene esportata e importata come BLOB, una sequenza di byte strutturata come indicato di seguito.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

Nella tabella seguente vengono descritti questi componenti. Tutti i valori sono in formato [*Little-Endian*](../secgloss/l-gly.md) .



| Campo          | Descrizione                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Struttura [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) . Il membro **Magic** deve avere un valore 0x31535344. Questo numero esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di DSS1. |
| g              | Sequenza di **byte** . Il generatore, g. Deve avere la stessa lunghezza di p. Se non ha la stessa lunghezza di p, deve essere riempita con 0x00 byte.                                                                      |
| p              | Sequenza di **byte** . Il modulo principale, p. Il bit più significativo del byte più significativo deve essere impostato su uno.                                                                                                 |
| publickeystruc | Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                |
| q              | Sequenza di **byte** . Lunghezza primo, q, 20 byte. Il bit più significativo del byte più significativo deve essere impostato su uno.                                                                                     |
| seedstruct     | Struttura [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) . Valori di inizializzazione e contatore per la verifica dei numeri primi.                                                                                                                                |
| y              | Sequenza di **byte** . Chiave pubblica, y. Deve avere la stessa lunghezza di p. Se non ha la stessa lunghezza di p, deve essere riempita con 0x00 byte.                                                                         |



 

> [!Note]  
> I [*BLOB di chiavi pubbliche*](../secgloss/p-gly.md) non sono crittografati. Contengono chiavi pubbliche in formato [*testo non crittografato*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>BLOB di chiavi private

Una [*chiave privata*](../secgloss/p-gly.md) DSS viene esportata e importata come sequenza di byte strutturata come indicato di seguito.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

Nella tabella seguente viene descritto ogni componente. Tutti i valori sono in formato [*Little-Endian*](../secgloss/l-gly.md) .



| Campo          | Descrizione                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Struttura [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) . Il membro **Magic** deve essere impostato su 0x32535344. Questo numero esadecimale è la codifica [*ASCII*](../secgloss/a-gly.md) di DSS2. |
| g              | Sequenza di **byte** . Il generatore, g. Deve avere la stessa lunghezza di p. Se non ha la stessa lunghezza di p, deve essere riempita con 0x00 byte.                                                                |
| publickeystruc | Struttura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                          |
| p              | Sequenza di **byte** . Il modulo principale, p. Il bit più significativo del byte più significativo deve essere impostato su uno.                                                                                           |
| q              | Sequenza di **byte** . Il primo, q. q ha una lunghezza di 20 byte. Il bit più significativo del byte più significativo deve essere impostato su uno.                                                                          |
| seedstruct     | Struttura [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) . Valori di inizializzazione e contatore per la verifica dei numeri primi.                                                                                                                          |
| x              | Sequenza di **byte** . Esponente del segreto, x. Deve avere sempre una lunghezza di 20 byte. Se x è di lunghezza inferiore a 20 byte, deve essere riempito con 0x00.                                                     |



 

Quando si chiama [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), lo sviluppatore può scegliere se crittografare la chiave. **PRIVATEKEYBLOB** viene crittografato se il parametro *hExpKey* contiene un handle valido per una chiave di sessione. Tutto tranne la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB è crittografata.

> [!Note]  
> L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata. L'applicazione deve gestire e archiviare queste informazioni. Se viene passato zero per *hExpKey*, la chiave privata verrà esportata senza crittografia.

 

> [!Caution]  
> È pericoloso esportare le chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da entità non autorizzate.

 

 

 
