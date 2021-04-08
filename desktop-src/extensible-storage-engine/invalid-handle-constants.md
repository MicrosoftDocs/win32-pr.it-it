---
description: 'Altre informazioni su: costanti handle non valide'
title: Costanti handle non valide
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: f5614b36acfca8b5be4c13849d459d25f984336a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058160"
---
# <a name="invalid-handle-constants"></a><span data-ttu-id="85c28-103">Costanti handle non valide</span><span class="sxs-lookup"><span data-stu-id="85c28-103">Invalid Handle Constants</span></span>


<span data-ttu-id="85c28-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="85c28-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="invalid-handle-constants"></a><span data-ttu-id="85c28-105">Costanti handle non valide</span><span class="sxs-lookup"><span data-stu-id="85c28-105">Invalid Handle Constants</span></span>

<span data-ttu-id="85c28-106">Le costanti seguenti indicano handle non validi per diversi aspetti di ESE.</span><span class="sxs-lookup"><span data-stu-id="85c28-106">The following constants indicate invalid handles for different aspects of ESE.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85c28-107">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="85c28-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="85c28-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85c28-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85c28-109">JET_instanceNil</span><span class="sxs-lookup"><span data-stu-id="85c28-109">JET_instanceNil</span></span><br />
<span data-ttu-id="85c28-110">(~ (JET_INSTANCE) 0)</span><span class="sxs-lookup"><span data-stu-id="85c28-110">(~(JET_INSTANCE)0)</span></span></p></td>
<td><p><span data-ttu-id="85c28-111">Handle non valido per un'istanza di database.</span><span class="sxs-lookup"><span data-stu-id="85c28-111">An invalid handle for a database instance.</span></span><br /><span data-ttu-id="85c28-112">
<strong>Windows XP:</strong> Introdotta in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="85c28-112">
<strong>Windows XP:</strong> Introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85c28-113">JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="85c28-113">JET_sesidNil</span></span><br />
<span data-ttu-id="85c28-114">(~ (JET_SESID) 0)</span><span class="sxs-lookup"><span data-stu-id="85c28-114">(~(JET_SESID)0)</span></span></p></td>
<td><p><span data-ttu-id="85c28-115">Handle non valido per un ID di sessione.</span><span class="sxs-lookup"><span data-stu-id="85c28-115">An invalid handle for a session ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85c28-116">JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="85c28-116">JET_tableidNil</span></span><br />
<span data-ttu-id="85c28-117">(~ (JET_TABLEID) 0)</span><span class="sxs-lookup"><span data-stu-id="85c28-117">(~(JET_TABLEID)0)</span></span></p></td>
<td><p><span data-ttu-id="85c28-118">Handle non valido per un ID tabella.</span><span class="sxs-lookup"><span data-stu-id="85c28-118">An invalid handle for a table ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85c28-119">JET_bitNil</span><span class="sxs-lookup"><span data-stu-id="85c28-119">JET_bitNil</span></span><br />
<span data-ttu-id="85c28-120">((JET_GRBIT) 0)</span><span class="sxs-lookup"><span data-stu-id="85c28-120">((JET_GRBIT)0)</span></span></p></td>
<td><p><span data-ttu-id="85c28-121">Handle non valido per un gruppo di bit.</span><span class="sxs-lookup"><span data-stu-id="85c28-121">An invalid handle for a group of bits.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85c28-122">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="85c28-122">JET_LSNil</span></span><br />
<span data-ttu-id="85c28-123">(~ (JET_LS) 0)</span><span class="sxs-lookup"><span data-stu-id="85c28-123">(~(JET_LS)0)</span></span></p></td>
<td><p><span data-ttu-id="85c28-124">Handle non valido per l'archiviazione locale.</span><span class="sxs-lookup"><span data-stu-id="85c28-124">An invalid handle for the Local Storage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85c28-125">JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="85c28-125">JET_dbidNil</span></span><br />
<span data-ttu-id="85c28-126">((JET_DBID) 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="85c28-126">((JET_DBID) 0xFFFFFFFF)</span></span></p></td>
<td><p><span data-ttu-id="85c28-127">Handle non valido per l'ID del database.</span><span class="sxs-lookup"><span data-stu-id="85c28-127">An invalid handle for the database ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="85c28-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85c28-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85c28-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="85c28-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="85c28-130">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="85c28-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85c28-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="85c28-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="85c28-132">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="85c28-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85c28-133"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="85c28-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="85c28-134">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="85c28-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

