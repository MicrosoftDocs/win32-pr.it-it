---
title: DXCoreSegmentGroup
description: Definisce le costanti che specificano il raggruppamento del segmento di memoria di un adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ce94d5f806879ea84f64c88d3a62b074a5c5415b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299996"
---
# <a name="dxcoresegmentgroup-enum"></a><span data-ttu-id="dd5b3-103">Enumerazione DXCoreSegmentGroup</span><span class="sxs-lookup"><span data-stu-id="dd5b3-103">DXCoreSegmentGroup enum</span></span>

<span data-ttu-id="dd5b3-104">Definisce le costanti che specificano il raggruppamento del segmento di memoria di un adapter.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-104">Defines constants that specify an adapter's memory segment grouping.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd5b3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd5b3-105">Syntax</span></span>

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a><span data-ttu-id="dd5b3-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="dd5b3-106">Constants</span></span>

### <a name="local"></a><span data-ttu-id="dd5b3-107">Locale</span><span class="sxs-lookup"><span data-stu-id="dd5b3-107">Local</span></span>

<span data-ttu-id="dd5b3-108">Specifica un raggruppamento di segmenti considerati locali per l'adapter e rappresenta la memoria più veloce disponibile per la GPU.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-108">Specifies a grouping of segments that is considered local to the adapter, and represents the fastest memory available to the GPU.</span></span> <span data-ttu-id="dd5b3-109">L'applicazione deve essere destinata al gruppo di segmenti locale come dimensione di destinazione per la relativa working set.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-109">Your application should target the local segment group as the target size for its working set.</span></span>

### <a name="nonlocal"></a><span data-ttu-id="dd5b3-110">Non locali</span><span class="sxs-lookup"><span data-stu-id="dd5b3-110">NonLocal</span></span>

<span data-ttu-id="dd5b3-111">Specifica un raggruppamento di segmenti considerati non locali per l'adapter e può avere prestazioni più lente rispetto al gruppo di segmenti locale.</span><span class="sxs-lookup"><span data-stu-id="dd5b3-111">Specifies a grouping of segments that is considered non-local to the adapter, and may have slower performance than the local segment group.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd5b3-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd5b3-112">See also</span></span>

<span data-ttu-id="dd5b3-113">Guida di [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="dd5b3-113">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>