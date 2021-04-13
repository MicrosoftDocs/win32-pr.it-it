---
title: Struttura DO_DOWNLOAD_RANGE_INFO
description: Identifica una matrice di intervalli di byte da scaricare da un file.
keywords:
- Struttura DO_DOWNLOAD_RANGE_INFO
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104398352"
---
# <a name="do_download_range_info-structure"></a><span data-ttu-id="e9f19-104">Struttura DO_DOWNLOAD_RANGE_INFO</span><span class="sxs-lookup"><span data-stu-id="e9f19-104">DO_DOWNLOAD_RANGE_INFO structure</span></span>

<span data-ttu-id="e9f19-105">La struttura **DO_DOWNLOAD_RANGE_INFO** identifica una matrice di intervalli di byte da scaricare da un file.</span><span class="sxs-lookup"><span data-stu-id="e9f19-105">The **DO_DOWNLOAD_RANGE_INFO** structure identifies an array of ranges of bytes to download from a file.</span></span> <span data-ttu-id="e9f19-106">Viene in genere passato come argomento facoltativo alla funzione **IDODownload:: Start** .</span><span class="sxs-lookup"><span data-stu-id="e9f19-106">It is typically passed as an optional argument to the **IDODownload::Start** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f19-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9f19-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a><span data-ttu-id="e9f19-108">Members</span><span class="sxs-lookup"><span data-stu-id="e9f19-108">Members</span></span>

`RangeCount`

<span data-ttu-id="e9f19-109">Numero di elementi negli intervalli.</span><span class="sxs-lookup"><span data-stu-id="e9f19-109">Number of elements in Ranges.</span></span>

`Ranges`

<span data-ttu-id="e9f19-110">Matrice di una o più strutture di **DO_DOWNLOAD_RANGE** che specificano gli intervalli da scaricare.</span><span class="sxs-lookup"><span data-stu-id="e9f19-110">Array of one or more **DO_DOWNLOAD_RANGE** structures that specify the ranges to download.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f19-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9f19-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e9f19-112">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="e9f19-112">**Minimum supported client**</span></span> | <span data-ttu-id="e9f19-113">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9f19-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e9f19-114">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="e9f19-114">**Minimum supported server**</span></span> | <span data-ttu-id="e9f19-115">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="e9f19-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e9f19-116">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="e9f19-116">**Header**</span></span> | <span data-ttu-id="e9f19-117">Do. h</span><span class="sxs-lookup"><span data-stu-id="e9f19-117">Do.h</span></span> |
