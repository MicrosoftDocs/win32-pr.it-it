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
# <a name="dss-version-3-public-key-blobs"></a><span data-ttu-id="67242-103">BLOB di chiavi pubbliche DSS versione 3</span><span class="sxs-lookup"><span data-stu-id="67242-103">DSS Version 3 Public Key BLOBs</span></span>

<span data-ttu-id="67242-104">I BLOB di [*chiavi pubbliche*](../secgloss/p-gly.md) DSS versione 3 di tipo PublicKeyBlob vengono usati per esportare e importare informazioni su una chiave pubblica DH.</span><span class="sxs-lookup"><span data-stu-id="67242-104">DSS version 3 [*Public Key BLOBs*](../secgloss/p-gly.md) of type PUBLICKEYBLOB are used to export and import information about a DH public key.</span></span> <span data-ttu-id="67242-105">Hanno il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="67242-105">They have the following format:</span></span>


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



<span data-ttu-id="67242-106">Questo formato [*BLOB*](../secgloss/b-gly.md) viene esportato quando \_ \_ si usa il flag Ver3 di crittografia BLOB con [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="67242-106">This [*BLOB*](../secgloss/b-gly.md) format is exported when the CRYPT\_BLOB\_VER3 flag is used with [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span> <span data-ttu-id="67242-107">Poiché la versione si trova nel BLOB, non è necessario specificare un flag quando si usa questo BLOB con [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="67242-107">Because the version is in the BLOB, there is no need to specify a flag when using this BLOB with [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span>

<span data-ttu-id="67242-108">Questo formato BLOB viene inoltre usato con la funzione [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) quando il valore *dwParam* KP \_ pub \_ params viene usato per impostare i parametri chiave su una chiave DSS.</span><span class="sxs-lookup"><span data-stu-id="67242-108">In addition, this BLOB format is used with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function when the *dwParam* value KP\_PUB\_PARAMS is used to set key parameters on a DSS key.</span></span> <span data-ttu-id="67242-109">Questa operazione viene eseguita quando \_ per generare la chiave è stato usato il flag di inpregen Crypt.</span><span class="sxs-lookup"><span data-stu-id="67242-109">This is done when the CRYPT\_PREGEN flag has been used to generate the key.</span></span> <span data-ttu-id="67242-110">Quando viene usato in questa situazione, il valore y viene ignorato e pertanto non deve essere incluso nel BLOB.</span><span class="sxs-lookup"><span data-stu-id="67242-110">When used in this situation, the y value is ignored and therefore should not be included in the BLOB.</span></span>

<span data-ttu-id="67242-111">La tabella seguente descrive ogni componente del BLOB della chiave.</span><span class="sxs-lookup"><span data-stu-id="67242-111">The following table describes each component of the key BLOB.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67242-112">Campo</span><span class="sxs-lookup"><span data-stu-id="67242-112">Field</span></span></th>
<th><span data-ttu-id="67242-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67242-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67242-114">Blobheader</span><span class="sxs-lookup"><span data-stu-id="67242-114">Blobheader</span></span></td>
<td><span data-ttu-id="67242-115">Struttura <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="67242-115">A <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc"><strong>BLOBHEADER</strong></a> structure.</span></span> <span data-ttu-id="67242-116">Il membro <strong>bsimbolo</strong> deve avere il valore PublicKeyBlob.</span><span class="sxs-lookup"><span data-stu-id="67242-116">The <strong>bType</strong> member must have a value of PUBLICKEYBLOB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67242-117">Dsspubkeyver3</span><span class="sxs-lookup"><span data-stu-id="67242-117">Dsspubkeyver3</span></span></td>
<td><span data-ttu-id="67242-118">Struttura <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="67242-118">A <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure.</span></span> <span data-ttu-id="67242-119">Il membro <strong>Magic</strong> deve essere impostato su &quot; DSS3 &quot; (0x33535344) per le chiavi pubbliche.</span><span class="sxs-lookup"><span data-stu-id="67242-119">The <strong>magic</strong> member should be set to &quot;DSS3&quot; (0x33535344) for public keys.</span></span> <span data-ttu-id="67242-120">Si noti che il valore esadecimale è semplicemente una codifica <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> di &quot; DSS3.&quot;</span><span class="sxs-lookup"><span data-stu-id="67242-120">Notice that the hexadecimal value is just an <a href="/windows/desktop/SecGloss/a-gly"><em>ASCII</em></a> encoding of &quot;DSS3.&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67242-121">P</span><span class="sxs-lookup"><span data-stu-id="67242-121">P</span></span></td>
<td><span data-ttu-id="67242-122">Il valore P si trova immediatamente dopo la struttura di <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> e deve essere sempre la lunghezza, in byte, del campo DSSPUBKEY_VER3 <strong>bitlenP</strong> (lunghezza in bit di P) diviso per otto (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little Endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="67242-122">The P value is located directly after the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a> structure, and should always be the length, in bytes, of the DSSPUBKEY_VER3 <strong>bitlenP</strong> field (bit length of P) divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67242-123">Q</span><span class="sxs-lookup"><span data-stu-id="67242-123">Q</span></span></td>
<td><span data-ttu-id="67242-124">Il valore Q si trova immediatamente dopo il valore P e deve essere sempre la lunghezza, in byte, del membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> diviso per otto (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little Endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="67242-124">The Q value is located directly after the P value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenQ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67242-125">G</span><span class="sxs-lookup"><span data-stu-id="67242-125">G</span></span></td>
<td><span data-ttu-id="67242-126">Il valore G si trova immediatamente dopo il valore Q e deve essere sempre la lunghezza, in byte, del membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> (lunghezza in bit di P) diviso per otto.</span><span class="sxs-lookup"><span data-stu-id="67242-126">The G value is located directly after the Q value and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="67242-127">Se la lunghezza dei dati è uno o più byte inferiori a P diviso 8, i dati devono essere riempiti con i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little Endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="67242-127">If the length of the data is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67242-128">J</span><span class="sxs-lookup"><span data-stu-id="67242-128">J</span></span></td>
<td><span data-ttu-id="67242-129">Il valore J si trova immediatamente dopo il valore G e deve essere sempre la lunghezza, in byte, del membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> diviso per otto (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little Endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="67242-129">The J value is located directly after the G value and should always be the length in bytes of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenJ</strong> member divided by eight (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span> <span data-ttu-id="67242-130">Se il valore di bitlenQ è 0, il valore è assente dal BLOB.</span><span class="sxs-lookup"><span data-stu-id="67242-130">If the bitlenQ value is 0, then the value is absent from the BLOB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67242-131">S</span><span class="sxs-lookup"><span data-stu-id="67242-131">Y</span></span></td>
<td><span data-ttu-id="67242-132">Il valore Y, (G ^ X) mod P, si trova immediatamente dopo il valore J e deve essere sempre la lunghezza, in byte, del DSSPUBKEY_VER3 membro <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong></strong></a><strong>bitlenP</strong> (lunghezza in bit di P) divisa per otto.</span><span class="sxs-lookup"><span data-stu-id="67242-132">The Y value, (G^X) mod P, is located directly after the J value, and should always be the length, in bytes, of the <a href="/previous-versions/windows/desktop/legacy/aa381983(v=vs.85)"><strong>DSSPUBKEY_VER3</strong></a><strong>bitlenP</strong> member (bit length of P) divided by eight.</span></span> <span data-ttu-id="67242-133">Se la lunghezza dei dati risultante dal calcolo di (G ^ X) mod P è uno o più byte inferiori a P diviso 8, i dati devono essere riempiti con i byte necessari (di valore zero) per rendere i dati la lunghezza desiderata (formato<a href="/windows/desktop/SecGloss/l-gly"><em>Little Endian</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="67242-133">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by 8, the data must be padded with the necessary bytes (of zero value) to make the data the desired length (<a href="/windows/desktop/SecGloss/l-gly"><em>little-endian</em></a> format).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="67242-134">Quando questa struttura viene usata con <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> con il valore <em>dwParam</em> KP_PUB_PARAMS, questo valore non è incluso nel BLOB.</span><span class="sxs-lookup"><span data-stu-id="67242-134">When this structure is used with <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a> with the <em>dwParam</em> value KP_PUB_PARAMS, then this value is not included in the BLOB.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="67242-135">I BLOB di chiavi pubbliche non sono crittografati, ma contengono chiavi pubbliche in formato testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="67242-135">Public key BLOBs are not encrypted, but contain public keys in plaintext form.</span></span>

 

 

 
