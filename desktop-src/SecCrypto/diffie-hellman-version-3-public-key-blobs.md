---
description: Diffie-Hellman blob di chiave pubblica versione 3 (tipo PUBLICKEYBLOB) vengono usati per esportare e importare informazioni su una chiave pubblica DH.
ms.assetid: ba29a71a-7509-49c7-93d2-f0a699532706
title: Diffie-Hellman BLOB a chiave pubblica di Diffie-Hellman versione 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21515e370fba1c63ab3d852a88ad45b974683a3ca5ba3c3ad258733593fb6e5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767418"
---
# <a name="diffie-hellman-version-3-public-key-blobs"></a>Diffie-Hellman BLOB a chiave pubblica di Diffie-Hellman versione 3

Diffie-Hellman blob di chiave pubblica [*versione*](../secgloss/p-gly.md) 3 (tipo PUBLICKEYBLOB) vengono usati per esportare e importare informazioni su una chiave pubblica DH. Hanno il formato seguente:


```C++
BLOBHEADER blobheader; 
                 // As explained under "Data Structures"
DHPUBKEY_VER3 dhpubkeyver3;
BYTE p[dhpubkeyver3.bitlenP/8]; 
                 // Where P is the prime modulus
BYTE q[dhpubkeyver3.bitlenQ/8]; 
                 // Where Q is a large factor of P-1
BYTE g[dhpubkeyver3.bitlenP/8]; 
                 // Where G is the generator parameter
BYTE j[dhpubkeyver3.bitlenJ/8]; 
                 // Where J is (P-1)/Q
BYTE y[dhpubkeyver3.bitlenP/8]; 
                 // Where Y is (G^X) mod P
```



Questo formato BLOB viene esportato quando il flag CRYPT \_ BLOB \_ VER3 viene usato [**con CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Poiché la versione è nel BLOB, non è necessario specificare un flag quando si usa questo [*BLOB*](../secgloss/b-gly.md) con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Inoltre, questo formato BLOB viene usato con la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) quando il *valore dwParam* KP PUB PARAMS viene usato per impostare i parametri chiave in una \_ chiave \_ DH. Questa operazione viene eseguita quando è stato usato il flag CRYPT \_ PREGEN per generare la chiave. Se usato in questa situazione, il valore y viene ignorato e pertanto non deve essere incluso nel BLOB.

La tabella seguente descrive ogni componente del BLOB della chiave.



| Campo        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader   | Struttura [**BLOBHEADER.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) Il **membro bType** deve avere il valore PUBLICKEYBLOB.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| dhpubkeyver3 | Struttura [**DHPUBKEY \_ VER3.**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) Il **membro magic** deve essere impostato su 0x33484400 per le chiavi pubbliche. Si noti che il valore esadecimale è solo una [*codifica ASCII*](../secgloss/a-gly.md) "DH3".                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| P            | Il valore P si trova direttamente dopo la struttura [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) e deve essere sempre la lunghezza, in byte, del campo **bitlenP** **DHPUBKEY \_ VER3** (lunghezza in bit di P) divisa per otto (formato [*little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                                                                                                                                                                                           |
| Q            | Il valore Q si trova direttamente dopo il valore P e deve essere sempre la lunghezza in byte del campo **bitlenQ** [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) diviso per otto (formato [*little-endian).*](../secgloss/l-gly.md) Se il valore bitlenQ è 0, il valore è assente dal BLOB.                                                                                                                                                                                                                                                                                                                                                                 |
| G            | Il valore G si trova direttamente dopo il valore Q e deve essere sempre la lunghezza, in byte, del campo **bitlenP** [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) (lunghezza in bit di P) divisa per otto. Se la lunghezza dei dati è inferiore di uno o più byte rispetto a P diviso per 8, è necessario aggiungere ai dati i byte necessari (con valore zero) per ottenere la lunghezza desiderata (formato [*little-endian).*](../secgloss/l-gly.md)                                                                                                                                                                                                                              |
| J            | Il valore J si trova direttamente dopo il valore G e deve essere sempre la lunghezza in byte del campo **bitlenJ** [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) diviso per otto (formato [*little-endian).*](../secgloss/l-gly.md) Se il valore bitlenQ è 0, il valore è assente dal BLOB.                                                                                                                                                                                                                                                                                                                                                                 |
| S            | Il valore Y, (G^X) mod P, si trova direttamente dopo il valore J e deve essere sempre la lunghezza in byte del campo **bitlenP** [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) (lunghezza in bit di P) diviso per otto. Se la lunghezza dei dati risultanti dal calcolo di (G^X) mod P è minore di uno o più byte rispetto a P diviso per 8, è necessario aggiungere i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata [*(formato little-endian).*](../secgloss/l-gly.md) Quando questa struttura viene usata con [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con il valore *dwParam* KP PUB PARAMS, questo valore non \_ è \_ incluso nel BLOB. |



 

> [!Note]  
> I BLOB con chiave pubblica non vengono crittografati, ma contengono chiavi pubbliche in formato testo non crittografato.

 

 

 
