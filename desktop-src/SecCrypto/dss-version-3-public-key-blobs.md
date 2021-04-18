---
description: I BLOB di chiavi pubbliche DSS versione 3 di tipo PUBLICKEYBLOB vengono usati per esportare e importare informazioni su una chiave pubblica DH.
ms.assetid: 9aac1d61-8b61-4f0f-b037-afe4a60302de
title: BLOB di chiavi pubbliche DSS versione 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593ac69025ff046a9a8d014286c2464788c07b02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306440"
---
# <a name="dss-version-3-public-key-blobs"></a>BLOB di chiavi pubbliche DSS versione 3

I BLOB di [*chiavi pubbliche*](../secgloss/p-gly.md) DSS versione 3 di tipo PublicKeyBlob vengono usati per esportare e importare informazioni su una chiave pubblica DH. Hanno il formato seguente:


```C++
BLOBHEADER blobheader; 
        // As explained under "Data Structures"
DSSPUBKEY_VER3 dsspubkeyver3;
BYTE p[dsspubkeyver3.bitlenP/8]; 
       // Where P is the prime modulus
BYTE q[dsspubkeyver3.bitlenQ/8]; 
       // Where Q is a large factor of P-1
BYTE g[dsspubkeyver3.bitlenP/8]; 
       // Where G is the generator parameter
BYTE j[dsspubkeyver3.bitlenJ/8]; 
       // Where J is (P-1)/Q
BYTE y[dsspubkeyver3.bitlenP/8]; 
       // Where Y is (G^X) mod P
```



Questo formato [*BLOB*](../secgloss/b-gly.md) viene esportato quando \_ \_ si usa il flag Ver3 di crittografia BLOB con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey). Poiché la versione si trova nel BLOB, non è necessario specificare un flag quando si usa questo BLOB con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).

Questo formato BLOB viene inoltre usato con la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) quando il valore *dwParam* KP \_ pub \_ params viene usato per impostare i parametri chiave su una chiave DSS. Questa operazione viene eseguita quando \_ per generare la chiave è stato usato il flag di inpregen Crypt. Quando viene usato in questa situazione, il valore y viene ignorato e pertanto non deve essere incluso nel BLOB.

La tabella seguente descrive ogni componente del BLOB della chiave.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Campo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Blobheader</td>
<td>Struttura <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> . Il membro <strong>bsimbolo</strong> deve avere il valore PublicKeyBlob.</td>
</tr>
<tr class="even">
<td>Dsspubkeyver3</td>
<td>Struttura <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> . Il membro <strong>Magic</strong> deve essere impostato su &quot; DSS3 &quot; (0x33535344) per le chiavi pubbliche. Si noti che il valore esadecimale è semplicemente una codifica <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> di &quot; DSS3.&quot;<br/></td>
</tr>
<tr class="odd">
<td>P</td>
<td>Il valore P si trova immediatamente dopo la struttura di <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> e deve essere sempre la lunghezza, in byte, del campo DSSPUBKEY_VER3 <strong>bitlenP</strong> (lunghezza in bit di P) diviso per otto (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little Endian</em></a> ).</td>
</tr>
<tr class="even">
<td>Q</td>
<td>Il valore Q si trova immediatamente dopo il valore P e deve essere sempre la lunghezza, in byte, del membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> diviso per otto (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little Endian</em></a> ).</td>
</tr>
<tr class="odd">
<td>G</td>
<td>Il valore G si trova immediatamente dopo il valore Q e deve essere sempre la lunghezza, in byte, del membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> (lunghezza in bit di P) diviso per otto. Se la lunghezza dei dati è uno o più byte inferiori a P diviso 8, i dati devono essere riempiti con i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little Endian</em></a> ).</td>
</tr>
<tr class="even">
<td>J</td>
<td>Il valore J si trova immediatamente dopo il valore G e deve essere sempre la lunghezza, in byte, del membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> diviso per otto (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little Endian</em></a> ). Se il valore di bitlenQ è 0, il valore è assente dal BLOB.</td>
</tr>
<tr class="odd">
<td>S</td>
<td>Il valore Y, (G ^ X) mod P, si trova immediatamente dopo il valore J e deve essere sempre la lunghezza, in byte, del DSSPUBKEY_VER3 membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong></strong></a><strong>bitlenP</strong> (lunghezza in bit di P) divisa per otto. Se la lunghezza dei dati risultante dal calcolo di (G ^ X) mod P è uno o più byte inferiori a P diviso 8, i dati devono essere riempiti con i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little Endian</em></a> ).
<blockquote>
[!Note]<br />
Quando questa struttura viene usata con <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> con il valore <em>dwParam</em> KP_PUB_PARAMS, questo valore non è incluso nel BLOB.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> I BLOB di chiavi pubbliche non sono crittografati, ma contengono chiavi pubbliche in formato testo non crittografato.

 

 

 
