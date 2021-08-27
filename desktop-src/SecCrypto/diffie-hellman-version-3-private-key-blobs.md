---
description: Descrive il formato di un BLOB di chiave Diffie-Hellman versione 3 esportato.
ms.assetid: c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1
title: Diffie-Hellman versione 3 BLOB di chiave privata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1adeb61f7f64d7362e832ea395a125f9f25de9a5ac2ce82325645fd19745bb4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100831"
---
# <a name="diffie-hellman-version-3-private-key-blobs"></a>Diffie-Hellman versione 3 BLOB di chiave privata

Quando viene esportato Diffie-Hellman BLOB di [*chiave*](../secgloss/p-gly.md) privata versione 3, il formato è il seguente:


```C++
BLOBHEADER        blobheader;
DHPRIVKEY_VER3   dhprivkeyver3;
BYTE p[dhprivkeyver3.bitlenP/8]; 
            // Where P is the prime modulus
BYTE q[dhprivkeyver3.bitlenQ/8]; 
            // Where Q is a large factor of P-1
BYTE g[dhprivkeyver3.bitlenP/8]; 
            // Where G is the generator parameter
BYTE j[dhprivkeyver3.bitlenJ/8]; 
            // Where J is (P-1)/Q
BYTE y[dhprivkeyver3.bitlenP/8]; 
            // Where Y is (G^X) mod P
BYTE x[dhprivkeyver3.bitlenX/8]; 
            // Where X is the private exponent
```



Questo [*formato BLOB*](../secgloss/b-gly.md) viene esportato quando il flag CRYPT BLOB \_ \_ VER3 viene usato con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Poiché la versione è nel BLOB, non è necessario specificare un flag quando si usa questo BLOB con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Nella tabella seguente viene descritto ogni componente del [*BLOB della chiave.*](../secgloss/k-gly.md)



| Campo         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader    | Struttura [**BLOBHEADER.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| dhprivkeyver3 | Struttura [**DHPRIVKEY \_ VER3.**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) Il **membro magic** deve essere impostato su 0x34484400 per le chiavi private. Si noti che il valore esadecimale è solo una [*codifica ASCII*](../secgloss/a-gly.md) "DH4".                                                                                                                                                                                                                                                                                            |
| P             | Il valore P si trova direttamente dopo la struttura [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) e deve essere sempre la lunghezza in byte del campo **bitlenP** **DHPRIVKEY \_ VER3** (lunghezza in bit di P) diviso per otto (formato [*little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                            |
| Q             | Il valore Q si trova direttamente dopo il valore P e deve essere sempre la lunghezza in byte del campo **bitlenQ** [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) diviso per otto (formato [*little-endian).*](../secgloss/l-gly.md) Se il valore bitlenQ è 0, il valore è assente dal BLOB.                                                                                                                                                                                                  |
| G             | Il valore G si trova direttamente dopo il valore Q e deve essere sempre la lunghezza in byte del campo **bitlenP** [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) (lunghezza in bit di P) divisa per otto. Se la lunghezza dei dati è inferiore di uno o più byte rispetto a P diviso per 8, è necessario aggiungere i byte necessari (pari a zero) per rendere i dati la lunghezza desiderata (formato [*little-endian).*](../secgloss/l-gly.md)                                                                 |
| J             | Il valore J si trova direttamente dopo il valore G e deve essere sempre la lunghezza in byte del campo **bitlenJ** [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) diviso per otto (formato [*little-endian).*](../secgloss/l-gly.md) Se il valore bitlenJ è 0, il valore è assente dal BLOB.                                                                                                                                                                                                  |
| S             | Il valore Y, (G^X) mod P, si trova direttamente dopo il valore J e deve essere sempre la lunghezza in byte del campo **bitlenP** [**DHPRIVKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) (lunghezza in bit di P) divisa per otto. Se la lunghezza dei dati risultanti dal calcolo di (G^X) mod P è inferiore di uno o più byte rispetto a P diviso per 8, i dati devono essere riempiti con i byte necessari (valore zero) per rendere i dati di lunghezza desiderata [*(formato little-endian).*](../secgloss/l-gly.md) |
| X             | Il valore X è un numero intero casuale di grandi dimensioni in modo che la parte pubblica della coppia di chiavi DH, Y, sia uguale a: Y = (G^X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Quando si [**chiama CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)lo sviluppatore può scegliere se crittografare la chiave. La chiave viene crittografata se il *parametro hExpKey* contiene un handle valido per una chiave di sessione. Tutti gli elementi, ad parte la parte [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB, sono crittografati. Si noti che l'algoritmo di crittografia e i parametri della chiave di crittografia non vengono archiviati insieme al [*BLOB della chiave privata.*](../secgloss/p-gly.md) L'applicazione deve gestire e archiviare queste informazioni. Se per *hExpKey* viene passato zero, la chiave privata verrà esportata senza crittografia.

> [!Note]  
> È pericoloso esportare chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da parte di entità non autorizzate.

 

 

 
