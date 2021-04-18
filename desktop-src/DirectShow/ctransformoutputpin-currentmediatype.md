---
description: Il metodo CurrentMediaType Recupera il tipo di supporto per la connessione al pin corrente.
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: Metodo CTransformOutputPin. CurrentMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee9ee15c3cda2baf8ab8d6e9cb0ec3c797e91a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330847"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a><span data-ttu-id="2cfaa-103">CTransformOutputPin. CurrentMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="2cfaa-103">CTransformOutputPin.CurrentMediaType method</span></span>

<span data-ttu-id="2cfaa-104">Il `CurrentMediaType` metodo recupera il tipo di supporto per la connessione al pin corrente.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-104">The `CurrentMediaType` method retrieves the media type for the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cfaa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cfaa-105">Syntax</span></span>


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a><span data-ttu-id="2cfaa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2cfaa-106">Parameters</span></span>

<span data-ttu-id="2cfaa-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2cfaa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2cfaa-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2cfaa-108">Return value</span></span>

<span data-ttu-id="2cfaa-109">Restituisce un riferimento alla variabile membro [**CBasePin:: m \_ mt**](cbasepin-m-mt.md) .</span><span class="sxs-lookup"><span data-stu-id="2cfaa-109">Returns a reference to the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cfaa-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cfaa-110">Requirements</span></span>



| <span data-ttu-id="2cfaa-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cfaa-111">Requirement</span></span> | <span data-ttu-id="2cfaa-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2cfaa-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cfaa-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2cfaa-113">Header</span></span><br/>  | <dl> <span data-ttu-id="2cfaa-114"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2cfaa-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2cfaa-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="2cfaa-115">Library</span></span><br/> | <dl> <span data-ttu-id="2cfaa-116"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2cfaa-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




