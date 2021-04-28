---
description: 'Metodo CTransformInputPin.CurrentMediaType: il metodo CurrentMediaType recupera il tipo di supporto per la connessione pin corrente.'
ms.assetid: d46f4d8e-9e9d-49d3-b823-f2f0fcf25383
title: Metodo CTransformInputPin.CurrentMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 011f4eeda7f4a278baeceeadc7c21a822ae02b74
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084989"
---
# <a name="ctransforminputpincurrentmediatype-method"></a><span data-ttu-id="85c26-103">Metodo CTransformInputPin.CurrentMediaType</span><span class="sxs-lookup"><span data-stu-id="85c26-103">CTransformInputPin.CurrentMediaType method</span></span>

<span data-ttu-id="85c26-104">Il `CurrentMediaType` metodo recupera il tipo di supporto per la connessione pin corrente.</span><span class="sxs-lookup"><span data-stu-id="85c26-104">The `CurrentMediaType` method retrieves the media type for the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="85c26-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85c26-105">Syntax</span></span>


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a><span data-ttu-id="85c26-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85c26-106">Parameters</span></span>

<span data-ttu-id="85c26-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="85c26-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85c26-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85c26-108">Return value</span></span>

<span data-ttu-id="85c26-109">Restituisce un riferimento alla [**variabile membro CBasePin::m \_ mt.**](cbasepin-m-mt.md)</span><span class="sxs-lookup"><span data-stu-id="85c26-109">Returns a reference to the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="85c26-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85c26-110">Requirements</span></span>



| <span data-ttu-id="85c26-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c26-111">Requirement</span></span> | <span data-ttu-id="85c26-112">Valore</span><span class="sxs-lookup"><span data-stu-id="85c26-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85c26-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85c26-113">Header</span></span><br/>  | <dl> <span data-ttu-id="85c26-114"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="85c26-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="85c26-115">Libreria</span><span class="sxs-lookup"><span data-stu-id="85c26-115">Library</span></span><br/> | <dl> <span data-ttu-id="85c26-116"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="85c26-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




