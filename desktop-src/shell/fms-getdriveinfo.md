---
description: Contiene informazioni sull'unità selezionata nella finestra di Gestione file attiva (la finestra della directory o la finestra Risultati ricerca).
title: FMS_GETDRIVEINFO (Wfext.h)
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
ms.openlocfilehash: 107e12e1076a2fc928ecb9b578ab01d64898a83a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842232"
---
# <a name="fms_getdriveinfo-structure"></a><span data-ttu-id="7a585-103">Struttura \_ FMS GETDRIVEINFO</span><span class="sxs-lookup"><span data-stu-id="7a585-103">FMS\_GETDRIVEINFO structure</span></span>

<span data-ttu-id="7a585-104">Contiene informazioni sull'unità selezionata nella finestra di Gestione file attiva (la finestra della directory o la finestra Risultati ricerca).</span><span class="sxs-lookup"><span data-stu-id="7a585-104">Contains information about the drive selected in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a585-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a585-105">Syntax</span></span>


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a><span data-ttu-id="7a585-106">Members</span><span class="sxs-lookup"><span data-stu-id="7a585-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a585-107">**dwTotalSpace**</span><span class="sxs-lookup"><span data-stu-id="7a585-107">**dwTotalSpace**</span></span>
</dt> <dd>

<span data-ttu-id="7a585-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7a585-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7a585-109">Quantità totale di spazio di archiviazione, in byte, sul disco associato all'unità.</span><span class="sxs-lookup"><span data-stu-id="7a585-109">The total amount of storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="7a585-110">**dwFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="7a585-110">**dwFreeSpace**</span></span>
</dt> <dd>

<span data-ttu-id="7a585-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="7a585-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="7a585-112">Quantità di spazio di archiviazione disponibile, in byte, sul disco associato all'unità.</span><span class="sxs-lookup"><span data-stu-id="7a585-112">The amount of free storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="7a585-113">**szPath**</span><span class="sxs-lookup"><span data-stu-id="7a585-113">**szPath**</span></span>
</dt> <dd>

<span data-ttu-id="7a585-114">Tipo: **TCHAR \[ 260 \]**</span><span class="sxs-lookup"><span data-stu-id="7a585-114">Type: **TCHAR\[260\]**</span></span>

</dd> <dd>

<span data-ttu-id="7a585-115">Percorso con terminazione Null della directory corrente.</span><span class="sxs-lookup"><span data-stu-id="7a585-115">the null-terminated path of the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="7a585-116">**szVolume**</span><span class="sxs-lookup"><span data-stu-id="7a585-116">**szVolume**</span></span>
</dt> <dd>

<span data-ttu-id="7a585-117">Tipo: **TCHAR \[ 14 \]**</span><span class="sxs-lookup"><span data-stu-id="7a585-117">Type: **TCHAR\[14\]**</span></span>

</dd> <dd>

<span data-ttu-id="7a585-118">Etichetta del volume con terminazione Null del disco associato all'unità.</span><span class="sxs-lookup"><span data-stu-id="7a585-118">The null-terminated volume label of the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="7a585-119">**szShare**</span><span class="sxs-lookup"><span data-stu-id="7a585-119">**szShare**</span></span>
</dt> <dd>

<span data-ttu-id="7a585-120">Tipo: **TCHAR \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="7a585-120">Type: **TCHAR\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="7a585-121">Nome con terminazione Null della risorsa di rete (se l'accesso all'unità avviene tramite una rete).</span><span class="sxs-lookup"><span data-stu-id="7a585-121">The null-terminated name of the network resource (if the drive is being accessed through a network).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a585-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a585-122">Requirements</span></span>



| <span data-ttu-id="7a585-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a585-123">Requirement</span></span> | <span data-ttu-id="7a585-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7a585-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a585-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a585-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7a585-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7a585-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7a585-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a585-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7a585-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7a585-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7a585-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a585-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a585-130"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="7a585-130"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a585-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a585-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a585-132">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="7a585-132">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="7a585-133">**FM \_ GETDRIVEINFO**</span><span class="sxs-lookup"><span data-stu-id="7a585-133">**FM\_GETDRIVEINFO**</span></span>](fm-getdriveinfo.md)
</dt> </dl>

 

 




