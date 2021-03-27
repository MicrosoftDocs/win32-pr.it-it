---
description: Contiene informazioni sull'unità selezionata nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).
title: Struttura FMS_GETDRIVEINFO (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: b19b54d89f74fa122effa5853beb2961e0ddf1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979698"
---
# <a name="fms_getdriveinfo-structure"></a><span data-ttu-id="23abd-103">\_Struttura GETDRIVEINFO FMS</span><span class="sxs-lookup"><span data-stu-id="23abd-103">FMS\_GETDRIVEINFO structure</span></span>

<span data-ttu-id="23abd-104">Contiene informazioni sull'unità selezionata nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).</span><span class="sxs-lookup"><span data-stu-id="23abd-104">Contains information about the drive selected in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="23abd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23abd-105">Syntax</span></span>


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a><span data-ttu-id="23abd-106">Members</span><span class="sxs-lookup"><span data-stu-id="23abd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="23abd-107">**dwTotalSpace**</span><span class="sxs-lookup"><span data-stu-id="23abd-107">**dwTotalSpace**</span></span>
</dt> <dd>

<span data-ttu-id="23abd-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="23abd-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="23abd-109">Quantità totale di spazio di archiviazione, in byte, sul disco associato all'unità.</span><span class="sxs-lookup"><span data-stu-id="23abd-109">The total amount of storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="23abd-110">**dwFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="23abd-110">**dwFreeSpace**</span></span>
</dt> <dd>

<span data-ttu-id="23abd-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="23abd-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="23abd-112">Quantità di spazio di archiviazione disponibile, in byte, sul disco associato all'unità.</span><span class="sxs-lookup"><span data-stu-id="23abd-112">The amount of free storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="23abd-113">**szPath**</span><span class="sxs-lookup"><span data-stu-id="23abd-113">**szPath**</span></span>
</dt> <dd>

<span data-ttu-id="23abd-114">Tipo: **TCHAR \[ 260 \]**</span><span class="sxs-lookup"><span data-stu-id="23abd-114">Type: **TCHAR\[260\]**</span></span>

</dd> <dd>

<span data-ttu-id="23abd-115">percorso con terminazione null della directory corrente.</span><span class="sxs-lookup"><span data-stu-id="23abd-115">the null-terminated path of the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="23abd-116">**szVolume**</span><span class="sxs-lookup"><span data-stu-id="23abd-116">**szVolume**</span></span>
</dt> <dd>

<span data-ttu-id="23abd-117">Tipo: **TCHAR \[ 14 \]**</span><span class="sxs-lookup"><span data-stu-id="23abd-117">Type: **TCHAR\[14\]**</span></span>

</dd> <dd>

<span data-ttu-id="23abd-118">Etichetta del volume con terminazione null del disco associato all'unità.</span><span class="sxs-lookup"><span data-stu-id="23abd-118">The null-terminated volume label of the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="23abd-119">**szShare**</span><span class="sxs-lookup"><span data-stu-id="23abd-119">**szShare**</span></span>
</dt> <dd>

<span data-ttu-id="23abd-120">Tipo: **TCHAR \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="23abd-120">Type: **TCHAR\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="23abd-121">Nome con terminazione null della risorsa di rete (se l'unità è accessibile tramite una rete).</span><span class="sxs-lookup"><span data-stu-id="23abd-121">The null-terminated name of the network resource (if the drive is being accessed through a network).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23abd-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23abd-122">Requirements</span></span>



| <span data-ttu-id="23abd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="23abd-123">Requirement</span></span> | <span data-ttu-id="23abd-124">Valore</span><span class="sxs-lookup"><span data-stu-id="23abd-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23abd-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23abd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="23abd-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="23abd-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="23abd-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23abd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="23abd-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="23abd-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="23abd-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23abd-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="23abd-130"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="23abd-130"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23abd-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23abd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23abd-132">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="23abd-132">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="23abd-133">**\_GETDRIVEINFO FM**</span><span class="sxs-lookup"><span data-stu-id="23abd-133">**FM\_GETDRIVEINFO**</span></span>](fm-getdriveinfo.md)
</dt> </dl>

 

 




