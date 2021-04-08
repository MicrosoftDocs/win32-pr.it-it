---
description: 'Altre informazioni su: Proprietà JET_INDEXCREATE'
title: Proprietà JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 66b6ada105e6f6d12cb754f288478e85d75a07e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968347"
---
# <a name="jet_indexcreate-properties"></a><span data-ttu-id="9379d-103">Proprietà JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="9379d-103">JET_INDEXCREATE properties</span></span>

<span data-ttu-id="9379d-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="9379d-104">Include protected members</span></span>  
<span data-ttu-id="9379d-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="9379d-105">Include inherited members</span></span>  

<span data-ttu-id="9379d-106">Il tipo di [JET_INDEXCREATE](./jet-indexcreate-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="9379d-106">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="9379d-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9379d-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="9379d-108">Nome</span><span class="sxs-lookup"><span data-stu-id="9379d-108">Name</span></span></th>
<th><span data-ttu-id="9379d-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9379d-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9379d-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="9379d-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="9379d-112">Ottiene o imposta la lunghezza, in caratteri, di szKey, inclusi i due valori null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="9379d-112">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9379d-114"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="9379d-114"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="9379d-115">Ottiene o imposta la dimensione massima consentita, in byte, per le chiavi nell'indice.</span><span class="sxs-lookup"><span data-stu-id="9379d-115">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="9379d-116">Le dimensioni minime massime supportate per la chiave sono JET_cbKeyMostMin (255), ovvero le dimensioni massime della chiave legacy.</span><span class="sxs-lookup"><span data-stu-id="9379d-116">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="9379d-117">Le dimensioni massime della chiave dipendono dalle dimensioni della pagina del database <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="9379d-117">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="9379d-118">È possibile recuperare le dimensioni massime della <a href="dn351156(v=exchg.10).md">chiave con la</a>chiave.</span><span class="sxs-lookup"><span data-stu-id="9379d-118">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="9379d-119">Questo parametro viene ignorato in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9379d-119">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="9379d-120">A differenza dell'API non gestita, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) non è necessario, verrà aggiunto automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9379d-120">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9379d-122"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="9379d-122"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="9379d-123">Ottiene o imposta la lunghezza massima, in byte, di ogni colonna da archiviare nell'indice.</span><span class="sxs-lookup"><span data-stu-id="9379d-123">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9379d-125"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span><span class="sxs-lookup"><span data-stu-id="9379d-125"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="9379d-126">Ottiene o imposta il numero di colonne condizionali.</span><span class="sxs-lookup"><span data-stu-id="9379d-126">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9379d-128"><a href="dn335157(v=exchg.10).md">Err</a></span><span class="sxs-lookup"><span data-stu-id="9379d-128"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="9379d-129">Ottiene o imposta il codice di errore della creazione di questo indice.</span><span class="sxs-lookup"><span data-stu-id="9379d-129">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9379d-131"><a href="dn335119(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="9379d-131"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="9379d-132">Ottiene o imposta le opzioni di creazione degli indici.</span><span class="sxs-lookup"><span data-stu-id="9379d-132">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9379d-134"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span><span class="sxs-lookup"><span data-stu-id="9379d-134"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="9379d-135">Ottiene o imposta le opzioni di confronto Unicode facoltative.</span><span class="sxs-lookup"><span data-stu-id="9379d-135">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9379d-137"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span><span class="sxs-lookup"><span data-stu-id="9379d-137"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="9379d-138">Ottiene o imposta gli hint per l'allocazione, la manutenzione e l'utilizzo dello spazio.</span><span class="sxs-lookup"><span data-stu-id="9379d-138">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9379d-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="9379d-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="9379d-141">Ottiene o imposta le colonne condizionali facoltative.</span><span class="sxs-lookup"><span data-stu-id="9379d-141">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9379d-143"><a href="dn335121(v=exchg.10).md">szIndexName</a></span><span class="sxs-lookup"><span data-stu-id="9379d-143"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="9379d-144">Ottiene o imposta il nome dell'indice da creare.</span><span class="sxs-lookup"><span data-stu-id="9379d-144">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9379d-146"><a href="dn335161(v=exchg.10).md">szKey</a></span><span class="sxs-lookup"><span data-stu-id="9379d-146"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="9379d-147">Ottiene o imposta la descrizione della chiave di indice.</span><span class="sxs-lookup"><span data-stu-id="9379d-147">Gets or sets the description of the index key.</span></span> <span data-ttu-id="9379d-148">Si tratta di una stringa doppia con terminazione null di token delimitati da null.</span><span class="sxs-lookup"><span data-stu-id="9379d-148">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="9379d-149">Ogni token è nel formato [direction-specifier] [column-name], dove Direction-Specification è &quot; + &quot; o &quot; - &quot; .</span><span class="sxs-lookup"><span data-stu-id="9379d-149">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="9379d-150">ad esempio, un szKey di &quot; + abc\0-def\0 + ghi\0 &quot; indurrà l'indice sulle tre colonne &quot; ABC &quot; (in ordine crescente), &quot; def &quot; (in ordine decrescente) e &quot; ghi &quot; (in ordine crescente).</span><span class="sxs-lookup"><span data-stu-id="9379d-150">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="9379d-152"><a href="dn335162(v=exchg.10).md">ulDensity</a></span><span class="sxs-lookup"><span data-stu-id="9379d-152"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="9379d-153">Ottiene o imposta la densità dell'indice.</span><span class="sxs-lookup"><span data-stu-id="9379d-153">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9379d-154">Inizio</span><span class="sxs-lookup"><span data-stu-id="9379d-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="9379d-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9379d-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9379d-156">Riferimento</span><span class="sxs-lookup"><span data-stu-id="9379d-156">Reference</span></span>

[<span data-ttu-id="9379d-157">Classe JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="9379d-157">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="9379d-158">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9379d-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
