---
description: 'Altre informazioni su: Proprietà JET_OPENTEMPORARYTABLE'
title: Proprietà JET_OPENTEMPORARYTABLE (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_OPENTEMPORARYTABLE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_properties(v=EXCHG.10)
ms:contentKeyID: 55104127
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e9c55afddd1128a517c27f6a86466b488e6924a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104552064"
---
# <a name="jet_opentemporarytable-properties"></a><span data-ttu-id="1593f-103">Proprietà JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="1593f-103">JET_OPENTEMPORARYTABLE properties</span></span>

<span data-ttu-id="1593f-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="1593f-104">Include protected members</span></span>  
<span data-ttu-id="1593f-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="1593f-105">Include inherited members</span></span>  

<span data-ttu-id="1593f-106">Il tipo di [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="1593f-106">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="1593f-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1593f-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="1593f-108">Nome</span><span class="sxs-lookup"><span data-stu-id="1593f-108">Name</span></span></th>
<th><span data-ttu-id="1593f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1593f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="1593f-111"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="1593f-111"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="1593f-112">Ottiene o imposta la dimensione massima per una chiave che rappresenta una determinata riga.</span><span class="sxs-lookup"><span data-stu-id="1593f-112">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="1593f-113">È possibile impostare la dimensione massima della chiave per controllare la modalità di troncamento delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="1593f-113">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="1593f-114">Il troncamento della chiave è importante perché può influire sul fatto che le righe siano considerate distinte.</span><span class="sxs-lookup"><span data-stu-id="1593f-114">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="1593f-115">Se questo parametro è impostato su 0 o 255, le dimensioni massime della chiave e la relativa semantica rimarranno identiche alle dimensioni massime della chiave supportate da Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1593f-115">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="1593f-116">Questo parametro può essere impostato anche su un valore maggiore come funzione delle dimensioni della pagina del database per l'istanza <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="1593f-116">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="1593f-117">Per <a href="dn335292(v=exchg.10).md">ulteriori</a> informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="1593f-117">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="1593f-119"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="1593f-119"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="1593f-120">Ottiene o imposta la quantità massima di dati che verranno utilizzati da qualsiasi variabile lengthcolumn per costruire una chiave per una determinata riga.</span><span class="sxs-lookup"><span data-stu-id="1593f-120">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="1593f-121">Questo parametro può essere utilizzato per controllare la quantità di spazio chiave utilizzata da una determinata colonna chiave.</span><span class="sxs-lookup"><span data-stu-id="1593f-121">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="1593f-122">Questo limite è in byte.</span><span class="sxs-lookup"><span data-stu-id="1593f-122">This limit is in bytes.</span></span> <span data-ttu-id="1593f-123">Se questo parametro è zero o è uguale alla proprietà <a href="dn335290(v=exchg.10).md">cbKeyMost</a> , non è attivo alcun limite.</span><span class="sxs-lookup"><span data-stu-id="1593f-123">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="1593f-125"><a href="dn335287(v=exchg.10).md">CColumn</a></span><span class="sxs-lookup"><span data-stu-id="1593f-125"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="1593f-126">Ottiene o imposta il numero di colonne in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="1593f-126">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="1593f-128"><a href="dn351232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="1593f-128"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="1593f-129">Ottiene o imposta le opzioni per la tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="1593f-129">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="1593f-131"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="1593f-131"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="1593f-132">Ottiene o imposta l'ID delle impostazioni locali e i flag di normalizzazione da utilizzare per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="1593f-132">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="1593f-133">Se questo parametro è null, verrà utilizzato il valore LCID predefinito per confrontare eventuali colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="1593f-133">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="1593f-134">Il valore LCID predefinito corrisponde alle impostazioni locali per l'inglese (Stati Uniti).</span><span class="sxs-lookup"><span data-stu-id="1593f-134">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="1593f-135">Se questo parametro è null, i flag di normalizzazione predefiniti verranno utilizzati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="1593f-135">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="1593f-136">I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="1593f-136">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="1593f-138"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span><span class="sxs-lookup"><span data-stu-id="1593f-138"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="1593f-139">Ottiene o imposta le definizioni di colonna per le colonne create nella tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="1593f-139">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="1593f-141"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="1593f-141"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="1593f-142">Ottiene o imposta il buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea.</span><span class="sxs-lookup"><span data-stu-id="1593f-142">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="1593f-143">Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna.</span><span class="sxs-lookup"><span data-stu-id="1593f-143">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="1593f-144">Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione di <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="1593f-144">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="1593f-146"><a href="dn335293(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="1593f-146"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="1593f-147">Ottiene l'handle di tabella per la tabella temporanea creata in seguito a una chiamata riuscita a JetOpenTemporaryTable.</span><span class="sxs-lookup"><span data-stu-id="1593f-147">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1593f-148">Inizio</span><span class="sxs-lookup"><span data-stu-id="1593f-148">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="1593f-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1593f-149">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1593f-150">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1593f-150">Reference</span></span>

[<span data-ttu-id="1593f-151">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="1593f-151">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="1593f-152">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="1593f-152">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
