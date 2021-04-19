---
description: Per esportare e importare le informazioni relative a una chiave pubblica DH vengono usati i BLOB di chiave pubblica Diffie-Hellman versione 3 (tipo PUBLICKEYBLOB).
ms.assetid: ba29a71a-7509-49c7-93d2-f0a699532706
title: BLOB di chiave pubblica della versione 3 di Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7228e4b4a786dc0eb25d1ba199b5c20923dd8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311925"
---
# <a name="diffie-hellman-version-3-public-key-blobs"></a>BLOB di chiave pubblica della versione 3 di Diffie-Hellman

Per esportare e importare le informazioni relative a una chiave pubblica DH vengono usati i [*BLOB di chiave pubblica*](../secgloss/p-gly.md) Diffie-Hellman versione 3 (tipo PublicKeyBlob). Hanno il formato seguente:


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



Questo formato BLOB viene esportato quando \_ \_ si usa il flag Ver3 di crittografia BLOB con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Poiché la versione si trova nel BLOB, non è necessario specificare un flag quando si usa questo [*BLOB*](../secgloss/b-gly.md) con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Questo formato BLOB viene inoltre usato con la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) quando il valore *dwParam* KP \_ pub \_ params viene usato per impostare i parametri chiave su una chiave DH. Questa operazione viene eseguita quando \_ per generare la chiave è stato usato il flag di inpregen Crypt. Quando viene usato in questa situazione, il valore y viene ignorato e pertanto non deve essere incluso nel BLOB.

La tabella seguente descrive ogni componente del BLOB della chiave.



| Campo        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader   | Struttura [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) . Il membro **bsimbolo** deve avere il valore PublicKeyBlob.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| dhpubkeyver3 | Struttura [**\_ Ver3 di DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) . Il membro **Magic** deve essere impostato su 0x33484400 per le chiavi pubbliche. Si noti che il valore esadecimale è semplicemente una codifica [*ASCII*](../secgloss/a-gly.md) "DH3".                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| P            | Il valore P si trova immediatamente dopo la [**struttura \_ Ver3 di DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) e deve essere sempre la lunghezza, in byte, del **campo DHPUBKEY \_ Ver3** **bitlenP** (bit length of P) diviso per otto (formato [*Little Endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                                                                                                                                                                                           |
| Q            | Il valore Q si trova immediatamente dopo il valore P e deve essere sempre la lunghezza in byte del campo [**DHPUBKEY \_ Ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenQ** diviso per otto (formato [*Little Endian*](../secgloss/l-gly.md) ). Se il valore di bitlenQ è 0, il valore è assente dal BLOB.                                                                                                                                                                                                                                                                                                                                                                 |
| G            | Il valore G si trova immediatamente dopo il valore Q e deve essere sempre la lunghezza, in byte, del campo [**DHPUBKEY \_ Ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenP** (bit length of P) diviso per otto. Se la lunghezza dei dati è uno o più byte inferiori a P diviso 8, i dati devono essere riempiti con i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata (formato [*Little Endian*](../secgloss/l-gly.md) ).                                                                                                                                                                                                                              |
| J            | Il valore J si trova immediatamente dopo il valore G e deve essere sempre la lunghezza in byte del campo [**DHPUBKEY \_ Ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenJ** diviso per otto (formato [*Little Endian*](../secgloss/l-gly.md) ). Se il valore di bitlenQ è 0, il valore è assente dal BLOB.                                                                                                                                                                                                                                                                                                                                                                 |
| S            | Il valore Y, (G ^ X) mod P, si trova immediatamente dopo il valore J e deve essere sempre la lunghezza in byte del campo [**DHPUBKEY \_ Ver3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenP** (bit length of P) diviso per otto. Se la lunghezza dei dati risultante dal calcolo di (G ^ X) mod P è uno o più byte inferiori a P diviso 8, i dati devono essere riempiti con i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata (formato [*Little Endian*](../secgloss/l-gly.md) ). Quando questa struttura viene utilizzata con [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con il valore di *dwParam* KP \_ pub \_ params, questo valore non è incluso nel BLOB. |



 

> [!Note]  
> I BLOB di chiavi pubbliche non sono crittografati, ma contengono chiavi pubbliche in formato testo non crittografato.

 

 

 
