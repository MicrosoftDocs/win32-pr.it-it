---
description: Il metodo IsEndOfStream esegue una query se è stata ricevuta la notifica di fine del flusso.
ms.assetid: 44f9b740-ff7d-4387-9c2c-a5b6b90f3295
title: Metodo CBaseRenderer. IsEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.IsEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e07afb4dfb10e38d90184ba5747f200d1bc716d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326940"
---
# <a name="cbaserendererisendofstream-method"></a><span data-ttu-id="34951-103">CBaseRenderer. IsEndOfStream, metodo</span><span class="sxs-lookup"><span data-stu-id="34951-103">CBaseRenderer.IsEndOfStream method</span></span>

<span data-ttu-id="34951-104">Il `IsEndOfStream` metodo esegue una query se è stata ricevuta la notifica di fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="34951-104">The `IsEndOfStream` method queries whether the end-of-stream notification was received.</span></span>

## <a name="syntax"></a><span data-ttu-id="34951-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34951-105">Syntax</span></span>


```C++
BOOL IsEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="34951-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34951-106">Parameters</span></span>

<span data-ttu-id="34951-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="34951-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="34951-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34951-108">Return value</span></span>

<span data-ttu-id="34951-109">Restituisce il flag [**\_ bEOS CBaseRenderer:: m**](cbaserenderer-m-beos.md) .</span><span class="sxs-lookup"><span data-stu-id="34951-109">Returns the [**CBaseRenderer::m\_bEOS**](cbaserenderer-m-beos.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="34951-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34951-110">Requirements</span></span>



| <span data-ttu-id="34951-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="34951-111">Requirement</span></span> | <span data-ttu-id="34951-112">Valore</span><span class="sxs-lookup"><span data-stu-id="34951-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34951-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34951-113">Header</span></span><br/>  | <dl> <span data-ttu-id="34951-114"><dt>Renbase. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="34951-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="34951-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="34951-115">Library</span></span><br/> | <dl> <span data-ttu-id="34951-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="34951-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34951-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34951-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34951-118">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="34951-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




