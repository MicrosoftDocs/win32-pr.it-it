---
description: Descrive il formato di una chiave privata DSS versione 3 esportata.
ms.assetid: 650532fd-919b-495a-9fb9-981790447d3d
title: BLOB della chiave privata di DSS versione 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6706f8cbfccb8c836efefb99a30086dc459619c8477b773a557f503ebbb2243
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767256"
---
# <a name="dss-version-3-private-key-blobs"></a>BLOB della chiave privata di DSS versione 3

Quando viene esportata una chiave privata [*DSS*](../secgloss/d-gly.md) [](../secgloss/p-gly.md) versione 3, il formato è il seguente:


```C++
BLOBHEADER        blobheader; 
DSSPRIVKEY_VER3   dssprivkeyver3;
BYTE p[dssprivkeyver3.bitlenP/8]; 
                    // Where P is the prime modulus
BYTE q[dssprivkeyver3.bitlenQ/8]; 
                    // Where Q is a large factor of P-1
BYTE g[dssprivkeyver3.bitlenP/8]; 
                    // Where G is the generator parameter
BYTE j[dssprivkeyver3.bitlenJ/8]; 
                    // Where J is (P-1)/Q
BYTE y[dssprivkeyver3.bitlenP/8]; 
                    // Where Y is (G^X) mod P
BYTE x[dssprivkeyver3.bitlenX/8]; 
                    // Where X is the private exponent
```



Questo [*formato BLOB*](../secgloss/b-gly.md) viene esportato quando il flag CRYPT BLOB \_ \_ VER3 viene usato con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Poiché la versione è nel BLOB, non è necessario specificare un flag quando si usa questo BLOB con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Nella tabella seguente viene descritto ogni componente del [*BLOB della chiave*](../secgloss/k-gly.md).



| Campo          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blobheader     | Struttura [**BLOBHEADER.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) Il **membro bType** deve avere il valore PUBLICKEYBLOB.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Dssprivkeyver3 | Struttura **DSSPRIVKEY \_ VER3.** Il **membro magic** deve essere impostato su "DSS4" (0x34535344) per le chiavi private. Si noti che il valore esadecimale è solo una [*codifica ASCII*](../secgloss/a-gly.md) di "DSS4".<br/>                                                                                                                                                                                                                                                                     |
| P              | Il valore P si trova direttamente dopo la struttura **DSSPRIVKEY \_ VER3** e deve essere sempre la lunghezza, in byte, del campo **\_ bitlenP DSSPRIVKEY VER3** (lunghezza in bit di P) divisa per otto (formato [*little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                           |
| Q              | Il valore Q si trova direttamente dopo il valore P e deve essere sempre la lunghezza, in byte, del campo **\_ bitlenQ DSSPRIVKEY VER3** diviso per otto (formato [*little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                                                                     |
| G              | Il valore G si trova direttamente dopo il valore Q e deve essere sempre la lunghezza, in byte, del campo **DSSPRIVKEY \_ VER3 bitlenP** (lunghezza in bit di P) divisa per otto. Se la lunghezza dei dati è di uno o più byte inferiori a P divisa per 8, è necessario aggiungere i byte necessari (pari a zero) per rendere i dati la lunghezza desiderata (formato [*little-endian).*](../secgloss/l-gly.md)                                                                 |
| J              | Il valore J si trova direttamente dopo il valore G e deve essere sempre la lunghezza, in byte, del campo **DSSPRIVKEY \_ VER3 bitlenJ** diviso per otto (formato [*little-endian).*](../secgloss/l-gly.md) Se il valore bitlenJ è 0, il valore è assente dal BLOB.                                                                                                                                                                                                   |
| S              | Il valore Y, (G^X) mod P, si trova direttamente dopo il valore J e deve essere sempre la lunghezza, in byte, del campo **\_ bitlenP DSSPRIVKEY VER3** (lunghezza in bit di P) divisa per otto. Se la lunghezza dei dati risultanti dal calcolo di (G^X) mod P è inferiore di uno o più byte rispetto a P diviso per 8, i dati devono essere riempiti con i byte necessari (valore zero) per rendere i dati di lunghezza desiderata [*(formato little-endian).*](../secgloss/l-gly.md) |
| X              | Il valore X è un numero intero casuale di grandi dimensioni in modo che la parte pubblica della coppia di chiavi DH, Y, sia uguale a: Y = (G^X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                               |



 

Quando si chiama [**CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)lo sviluppatore può scegliere se crittografare la chiave. La chiave viene crittografata se il *parametro hExpKey* contiene un handle valido per una chiave di sessione. Tutti gli elementi, a parte la parte [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB, sono crittografati. Si noti che l'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al [*BLOB della chiave privata.*](../secgloss/p-gly.md) L'applicazione deve gestire e archiviare queste informazioni. Se per *hExpKey* viene passato zero, la chiave privata verrà esportata senza crittografia.

> [!IMPORTANT]
> È pericoloso esportare chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da parte di entità non autorizzate.

 

 

 
