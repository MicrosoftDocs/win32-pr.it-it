---
description: 'Altre informazioni su: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: 35ffb2d17c01c3d157fc7ed66a320529f844ff9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305770"
---
# <a name="jet_snp"></a><span data-ttu-id="9be08-103">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="9be08-103">JET_SNP</span></span>


<span data-ttu-id="9be08-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9be08-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snp"></a><span data-ttu-id="9be08-105">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="9be08-105">JET_SNP</span></span>

<span data-ttu-id="9be08-106">Il **JET_SNP** gruppo di costanti descrive il tipo di operazione per cui è necessario ottenere informazioni sullo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="9be08-106">The **JET_SNP** group of constants describe the type of the operation for which progress information is to be obtained.</span></span> <span data-ttu-id="9be08-107">Queste costanti vengono usate come parametro *SNP* della funzione di callback [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="9be08-107">These constants are used as the *snp* parameter of the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9be08-108">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="9be08-108">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="9be08-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9be08-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9be08-110">JET_snpRepair</span><span class="sxs-lookup"><span data-stu-id="9be08-110">JET_snpRepair</span></span><br />
<span data-ttu-id="9be08-111">2</span><span class="sxs-lookup"><span data-stu-id="9be08-111">2</span></span></p></td>
<td><p><span data-ttu-id="9be08-112">Il callback è per un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9be08-112">The callback is for a repair operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9be08-113">JET_snpCompact</span><span class="sxs-lookup"><span data-stu-id="9be08-113">JET_snpCompact</span></span><br />
<span data-ttu-id="9be08-114">4</span><span class="sxs-lookup"><span data-stu-id="9be08-114">4</span></span></p></td>
<td><p><span data-ttu-id="9be08-115">Il callback è per la deframmentazione del database.</span><span class="sxs-lookup"><span data-stu-id="9be08-115">The callback is for database defragmentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9be08-116">JET_snpRestore</span><span class="sxs-lookup"><span data-stu-id="9be08-116">JET_snpRestore</span></span><br />
<span data-ttu-id="9be08-117">8</span><span class="sxs-lookup"><span data-stu-id="9be08-117">8</span></span></p></td>
<td><p><span data-ttu-id="9be08-118">Il callback è per un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9be08-118">The callback is for a restore operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9be08-119">JET_snpBackup</span><span class="sxs-lookup"><span data-stu-id="9be08-119">JET_snpBackup</span></span><br />
<span data-ttu-id="9be08-120">9</span><span class="sxs-lookup"><span data-stu-id="9be08-120">9</span></span></p></td>
<td><p><span data-ttu-id="9be08-121">Il callback è per un'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="9be08-121">The callback is for a backup operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9be08-122">JET_snpUpgrade</span><span class="sxs-lookup"><span data-stu-id="9be08-122">JET_snpUpgrade</span></span><br />
<span data-ttu-id="9be08-123">10</span><span class="sxs-lookup"><span data-stu-id="9be08-123">10</span></span></p></td>
<td><p><span data-ttu-id="9be08-124">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="9be08-124">Not supported.</span></span></p>
<p><span data-ttu-id="9be08-125"><strong>Windows 2000:</strong>  Il callback è per l'operazione di aggiornamento del formato del database.</span><span class="sxs-lookup"><span data-stu-id="9be08-125"><strong>Windows 2000:</strong>  The callback is for the database format upgrade operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9be08-126">JET_snpScrub</span><span class="sxs-lookup"><span data-stu-id="9be08-126">JET_snpScrub</span></span><br />
<span data-ttu-id="9be08-127">11</span><span class="sxs-lookup"><span data-stu-id="9be08-127">11</span></span></p></td>
<td><p><span data-ttu-id="9be08-128">Il callback è per un'operazione di azzeramento del database (ovvero, pulitura).</span><span class="sxs-lookup"><span data-stu-id="9be08-128">The callback is for a database zeroing (that is, scrubbing) operation.</span></span></p>
<p><span data-ttu-id="9be08-129"><strong>Windows server 2003 e windows 2000 Server:</strong>  Non supportato.</span><span class="sxs-lookup"><span data-stu-id="9be08-129"><strong>Windows Server 2003 and Windows 2000 Server:</strong>  Not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9be08-130">JET_snpUpgradeRecordFormat</span><span class="sxs-lookup"><span data-stu-id="9be08-130">JET_snpUpgradeRecordFormat</span></span><br />
<span data-ttu-id="9be08-131">12</span><span class="sxs-lookup"><span data-stu-id="9be08-131">12</span></span></p></td>
<td><p><span data-ttu-id="9be08-132">Il callback è per il processo di aggiornamento del formato di record di tutte le pagine del database.</span><span class="sxs-lookup"><span data-stu-id="9be08-132">The callback is for the process of upgrading the record format of all database pages.</span></span></p>
<p><span data-ttu-id="9be08-133"><strong>Windows server 2003 e windows 2000 Server:</strong>  Non supportato.</span><span class="sxs-lookup"><span data-stu-id="9be08-133"><strong>Windows Server 2003 and Windows 2000 Server:</strong>  Not supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="9be08-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9be08-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9be08-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="9be08-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9be08-136">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="9be08-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9be08-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9be08-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9be08-138">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="9be08-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9be08-139"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="9be08-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9be08-140">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="9be08-140">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="9be08-141">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9be08-141">See Also</span></span>

[<span data-ttu-id="9be08-142">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="9be08-142">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="9be08-143">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="9be08-143">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="9be08-144">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="9be08-144">JET_SNT</span></span>](./jet-snt.md)
