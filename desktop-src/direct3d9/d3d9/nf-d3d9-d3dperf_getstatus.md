---
title: Funzione D3DPERF_GetStatus
description: Determinare lo stato corrente del Profiler dal programma di destinazione.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "104336585"
---
# <a name="d3dperf_getstatus-function"></a><span data-ttu-id="7f0e8-103">Funzione D3DPERF_GetStatus</span><span class="sxs-lookup"><span data-stu-id="7f0e8-103">D3DPERF_GetStatus function</span></span>

<span data-ttu-id="7f0e8-104">Determinare lo stato corrente del Profiler dal programma di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7f0e8-104">Determine the current state of the profiler from the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f0e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f0e8-105">Syntax</span></span>

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a><span data-ttu-id="7f0e8-106">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f0e8-106">Return value</span></span>

<span data-ttu-id="7f0e8-107">Valore diverso da zero quando PIX sta profilando il programma di destinazione; in caso contrario, zero.</span><span class="sxs-lookup"><span data-stu-id="7f0e8-107">A non-zero value when PIX is profiling the target program; otherwise, zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f0e8-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f0e8-108">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7f0e8-109">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="7f0e8-109">**Target Platform**</span></span> | <span data-ttu-id="7f0e8-110">Windows</span><span class="sxs-lookup"><span data-stu-id="7f0e8-110">Windows</span></span> |
| <span data-ttu-id="7f0e8-111">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="7f0e8-111">**Header**</span></span> | <span data-ttu-id="7f0e8-112">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="7f0e8-112">d3d9.h</span></span> |
| <span data-ttu-id="7f0e8-113">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="7f0e8-113">**Library**</span></span> | <span data-ttu-id="7f0e8-114">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="7f0e8-114">d3d9.lib</span></span> |
| <span data-ttu-id="7f0e8-115">**DLL**</span><span class="sxs-lookup"><span data-stu-id="7f0e8-115">**DLL**</span></span> | <span data-ttu-id="7f0e8-116">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="7f0e8-116">d3d9.dll</span></span> |