---
description: 'Altre informazioni su: membri JET_OPENTEMPORARYTABLE'
title: Membri di JET_OPENTEMPORARYTABLE (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_OPENTEMPORARYTABLE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_members(v=EXCHG.10)
ms:contentKeyID: 55104223
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af149ecba6858aca4b4877fc9446872386406838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557860"
---
# <a name="jet_opentemporarytable-members"></a><span data-ttu-id="71d00-103">Membri JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="71d00-103">JET_OPENTEMPORARYTABLE members</span></span>

<span data-ttu-id="71d00-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="71d00-104">Include protected members</span></span>  
<span data-ttu-id="71d00-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="71d00-105">Include inherited members</span></span>  

<span data-ttu-id="71d00-106">Raccolta di parametri per il metodo JetOpenTemporaryTable.</span><span class="sxs-lookup"><span data-stu-id="71d00-106">A collection of parameters for the JetOpenTemporaryTable method.</span></span>

<span data-ttu-id="71d00-107">Il tipo di [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="71d00-107">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="71d00-108">Costruttori</span><span class="sxs-lookup"><span data-stu-id="71d00-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="71d00-109">Nome</span><span class="sxs-lookup"><span data-stu-id="71d00-109">Name</span></span></th>
<th><span data-ttu-id="71d00-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71d00-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="71d00-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span><span class="sxs-lookup"><span data-stu-id="71d00-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71d00-113">Inizio</span><span class="sxs-lookup"><span data-stu-id="71d00-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="71d00-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="71d00-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="71d00-115">Nome</span><span class="sxs-lookup"><span data-stu-id="71d00-115">Name</span></span></th>
<th><span data-ttu-id="71d00-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71d00-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="71d00-118"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="71d00-118"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="71d00-119">Ottiene o imposta la dimensione massima per una chiave che rappresenta una determinata riga.</span><span class="sxs-lookup"><span data-stu-id="71d00-119">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="71d00-120">È possibile impostare la dimensione massima della chiave per controllare la modalità di troncamento delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="71d00-120">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="71d00-121">Il troncamento della chiave è importante perché può influire sul fatto che le righe siano considerate distinte.</span><span class="sxs-lookup"><span data-stu-id="71d00-121">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="71d00-122">Se questo parametro è impostato su 0 o 255, le dimensioni massime della chiave e la relativa semantica rimarranno identiche alle dimensioni massime della chiave supportate da Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="71d00-122">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="71d00-123">Questo parametro può essere impostato anche su un valore maggiore come funzione delle dimensioni della pagina del database per l'istanza <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="71d00-123">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="71d00-124">Per <a href="dn335292(v=exchg.10).md">ulteriori</a> informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="71d00-124">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="71d00-126"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="71d00-126"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="71d00-127">Ottiene o imposta la quantità massima di dati che verranno utilizzati da qualsiasi variabile lengthcolumn per costruire una chiave per una determinata riga.</span><span class="sxs-lookup"><span data-stu-id="71d00-127">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="71d00-128">Questo parametro può essere utilizzato per controllare la quantità di spazio chiave utilizzata da una determinata colonna chiave.</span><span class="sxs-lookup"><span data-stu-id="71d00-128">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="71d00-129">Questo limite è in byte.</span><span class="sxs-lookup"><span data-stu-id="71d00-129">This limit is in bytes.</span></span> <span data-ttu-id="71d00-130">Se questo parametro è zero o è uguale alla proprietà <a href="dn335290(v=exchg.10).md">cbKeyMost</a> , non è attivo alcun limite.</span><span class="sxs-lookup"><span data-stu-id="71d00-130">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="71d00-132"><a href="dn335287(v=exchg.10).md">CColumn</a></span><span class="sxs-lookup"><span data-stu-id="71d00-132"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="71d00-133">Ottiene o imposta il numero di colonne in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="71d00-133">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="71d00-135"><a href="dn351232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="71d00-135"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="71d00-136">Ottiene o imposta le opzioni per la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="71d00-136">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="71d00-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="71d00-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="71d00-139">Ottiene o imposta l'ID delle impostazioni locali e i flag di normalizzazione da utilizzare per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="71d00-139">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="71d00-140">Se questo parametro è null, verrà utilizzato il valore LCID predefinito per confrontare eventuali colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="71d00-140">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="71d00-141">Il valore LCID predefinito corrisponde alle impostazioni locali per l'inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="71d00-141">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="71d00-142">Se questo parametro è null, i flag di normalizzazione predefiniti verranno utilizzati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="71d00-142">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="71d00-143">I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="71d00-143">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="71d00-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span><span class="sxs-lookup"><span data-stu-id="71d00-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="71d00-146">Ottiene o imposta le definizioni di colonna per le colonne create nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="71d00-146">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="71d00-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="71d00-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="71d00-149">Ottiene o imposta il buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="71d00-149">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="71d00-150">Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="71d00-150">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="71d00-151">Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione di <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="71d00-151">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="71d00-153"><a href="dn335293(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="71d00-153"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="71d00-154">Ottiene l'handle di tabella per la tabella temporanea creata in seguito a una chiamata riuscita a JetOpenTemporaryTable.</span><span class="sxs-lookup"><span data-stu-id="71d00-154">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71d00-155">Inizio</span><span class="sxs-lookup"><span data-stu-id="71d00-155">Top</span></span>

## <a name="methods"></a><span data-ttu-id="71d00-156">Metodi</span><span class="sxs-lookup"><span data-stu-id="71d00-156">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="71d00-157">Nome</span><span class="sxs-lookup"><span data-stu-id="71d00-157">Name</span></span></th>
<th><span data-ttu-id="71d00-158">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71d00-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="71d00-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></span><span class="sxs-lookup"><span data-stu-id="71d00-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="71d00-161">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="71d00-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="71d00-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span><span class="sxs-lookup"><span data-stu-id="71d00-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="71d00-164">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="71d00-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="71d00-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="71d00-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="71d00-167">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="71d00-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="71d00-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="71d00-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="71d00-170">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="71d00-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><span data-ttu-id="71d00-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="71d00-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="71d00-173">Ereditato da <a href="/dotnet/api/system.object">Object</a>.</span><span class="sxs-lookup"><span data-stu-id="71d00-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><span data-ttu-id="71d00-175"><a href="dn335286(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="71d00-175"><a href="dn335286(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="71d00-176">Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>corrente.</span><span class="sxs-lookup"><span data-stu-id="71d00-176">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>.</span></span> <span data-ttu-id="71d00-177">Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</span><span class="sxs-lookup"><span data-stu-id="71d00-177">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="71d00-178">Inizio</span><span class="sxs-lookup"><span data-stu-id="71d00-178">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="71d00-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71d00-179">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="71d00-180">Riferimento</span><span class="sxs-lookup"><span data-stu-id="71d00-180">Reference</span></span>

[<span data-ttu-id="71d00-181">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="71d00-181">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="71d00-182">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="71d00-182">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
