---
description: 'Altre informazioni su: struttura JET_SPACEHINTS'
title: Struttura JET_SPACEHINTS
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf786d1f47b5eaae3f9540c8635853020f9b0521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305759"
---
# <a name="jet_spacehints-structure"></a><span data-ttu-id="77c5d-103">Struttura JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="77c5d-103">JET_SPACEHINTS Structure</span></span>


<span data-ttu-id="77c5d-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="77c5d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_spacehints-structure"></a><span data-ttu-id="77c5d-105">Struttura JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="77c5d-105">JET_SPACEHINTS Structure</span></span>

<span data-ttu-id="77c5d-106">La struttura di **JET_SPACEHINTS** contiene informazioni sui modelli di allocazione dello spazio quando un albero b aumenta attraverso le divisioni di accodamento o Hotpoint.</span><span class="sxs-lookup"><span data-stu-id="77c5d-106">The **JET_SPACEHINTS** structure contains information about space allocation patterns when a b-tree grows through append or hotpoint splits.</span></span> <span data-ttu-id="77c5d-107">Le divisioni di Accodamento si verificano quando vengono aggiunti record alla fine di un albero b e si verificano divisioni Hotpoint quando più record vengono aggiunti allo stesso punto di inserimento virtuale (ad esempio, aggiungendo ' Marie ',' Mark ',' Martin '',' Mary ' al centro di una struttura b-tree ordinata in ordine alfabetico).</span><span class="sxs-lookup"><span data-stu-id="77c5d-107">Append splits happen when records are added to the end of a b-tree and hotpoint splits happen when multiple records are added to the same virtual insertion point (for example, adding 'Marie', 'Mark', 'Martin', 'Mary' to the middle of a b-tree that is sorted alphabetically).</span></span>

<span data-ttu-id="77c5d-108">**Windows 7:** La struttura **JET_SPACEHINTS** è stata introdotta in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="77c5d-108">**Windows 7:** The **JET_SPACEHINTS** structure is introduced in Windows 7.</span></span>

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a><span data-ttu-id="77c5d-109">Membri</span><span class="sxs-lookup"><span data-stu-id="77c5d-109">Members</span></span>

<span data-ttu-id="77c5d-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="77c5d-110">**cbStruct**</span></span>

<span data-ttu-id="77c5d-111">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="77c5d-111">The size, in bytes, of this structure.</span></span> <span data-ttu-id="77c5d-112">Impostare questo membro su sizeof (JET_SPACEHINTS).</span><span class="sxs-lookup"><span data-stu-id="77c5d-112">Set this member to sizeof( JET_SPACEHINTS ).</span></span>

<span data-ttu-id="77c5d-113">**ulInitialDensity**</span><span class="sxs-lookup"><span data-stu-id="77c5d-113">**ulInitialDensity**</span></span>

<span data-ttu-id="77c5d-114">Densità in corrispondenza del layout (Accodamento).</span><span class="sxs-lookup"><span data-stu-id="77c5d-114">The density at (append) layout.</span></span>

<span data-ttu-id="77c5d-115">**cbInitial**</span><span class="sxs-lookup"><span data-stu-id="77c5d-115">**cbInitial**</span></span>

<span data-ttu-id="77c5d-116">Dimensioni iniziali (in byte) dell'oggetto da creare.</span><span class="sxs-lookup"><span data-stu-id="77c5d-116">The initial size (in bytes) of the object being created.</span></span> <span data-ttu-id="77c5d-117">Deve essere un multiplo delle dimensioni della pagina del database.</span><span class="sxs-lookup"><span data-stu-id="77c5d-117">This must be a multiple of the database page size.</span></span>

<span data-ttu-id="77c5d-118">**grbit**</span><span class="sxs-lookup"><span data-stu-id="77c5d-118">**grbit**</span></span>

<span data-ttu-id="77c5d-119">Gruppo di bit che contiene le opzioni da utilizzare per questa struttura, che includono zero o più degli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="77c5d-119">A group of bits that contain the options to be used for this structure, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77c5d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="77c5d-120">Value</span></span></p></th>
<th><p><span data-ttu-id="77c5d-121">Significato</span><span class="sxs-lookup"><span data-stu-id="77c5d-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77c5d-122">JET_bitSpaceHintsUtilizeParentSpace</span><span class="sxs-lookup"><span data-stu-id="77c5d-122">JET_bitSpaceHintsUtilizeParentSpace</span></span><br />
<span data-ttu-id="77c5d-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="77c5d-123">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="77c5d-124">Modifica i criteri di allocazione interna per ottenere spazio heirarchically dall'elemento padre diretto di un albero b.</span><span class="sxs-lookup"><span data-stu-id="77c5d-124">Changes the internal allocation policy to get space heirarchically from the immediate parent of a b-tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77c5d-125">JET_bitCreateHintAppendSequential</span><span class="sxs-lookup"><span data-stu-id="77c5d-125">JET_bitCreateHintAppendSequential</span></span><br />
<span data-ttu-id="77c5d-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="77c5d-126">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="77c5d-127">Consente di aumentare il comportamento di suddivisione dell'accodamento in base alla dinamica di crescita della tabella (impostata da cbMinExtent, ulGrowth, cbMaxExtent).</span><span class="sxs-lookup"><span data-stu-id="77c5d-127">Enables append split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77c5d-128">JET_bitCreateHintHotpointSequential</span><span class="sxs-lookup"><span data-stu-id="77c5d-128">JET_bitCreateHintHotpointSequential</span></span><br />
<span data-ttu-id="77c5d-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="77c5d-129">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="77c5d-130">Consente di aumentare il comportamento di suddivisione Hotpoint in base alla dinamica di crescita della tabella (impostata da cbMinExtent, ulGrowth, cbMaxExtent).</span><span class="sxs-lookup"><span data-stu-id="77c5d-130">Enables hotpoint split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77c5d-131">JET_bitRetrieveHintTableScanForward</span><span class="sxs-lookup"><span data-stu-id="77c5d-131">JET_bitRetrieveHintTableScanForward</span></span><br />
<span data-ttu-id="77c5d-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="77c5d-132">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="77c5d-133">Se impostato, il client indica che l'analisi sequenziale di avanzamento è il modello di utilizzo predominante della tabella.</span><span class="sxs-lookup"><span data-stu-id="77c5d-133">If set, the client indicates that forward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77c5d-134">JET_bitRetrieveHintTableScanBackward</span><span class="sxs-lookup"><span data-stu-id="77c5d-134">JET_bitRetrieveHintTableScanBackward</span></span><br />
<span data-ttu-id="77c5d-135">0x00000020</span><span class="sxs-lookup"><span data-stu-id="77c5d-135">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="77c5d-136">Se impostato, il client indica che l'analisi sequenziale indietro è il modello di utilizzo predominante della tabella.</span><span class="sxs-lookup"><span data-stu-id="77c5d-136">If set, the client indicates that backward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77c5d-137">JET_bitDeleteHintTableSequential</span><span class="sxs-lookup"><span data-stu-id="77c5d-137">JET_bitDeleteHintTableSequential</span></span><br />
<span data-ttu-id="77c5d-138">0x00000100</span><span class="sxs-lookup"><span data-stu-id="77c5d-138">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="77c5d-139">Se impostato, l'applicazione prevede che la tabella venga pulita in ordine sequenziale, dalla chiave più bassa alla chiave più alta.</span><span class="sxs-lookup"><span data-stu-id="77c5d-139">If set, the application expects this table to be cleaned up in sequential order, from lowest key to highest key.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="77c5d-140">**ulMaintDensity**</span><span class="sxs-lookup"><span data-stu-id="77c5d-140">**ulMaintDensity**</span></span>

<span data-ttu-id="77c5d-141">densità per mulMaintDensity</span><span class="sxs-lookup"><span data-stu-id="77c5d-141">density to mulMaintDensity</span></span>

<span data-ttu-id="77c5d-142">Densità da gestire all'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="77c5d-142">Density to maintain at.</span></span> <span data-ttu-id="77c5d-143">Se gli hint di spazio specificano JET_bitRetrieveHintTableScanForward o JET_bitRetrieveHintTableScanBackward, la deframmentazione della tabella verrà attivata quando lo spazio utilizzato nella tabella scende al di sotto di questa soglia.</span><span class="sxs-lookup"><span data-stu-id="77c5d-143">If the space hints specify JET_bitRetrieveHintTableScanForward or JET_bitRetrieveHintTableScanBackward, table defragmentation will be triggered when the used space in the table drops below this threshold.</span></span> <span data-ttu-id="77c5d-144">La deframmentazione della tabella può essere disabilitata impostando questo membro su zero.</span><span class="sxs-lookup"><span data-stu-id="77c5d-144">Table defragmentation can be disabled by setting this member to zero.</span></span> <span data-ttu-id="77c5d-145">Se si imposta questo membro su 100, la deframmentazione della tabella verrà eseguita non appena viene liberata una pagina.</span><span class="sxs-lookup"><span data-stu-id="77c5d-145">Setting this member to 100 will cause table defragmentation to run as soon as a page is freed.</span></span>

<span data-ttu-id="77c5d-146">**ulGrowth**</span><span class="sxs-lookup"><span data-stu-id="77c5d-146">**ulGrowth**</span></span>

<span data-ttu-id="77c5d-147">Percentuale di incremento rispetto all'ultimo aumento o alla dimensione iniziale, arrotondata alle dimensioni di allocazione del JET nativo più vicine.</span><span class="sxs-lookup"><span data-stu-id="77c5d-147">The percent growth from the last growth or initial size, rounded to nearest native JET allocation size.</span></span>

<span data-ttu-id="77c5d-148">**cbMinExtent troppo piccola**</span><span class="sxs-lookup"><span data-stu-id="77c5d-148">**cbMinExtent too small**</span></span>

<span data-ttu-id="77c5d-149">Viene eseguito l'override di ulGrowth se è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="77c5d-149">This overrides ulGrowth if too small.</span></span>

<span data-ttu-id="77c5d-150">**cbMaxExtent**</span><span class="sxs-lookup"><span data-stu-id="77c5d-150">**cbMaxExtent**</span></span>

<span data-ttu-id="77c5d-151">Valore massimo per la crescita in byte.</span><span class="sxs-lookup"><span data-stu-id="77c5d-151">The maximum value for growth in bytes.</span></span> <span data-ttu-id="77c5d-152">Questo ulGrowth Caps.</span><span class="sxs-lookup"><span data-stu-id="77c5d-152">This caps ulGrowth.</span></span>

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a><span data-ttu-id="77c5d-153">Quando un albero b aumenta attraverso le divisioni di accodamento o Hotpoint (in contrapposizione agli inserimenti di record casuali), la quantità di spazio che la tabella aumenterà è calcolata come segue:</span><span class="sxs-lookup"><span data-stu-id="77c5d-153">When a b-tree grows through append or hotpoint splits (as opposed to random record insertions), the amount of space the table will grow by is calculated as follows:</span></span>

1.  <span data-ttu-id="77c5d-154">Al momento della creazione, viene fornito il cbInitial dell'albero b, sempre.</span><span class="sxs-lookup"><span data-stu-id="77c5d-154">At creation, we give the b-tree cbInitial, always.</span></span>

2.  <span data-ttu-id="77c5d-155">Durante la prima allocazione di una determinata area, si essegnerà: cbInitial \* ulGrowth/100 (arrotondato alle dimensioni di pagina del database) o cbMinExtent se più grande.</span><span class="sxs-lookup"><span data-stu-id="77c5d-155">During the first allocation of a given area, we will allocate: cbInitial \* ulGrowth / 100 (rounded to the DB's page size), or cbMinExtent if larger.</span></span>

3.  <span data-ttu-id="77c5d-156">Durante l'allocazione successiva, cbLastAlloc \* ulGrowth/100 (arrotondato alle dimensioni di pagina del database) o cbMinExtent se più grande.</span><span class="sxs-lookup"><span data-stu-id="77c5d-156">During the next allocation, cbLastAlloc \* ulGrowth / 100 (rounded to the page size of the DB), or cbMinExtent if larger.</span></span>

4.  <span data-ttu-id="77c5d-157">A una certa allocazione (che potrebbe essere la prima allocazione), le dimensioni calcolate supereranno cbMaxExtent e la dimensione di crescita sarà successiva.</span><span class="sxs-lookup"><span data-stu-id="77c5d-157">At some allocation (which could be the first allocation), the calculated size will exceed cbMaxExtent, and that will be the growth size thereafter.</span></span>

### <a name="requirements"></a><span data-ttu-id="77c5d-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77c5d-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77c5d-159"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="77c5d-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="77c5d-160">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="77c5d-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77c5d-161"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="77c5d-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="77c5d-162">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="77c5d-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="77c5d-163"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="77c5d-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="77c5d-164">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="77c5d-164">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="77c5d-165">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="77c5d-165">See Also</span></span>

[<span data-ttu-id="77c5d-166">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="77c5d-166">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="77c5d-167">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="77c5d-167">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)
