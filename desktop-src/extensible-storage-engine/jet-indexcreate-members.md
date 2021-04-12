---
description: 'Altre informazioni su: membri JET_INDEXCREATE'
title: Membri JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_members(v=EXCHG.10)
ms:contentKeyID: 55103641
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbe9ce962221db30c8cdae90461fa55fc0baea19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233365"
---
# <a name="jet_indexcreate-members"></a><span data-ttu-id="02c05-103">Membri JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="02c05-103">JET_INDEXCREATE members</span></span>

<span data-ttu-id="02c05-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="02c05-104">Include protected members</span></span>  
<span data-ttu-id="02c05-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="02c05-105">Include inherited members</span></span>  

<span data-ttu-id="02c05-106">Contiene le informazioni necessarie per creare un indice sui dati in un database ESE.</span><span class="sxs-lookup"><span data-stu-id="02c05-106">Contains the information needed to create an index over data in an ESE database.</span></span> <span data-ttu-id="02c05-107">Contiene le informazioni necessarie per creare un indice sui dati in un database ESE.</span><span class="sxs-lookup"><span data-stu-id="02c05-107">Contains the information needed to create an index over data in an ESE database.</span></span>

<span data-ttu-id="02c05-108">Il tipo di [JET_INDEXCREATE](./jet-indexcreate-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="02c05-108">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="02c05-109">Costruttori</span><span class="sxs-lookup"><span data-stu-id="02c05-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="02c05-110">Nome</span><span class="sxs-lookup"><span data-stu-id="02c05-110">Name</span></span></th>
<th><span data-ttu-id="02c05-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02c05-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="02c05-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span><span class="sxs-lookup"><span data-stu-id="02c05-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02c05-114">Inizio</span><span class="sxs-lookup"><span data-stu-id="02c05-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="02c05-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="02c05-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="02c05-116">Nome</span><span class="sxs-lookup"><span data-stu-id="02c05-116">Name</span></span></th>
<th><span data-ttu-id="02c05-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02c05-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="02c05-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="02c05-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="02c05-120">Ottiene o imposta la lunghezza, in caratteri, di szKey, inclusi i due valori null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="02c05-120">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="02c05-122"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="02c05-122"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="02c05-123">Ottiene o imposta la dimensione massima consentita, in byte, per le chiavi nell'indice.</span><span class="sxs-lookup"><span data-stu-id="02c05-123">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="02c05-124">Le dimensioni minime massime supportate per la chiave sono JET_cbKeyMostMin (255), ovvero le dimensioni massime della chiave legacy.</span><span class="sxs-lookup"><span data-stu-id="02c05-124">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="02c05-125">Le dimensioni massime della chiave dipendono dalle dimensioni della pagina del database <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="02c05-125">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="02c05-126">È possibile recuperare le dimensioni massime della <a href="dn351156(v=exchg.10).md">chiave con la</a>chiave.</span><span class="sxs-lookup"><span data-stu-id="02c05-126">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="02c05-127">Questo parametro viene ignorato in Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="02c05-127">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="02c05-128">A differenza dell'API non gestita, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) non è necessario, verrà aggiunto automaticamente.</span><span class="sxs-lookup"><span data-stu-id="02c05-128">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="02c05-130"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="02c05-130"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="02c05-131">Ottiene o imposta la lunghezza massima, in byte, di ogni colonna da archiviare nell'indice.</span><span class="sxs-lookup"><span data-stu-id="02c05-131">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="02c05-133"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span><span class="sxs-lookup"><span data-stu-id="02c05-133"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="02c05-134">Ottiene o imposta il numero di colonne condizionali.</span><span class="sxs-lookup"><span data-stu-id="02c05-134">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="02c05-136"><a href="dn335157(v=exchg.10).md">Err</a></span><span class="sxs-lookup"><span data-stu-id="02c05-136"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="02c05-137">Ottiene o imposta il codice di errore della creazione di questo indice.</span><span class="sxs-lookup"><span data-stu-id="02c05-137">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="02c05-139"><a href="dn335119(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="02c05-139"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="02c05-140">Ottiene o imposta le opzioni di creazione degli indici.</span><span class="sxs-lookup"><span data-stu-id="02c05-140">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="02c05-142"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span><span class="sxs-lookup"><span data-stu-id="02c05-142"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="02c05-143">Ottiene o imposta le opzioni di confronto Unicode facoltative.</span><span class="sxs-lookup"><span data-stu-id="02c05-143">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="02c05-145"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span><span class="sxs-lookup"><span data-stu-id="02c05-145"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="02c05-146">Ottiene o imposta gli hint per l'allocazione, la manutenzione e l'utilizzo dello spazio.</span><span class="sxs-lookup"><span data-stu-id="02c05-146">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="02c05-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="02c05-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="02c05-149">Ottiene o imposta le colonne condizionali facoltative.</span><span class="sxs-lookup"><span data-stu-id="02c05-149">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="02c05-151"><a href="dn335121(v=exchg.10).md">szIndexName</a></span><span class="sxs-lookup"><span data-stu-id="02c05-151"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="02c05-152">Ottiene o imposta il nome dell'indice da creare.</span><span class="sxs-lookup"><span data-stu-id="02c05-152">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="02c05-154"><a href="dn335161(v=exchg.10).md">szKey</a></span><span class="sxs-lookup"><span data-stu-id="02c05-154"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="02c05-155">Ottiene o imposta la descrizione della chiave di indice.</span><span class="sxs-lookup"><span data-stu-id="02c05-155">Gets or sets the description of the index key.</span></span> <span data-ttu-id="02c05-156">Si tratta di una stringa doppia con terminazione null di token delimitati da null.</span><span class="sxs-lookup"><span data-stu-id="02c05-156">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="02c05-157">Ogni token è nel formato [direction-specifier] [column-name], dove Direction-Specification è &quot; + &quot; o &quot; - &quot; .</span><span class="sxs-lookup"><span data-stu-id="02c05-157">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="02c05-158">ad esempio, un szKey di &quot; + abc\0-def\0 + ghi\0 &quot; indurrà l'indice sulle tre colonne &quot; ABC &quot; (in ordine crescente), &quot; def &quot; (in ordine decrescente) e &quot; ghi &quot; (in ordine crescente).</span><span class="sxs-lookup"><span data-stu-id="02c05-158">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="02c05-160"><a href="dn335162(v=exchg.10).md">ulDensity</a></span><span class="sxs-lookup"><span data-stu-id="02c05-160"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="02c05-161">Ottiene o imposta la densità dell'indice.</span><span class="sxs-lookup"><span data-stu-id="02c05-161">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02c05-162">Inizio</span><span class="sxs-lookup"><span data-stu-id="02c05-162">Top</span></span>

## <a name="methods"></a><span data-ttu-id="02c05-163">Metodi</span><span class="sxs-lookup"><span data-stu-id="02c05-163">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="02c05-164">Nome</span><span class="sxs-lookup"><span data-stu-id="02c05-164">Name</span></span></th>
<th><span data-ttu-id="02c05-165">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02c05-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="02c05-167"><a href="dn335116(v=exchg.10).md">ContentEquals</a></span><span class="sxs-lookup"><span data-stu-id="02c05-167"><a href="dn335116(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="02c05-168">Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.</span><span class="sxs-lookup"><span data-stu-id="02c05-168">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="02c05-170"><a href="dn335153(v=exchg.10).md">DeepClone</a></span><span class="sxs-lookup"><span data-stu-id="02c05-170"><a href="dn335153(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="02c05-171">Restituisce una copia completa dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="02c05-171">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="02c05-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="02c05-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="02c05-174">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="02c05-174">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="02c05-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="02c05-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="02c05-177">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="02c05-177">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="02c05-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="02c05-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="02c05-180">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="02c05-180">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="02c05-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="02c05-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="02c05-183">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="02c05-183">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="02c05-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="02c05-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="02c05-186">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="02c05-186">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="02c05-188"><a href="dn335154(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="02c05-188"><a href="dn335154(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="02c05-189">Generare una rappresentazione di stringa dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="02c05-189">Generate a string representation of the instance.</span></span> <span data-ttu-id="02c05-190">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="02c05-190">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02c05-191">Inizio</span><span class="sxs-lookup"><span data-stu-id="02c05-191">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="02c05-192">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02c05-192">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02c05-193">Riferimento</span><span class="sxs-lookup"><span data-stu-id="02c05-193">Reference</span></span>

[<span data-ttu-id="02c05-194">Classe JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="02c05-194">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="02c05-195">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="02c05-195">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
