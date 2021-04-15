---
description: Descrive il formato di un BLOB di chiave privata esportato Diffie-Hellman versione 3.
ms.assetid: c759e6e1-f7af-4cd6-a67e-ff0da1e91eb1
title: BLOB della chiave privata della versione 3 di Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb35a6db0cfd75d34ba30d26be816a64c1b04205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484596"
---
# <a name="diffie-hellman-version-3-private-key-blobs"></a>BLOB della chiave privata della versione 3 di Diffie-Hellman

Quando viene esportato un BLOB di [*chiave privata*](../secgloss/p-gly.md) Diffie-Hellman versione 3, il formato è il seguente:


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



Questo formato [*BLOB*](../secgloss/b-gly.md) viene esportato quando \_ \_ si usa il flag Ver3 di crittografia BLOB con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Poiché la versione si trova nel BLOB, non è necessario specificare un flag quando si usa questo BLOB con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

La tabella seguente descrive ogni componente del [*BLOB della chiave*](../secgloss/k-gly.md).



| Campo         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader    | Struttura [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| dhprivkeyver3 | Struttura [**\_ Ver3 di DHPRIVKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) . Il membro **Magic** deve essere impostato su 0x34484400 per le chiavi private. Si noti che il valore esadecimale è semplicemente una codifica [*ASCII*](../secgloss/a-gly.md) "doppie DH4".                                                                                                                                                                                                                                                                                            |
| P             | Il valore P si trova immediatamente dopo la [**struttura \_ Ver3 di DHPRIVKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) e deve essere sempre la lunghezza in byte del campo **DHPRIVKEY \_ Ver3** **bitlenP** (bit length of P) diviso per otto (formato [*Little Endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                            |
| Q             | Il valore Q si trova immediatamente dopo il valore P e deve essere sempre la lunghezza in byte del campo [**DHPRIVKEY \_ Ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenQ** diviso per otto (formato [*Little Endian*](../secgloss/l-gly.md) ). Se il valore di bitlenQ è 0, il valore è assente dal BLOB.                                                                                                                                                                                                  |
| G             | Il valore G si trova immediatamente dopo il valore Q e deve essere sempre la lunghezza, in byte, del campo [**DHPRIVKEY \_ Ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenP** (bit length of P) diviso per otto. Se la lunghezza dei dati è uno o più byte inferiori a P diviso 8, i dati devono essere riempiti con i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata (formato [*Little Endian*](../secgloss/l-gly.md) ).                                                                 |
| J             | Il valore J si trova immediatamente dopo il valore G e deve essere sempre la lunghezza in byte del campo [**DHPRIVKEY \_ Ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenJ** diviso per otto (formato [*Little Endian*](../secgloss/l-gly.md) ). Se il valore di bitlenJ è 0, il valore è assente dal BLOB.                                                                                                                                                                                                  |
| S             | Il valore Y, (G ^ X) mod P, si trova immediatamente dopo il valore J e deve essere sempre la lunghezza in byte del campo [**DHPRIVKEY \_ Ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhprivkey_ver3) **bitlenP** (bit length of P) diviso per otto. Se la lunghezza dei dati risultante dal calcolo di (G ^ X) mod P è uno o più byte inferiori a P diviso 8, i dati devono essere riempiti con i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata (formato [*Little Endian*](../secgloss/l-gly.md) ). |
| X             | Il valore X è un numero intero casuale di grandi dimensioni in modo che la parte pubblica della coppia di chiavi DH, Y, sia uguale a: Y = (G ^ X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

Quando si chiama [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), lo sviluppatore può scegliere se crittografare la chiave. La chiave viene crittografata se il parametro *hExpKey* contiene un handle valido per una chiave di sessione. Tutto tranne la parte [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB è crittografata. Si noti che i parametri dell'algoritmo di crittografia e della chiave di crittografia non vengono archiviati insieme al [*BLOB della chiave privata*](../secgloss/p-gly.md). L'applicazione deve gestire e archiviare queste informazioni. Se viene passato zero per *hExpKey*, la chiave privata verrà esportata senza crittografia.

> [!Note]  
> È pericoloso esportare le chiavi private senza crittografia perché sono quindi vulnerabili all'intercettazione e all'uso da entità non autorizzate.

 

 

 
