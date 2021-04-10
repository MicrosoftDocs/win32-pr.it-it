---
description: 'Altre informazioni su: JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: 5d1d4fa75c8a41528e9868bc94fa638042d01cff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225883"
---
# <a name="jet_snt"></a><span data-ttu-id="600c3-103">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="600c3-103">JET_SNT</span></span>


<span data-ttu-id="600c3-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="600c3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snt"></a><span data-ttu-id="600c3-105">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="600c3-105">JET_SNT</span></span>

<span data-ttu-id="600c3-106">Il gruppo [JET_SNT]() di costanti descrive i punti dello stato di avanzamento di un'operazione su cui vengono richieste informazioni in una chiamata alla funzione di callback di [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="600c3-106">The [JET_SNT]() group of constants describe the points of the progress of an operation about which information is requested in a call to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="600c3-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="600c3-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="600c3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="600c3-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="600c3-109">JET_sntBegin</span><span class="sxs-lookup"><span data-stu-id="600c3-109">JET_sntBegin</span></span><br />
<span data-ttu-id="600c3-110">5</span><span class="sxs-lookup"><span data-stu-id="600c3-110">5</span></span></p></td>
<td><p><span data-ttu-id="600c3-111">Inizio di un'operazione</span><span class="sxs-lookup"><span data-stu-id="600c3-111">The beginning of an operation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="600c3-112">JET_sntRequirements</span><span class="sxs-lookup"><span data-stu-id="600c3-112">JET_sntRequirements</span></span><br />
<span data-ttu-id="600c3-113">7</span><span class="sxs-lookup"><span data-stu-id="600c3-113">7</span></span></p></td>
<td><p><span data-ttu-id="600c3-114">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="600c3-114">Not supported.</span></span></p>
<p><span data-ttu-id="600c3-115"><strong>Server Windows 2000:</strong>  L'operazione è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="600c3-115"><strong>Windows 2000 Server:</strong>  The operation is started.</span></span> <span data-ttu-id="600c3-116">In questo caso, l'ultimo parametro della funzione di callback deve essere un puntatore valido a una struttura <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> che indica il numero totale di unità da eseguire.</span><span class="sxs-lookup"><span data-stu-id="600c3-116">In this case, the last parameter of the callback function should be a valid pointer to a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure indicating the total number of units to be executed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="600c3-117">JET_sntProgress</span><span class="sxs-lookup"><span data-stu-id="600c3-117">JET_sntProgress</span></span><br />
<span data-ttu-id="600c3-118">0</span><span class="sxs-lookup"><span data-stu-id="600c3-118">0</span></span></p></td>
<td><p><span data-ttu-id="600c3-119">Il numero di unità completate e il numero di unità ancora da eseguire.</span><span class="sxs-lookup"><span data-stu-id="600c3-119">The number of units completed and number of units yet to be done.</span></span> <span data-ttu-id="600c3-120">Queste informazioni vengono restituite nei membri di una struttura <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> .</span><span class="sxs-lookup"><span data-stu-id="600c3-120">This information is returned in the members of a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="600c3-121">JET_sntComplete</span><span class="sxs-lookup"><span data-stu-id="600c3-121">JET_sntComplete</span></span><br />
<span data-ttu-id="600c3-122">6</span><span class="sxs-lookup"><span data-stu-id="600c3-122">6</span></span></p></td>
<td><p><span data-ttu-id="600c3-123">Il completamento di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="600c3-123">The completion of an operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="600c3-124">JET_sntFail</span><span class="sxs-lookup"><span data-stu-id="600c3-124">JET_sntFail</span></span><br />
<span data-ttu-id="600c3-125">3</span><span class="sxs-lookup"><span data-stu-id="600c3-125">3</span></span></p></td>
<td><p><span data-ttu-id="600c3-126">Errore di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="600c3-126">The failure of an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="600c3-127">JET_sntRecoveryStep</span><span class="sxs-lookup"><span data-stu-id="600c3-127">JET_sntRecoveryStep</span></span><br />
<span data-ttu-id="600c3-128">8</span><span class="sxs-lookup"><span data-stu-id="600c3-128">8</span></span></p></td>
<td><p><span data-ttu-id="600c3-129">Controllo di recupero di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="600c3-129">The recovery control of an operation.</span></span></p>
<div class="alert">

> [!NOTE]
> <P><span data-ttu-id="600c3-130">Questo valore non è applicabile alle versioni del sistema operativo Windows a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="600c3-130">This value is not applicable to versions of the Windows operating system starting with Windows 8.</span></span></P>


</div></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="600c3-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="600c3-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="600c3-132"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="600c3-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="600c3-133">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="600c3-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="600c3-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="600c3-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="600c3-135">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="600c3-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="600c3-136"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="600c3-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="600c3-137">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="600c3-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="600c3-138">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="600c3-138">See Also</span></span>

[<span data-ttu-id="600c3-139">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="600c3-139">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="600c3-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="600c3-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="600c3-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="600c3-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)
