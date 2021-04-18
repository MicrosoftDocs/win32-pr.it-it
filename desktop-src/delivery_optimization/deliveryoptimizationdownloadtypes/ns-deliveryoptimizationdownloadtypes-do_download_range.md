---
title: Struttura DO_DOWNLOAD_RANGE
description: Identifica un singolo intervallo di byte da scaricare da un file.
keywords:
- Struttura DO_DOWNLOAD_RANGE
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "106299309"
---
# <a name="do_download_range-structure"></a><span data-ttu-id="f6c2d-104">Struttura DO_DOWNLOAD_RANGE</span><span class="sxs-lookup"><span data-stu-id="f6c2d-104">DO_DOWNLOAD_RANGE structure</span></span>

<span data-ttu-id="f6c2d-105">La struttura **DO_DOWNLOAD_RANGE** identifica un singolo intervallo di byte da scaricare da un file.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-105">The **DO_DOWNLOAD_RANGE** structure identifies a single range of bytes to download from a file.</span></span> <span data-ttu-id="f6c2d-106">La struttura **DO_DOWNLOAD_RANGE** è inclusa nella struttura **DO_DOWNLOAD_RANGES_INFO** per fornire una matrice di intervalli da scaricare.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-106">The **DO_DOWNLOAD_RANGE** structure is included within **DO_DOWNLOAD_RANGES_INFO** structure to provide an array of ranges to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c2d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f6c2d-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a><span data-ttu-id="f6c2d-108">Members</span><span class="sxs-lookup"><span data-stu-id="f6c2d-108">Members</span></span>

`Offset`

<span data-ttu-id="f6c2d-109">Offset in base zero all'inizio dell'intervallo di byte da scaricare da un file.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

`Length`

<span data-ttu-id="f6c2d-110">Lunghezza dell'intervallo, in byte.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-110">The length of the range, in bytes.</span></span> <span data-ttu-id="f6c2d-111">Non specificare una lunghezza pari a zero byte.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-111">Do not specify a zero-byte length.</span></span> <span data-ttu-id="f6c2d-112">Per indicare che l'intervallo si estende fino alla fine del file, specificare **DO_LENGTH_TO_EOF**.</span><span class="sxs-lookup"><span data-stu-id="f6c2d-112">To indicate that the range extends to the end of the file, specify **DO_LENGTH_TO_EOF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6c2d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6c2d-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f6c2d-114">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="f6c2d-114">**Minimum supported client**</span></span> | <span data-ttu-id="f6c2d-115">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6c2d-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="f6c2d-116">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="f6c2d-116">**Minimum supported server**</span></span> | <span data-ttu-id="f6c2d-117">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="f6c2d-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="f6c2d-118">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="f6c2d-118">**Header**</span></span> | <span data-ttu-id="f6c2d-119">DeliveryOptimizationDownloadTypes. h</span><span class="sxs-lookup"><span data-stu-id="f6c2d-119">DeliveryOptimizationDownloadTypes.h</span></span> |
