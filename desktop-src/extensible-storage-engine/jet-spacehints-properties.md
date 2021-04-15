---
description: 'Altre informazioni su: Proprietà JET_SPACEHINTS'
title: Proprietà JET_SPACEHINTS
TOCTitle: JET_SPACEHINTS properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SPACEHINTS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_spacehints_properties(v=EXCHG.10)
ms:contentKeyID: 55103923
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f361e0a1fbcf8057ae900e57846cce8457489398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556212"
---
# <a name="jet_spacehints-properties"></a><span data-ttu-id="b6944-103">Proprietà JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="b6944-103">JET_SPACEHINTS properties</span></span>

<span data-ttu-id="b6944-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="b6944-104">Include protected members</span></span>  
<span data-ttu-id="b6944-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="b6944-105">Include inherited members</span></span>  

<span data-ttu-id="b6944-106">Il tipo di [JET_SPACEHINTS](./jet-spacehints-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="b6944-106">The [JET_SPACEHINTS](./jet-spacehints-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="b6944-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b6944-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b6944-108">Nome</span><span class="sxs-lookup"><span data-stu-id="b6944-108">Name</span></span></th>
<th><span data-ttu-id="b6944-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6944-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b6944-111"><a href="dn351103(v=exchg.10).md">cbInitial</a></span><span class="sxs-lookup"><span data-stu-id="b6944-111"><a href="dn351103(v=exchg.10).md">cbInitial</a></span></span></td>
<td><span data-ttu-id="b6944-112">Ottiene o imposta le dimensioni iniziali (in byte).</span><span class="sxs-lookup"><span data-stu-id="b6944-112">Gets or sets the initial size (in bytes).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b6944-114"><a href="dn351105(v=exchg.10).md">cbMaxExtent</a></span><span class="sxs-lookup"><span data-stu-id="b6944-114"><a href="dn351105(v=exchg.10).md">cbMaxExtent</a></span></span></td>
<td><span data-ttu-id="b6944-115">Ottiene o imposta il valore che imposta il limite massimo di ulGrowth.</span><span class="sxs-lookup"><span data-stu-id="b6944-115">Gets or sets the value that sets the ceiling of ulGrowth.</span></span> <span data-ttu-id="b6944-116">Questo valore è in byte.</span><span class="sxs-lookup"><span data-stu-id="b6944-116">This value is in bytes.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b6944-118"><a href="dn351104(v=exchg.10).md">cbMinExtent</a></span><span class="sxs-lookup"><span data-stu-id="b6944-118"><a href="dn351104(v=exchg.10).md">cbMinExtent</a></span></span></td>
<td><span data-ttu-id="b6944-119">Ottiene o imposta il valore che esegue l'override di ulGrowth se troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="b6944-119">Gets or sets the value that overrides ulGrowth if too small.</span></span> <span data-ttu-id="b6944-120">Questo valore è in byte.</span><span class="sxs-lookup"><span data-stu-id="b6944-120">This value is in bytes.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b6944-122"><a href="dn351068(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="b6944-122"><a href="dn351068(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="b6944-123">Ottiene o imposta le opzioni degli hint di spazio.</span><span class="sxs-lookup"><span data-stu-id="b6944-123">Gets or sets the space hints options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b6944-125"><a href="dn351069(v=exchg.10).md">ulGrowth</a></span><span class="sxs-lookup"><span data-stu-id="b6944-125"><a href="dn351069(v=exchg.10).md">ulGrowth</a></span></span></td>
<td><span data-ttu-id="b6944-126">Ottiene o imposta la percentuale di crescita dall'ultima crescita o dalle dimensioni iniziali (probabilmente arrotondate alle dimensioni di allocazione del JET nativo più vicine).</span><span class="sxs-lookup"><span data-stu-id="b6944-126">Gets or sets the percent growth from last growth or initial size (possibly rounded to nearest native JET allocation size).</span></span> <span data-ttu-id="b6944-127">I valori validi sono 0 e [100, 50000).</span><span class="sxs-lookup"><span data-stu-id="b6944-127">Valid values are 0, and [100, 50000).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b6944-129"><a href="dn351070(v=exchg.10).md">ulInitialDensity</a></span><span class="sxs-lookup"><span data-stu-id="b6944-129"><a href="dn351070(v=exchg.10).md">ulInitialDensity</a></span></span></td>
<td><span data-ttu-id="b6944-130">Ottiene o imposta la densità in corrispondenza del layout (Accodamento).</span><span class="sxs-lookup"><span data-stu-id="b6944-130">Gets or sets the density at (append) layout.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="b6944-132"><a href="dn351071(v=exchg.10).md">ulMaintDensity</a></span><span class="sxs-lookup"><span data-stu-id="b6944-132"><a href="dn351071(v=exchg.10).md">ulMaintDensity</a></span></span></td>
<td><span data-ttu-id="b6944-133">Ottiene o imposta la densità da mantenere.</span><span class="sxs-lookup"><span data-stu-id="b6944-133">Gets or sets the density at which to maintain.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b6944-134">Inizio</span><span class="sxs-lookup"><span data-stu-id="b6944-134">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="b6944-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6944-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b6944-136">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b6944-136">Reference</span></span>

[<span data-ttu-id="b6944-137">Classe JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="b6944-137">JET_SPACEHINTS class</span></span>](./jet-spacehints-class.md)

[<span data-ttu-id="b6944-138">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b6944-138">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
