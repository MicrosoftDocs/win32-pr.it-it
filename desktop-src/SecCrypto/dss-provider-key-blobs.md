---
description: Usato con il provider DSS (Digital Signature Standard) per esportare e importare chiavi nel provider del servizio di crittografia (CSP).
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: BLOB delle chiavi del provider DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: accbc2cbdc7f543fb2a46b77741d5be7f9e216efcf36b487f7d08912bf5d3991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875321"
---
# <a name="dss-provider-key-blobs"></a>BLOB delle chiavi del provider DSS

[*I BLOB*](../secgloss/b-gly.md) vengono usati con il provider [*DSS (Digital Signature Standard)*](../secgloss/d-gly.md) per esportare e importare chiavi nel [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP).

-   [BLOB di chiave pubblica](#public-key-blobs)
-   [BLOB di chiave privata](#private-key-blobs)

## <a name="public-key-blobs"></a>BLOB di chiave pubblica

Una chiave [*pubblica*](../secgloss/p-gly.md) DSS viene esportata e importata come BLOB, una sequenza di byte strutturata come segue.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

Nella tabella seguente vengono descritti questi componenti. Tutti i valori sono in [*formato little-endian.*](../secgloss/l-gly.md)



| Campo          | Descrizione                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Struttura [**DSSPUBKEY.**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) Il **membro magic** deve avere un valore di 0x31535344. Questo numero esadecimale è la [*codifica ASCII*](../secgloss/a-gly.md) di DSS1. |
| g              | Sequenza **BYTE.** Generatore, g. Deve avere la stessa lunghezza di p. Se non ha la stessa lunghezza di p, deve essere riempito con 0x00 byte.                                                                      |
| p              | Sequenza **BYTE.** Modulo primo, p. Il bit più significativo del byte più significativo deve essere impostato su uno.                                                                                                 |
| publickeystruc | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                |
| q              | Sequenza **BYTE.** Valore primo, q, 20 byte di lunghezza. Il bit più significativo del byte più significativo deve essere impostato su uno.                                                                                     |
| seedstruct     | Struttura [**DSSSEED.**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) Valori di valore di valore di seed e contatore per la verifica dei numeri primi.                                                                                                                                |
| y              | Sequenza **BYTE.** Chiave pubblica, y. Deve avere la stessa lunghezza di p. Se non ha la stessa lunghezza di p, deve essere riempito con 0x00 byte.                                                                         |



 

> [!Note]  
> [*I BLOB con chiave pubblica*](../secgloss/p-gly.md) non vengono crittografati. Contengono chiavi pubbliche in [*formato testo non*](../secgloss/p-gly.md) crittografato.

 

## <a name="private-key-blobs"></a>BLOB di chiave privata

Una chiave privata [*DSS*](../secgloss/p-gly.md) viene esportata e importata come sequenza di byte strutturata come segue.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

La tabella seguente descrive ogni componente. Tutti i valori sono in [*formato little-endian.*](../secgloss/l-gly.md)



| Campo          | Descrizione                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Struttura [**DSSPUBKEY.**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) Il **membro magic** deve essere impostato su 0x32535344. Questo numero esadecimale è la [*codifica ASCII*](../secgloss/a-gly.md) di DSS2. |
| g              | Sequenza **BYTE.** Generatore, g. Deve avere la stessa lunghezza di p. Se non ha la stessa lunghezza di p, deve essere riempito con 0x00 byte.                                                                |
| publickeystruc | Struttura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                          |
| p              | Sequenza **BYTE.** Modulo primo, p. Il bit più significativo del byte più significativo deve essere impostato su uno.                                                                                           |
| q              | Sequenza **BYTE.** Numero primo, q. q ha una lunghezza di 20 byte. Il bit più significativo del byte più significativo deve essere impostato su uno.                                                                          |
| seedstruct     | Struttura [**DSSSEED.**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) Valori di valore di valore di seed e contatore per la verifica dei numeri primi.                                                                                                                          |
| x              | Sequenza **BYTE.** Esponente segreto, x. Deve avere sempre una lunghezza di 20 byte. Se x ha una lunghezza inferiore a 20 byte, deve essere riempito con 0x00.                                                     |



 

Quando si chiama [**CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)lo sviluppatore può scegliere se crittografare la chiave. **PRIVATEKEYBLOB viene** crittografato se il *parametro hExpKey* contiene un handle valido per una chiave di sessione. Tutti gli elementi, a parte la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB, sono crittografati.

> [!Note]  
> L'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al BLOB della chiave privata. L'applicazione deve gestire e archiviare queste informazioni. Se per *hExpKey* viene passato zero, la chiave privata verrà esportata senza crittografia.

 

> [!Caution]  
> È pericoloso esportare chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da parte di entità non autorizzate.

 

 

 
