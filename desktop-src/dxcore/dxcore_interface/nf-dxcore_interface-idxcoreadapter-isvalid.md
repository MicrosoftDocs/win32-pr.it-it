---
title: IDXCoreAdapter::IsValid
description: Determina se l'oggetto adattatore DXCore è ancora valido.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f58d8607b75253efda2e111eb358f576d36b65f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047122"
---
# <a name="idxcoreadapterisvalid-method"></a><span data-ttu-id="be603-103">Metodo IDXCoreAdapter:: IsValid</span><span class="sxs-lookup"><span data-stu-id="be603-103">IDXCoreAdapter::IsValid method</span></span>

<span data-ttu-id="be603-104">Determina se l'oggetto adattatore DXCore è ancora valido.</span><span class="sxs-lookup"><span data-stu-id="be603-104">Determines whether this DXCore adapter object is still valid.</span></span> <span data-ttu-id="be603-105">Per istruzioni sulla programmazione ed esempi di codice, vedere [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="be603-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="be603-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be603-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a><span data-ttu-id="be603-107">Restituisce</span><span class="sxs-lookup"><span data-stu-id="be603-107">Returns</span></span>

<span data-ttu-id="be603-108">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="be603-108">Type: **bool**</span></span>

<span data-ttu-id="be603-109">Restituisce  `true`   se l'oggetto adattatore DXCore è ancora valido.</span><span class="sxs-lookup"><span data-stu-id="be603-109">Returns `true` if this DXCore adapter object is still valid.</span></span> <span data-ttu-id="be603-110">In caso contrario, restituisce  `false` .</span><span class="sxs-lookup"><span data-stu-id="be603-110">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="be603-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be603-111">See also</span></span>

<span data-ttu-id="be603-112">Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="be603-112">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>