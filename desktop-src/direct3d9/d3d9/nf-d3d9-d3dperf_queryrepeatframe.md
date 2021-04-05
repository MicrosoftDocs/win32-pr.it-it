---
title: Funzione D3DPERF_QueryRepeatFrame
description: Determinare se un profiler delle prestazioni richiede che il frame corrente venga nuovamente inviato a Direct3D per l'analisi delle prestazioni. Questa funzione non è attualmente supportata da PIX.
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
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/08/2020
ms.locfileid: "103723878"
---
# <a name="d3dperf_queryrepeatframe-function"></a><span data-ttu-id="646b6-104">Funzione D3DPERF_QueryRepeatFrame</span><span class="sxs-lookup"><span data-stu-id="646b6-104">D3DPERF_QueryRepeatFrame function</span></span>

<span data-ttu-id="646b6-105">Determinare se un profiler delle prestazioni richiede che il frame corrente venga nuovamente inviato a Direct3D per l'analisi delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="646b6-105">Determine whether a performance profiler is requesting that the current frame be resubmitted to Direct3D for performance analysis.</span></span> <span data-ttu-id="646b6-106">Questa funzione non è attualmente supportata da PIX.</span><span class="sxs-lookup"><span data-stu-id="646b6-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="646b6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="646b6-107">Syntax</span></span>

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a><span data-ttu-id="646b6-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="646b6-108">Return value</span></span>

<span data-ttu-id="646b6-109">Se il valore restituito è TRUE, il chiamante deve ripetere la stessa sequenza di chiamate.</span><span class="sxs-lookup"><span data-stu-id="646b6-109">If the return value is TRUE, the caller should repeat the same sequence of calls.</span></span> <span data-ttu-id="646b6-110">Se FALSE, il chiamante deve continuare.</span><span class="sxs-lookup"><span data-stu-id="646b6-110">If FALSE, the caller should continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="646b6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="646b6-111">Remarks</span></span>

<span data-ttu-id="646b6-112">La funzione deve essere chiamata immediatamente dopo la chiamata di **IDirect3DDevice9::P** reinviate.</span><span class="sxs-lookup"><span data-stu-id="646b6-112">The function should be called immediately after **IDirect3DDevice9::Present** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="646b6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="646b6-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="646b6-114">**Piattaforma di destinazione**</span><span class="sxs-lookup"><span data-stu-id="646b6-114">**Target Platform**</span></span> | <span data-ttu-id="646b6-115">Windows</span><span class="sxs-lookup"><span data-stu-id="646b6-115">Windows</span></span> |
| <span data-ttu-id="646b6-116">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="646b6-116">**Header**</span></span> | <span data-ttu-id="646b6-117">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="646b6-117">d3d9.h</span></span> |
| <span data-ttu-id="646b6-118">**Libreria**</span><span class="sxs-lookup"><span data-stu-id="646b6-118">**Library**</span></span> | <span data-ttu-id="646b6-119">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="646b6-119">d3d9.lib</span></span> |
| <span data-ttu-id="646b6-120">**DLL**</span><span class="sxs-lookup"><span data-stu-id="646b6-120">**DLL**</span></span> | <span data-ttu-id="646b6-121">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="646b6-121">d3d9.dll</span></span> |