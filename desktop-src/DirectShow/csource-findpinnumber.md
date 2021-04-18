---
description: Il metodo FindPinNumber Recupera il numero di un PIN specificato sul filtro.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: Metodo CSource. FindPinNumber (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324650"
---
# <a name="csourcefindpinnumber-method"></a><span data-ttu-id="4a1b8-103">CSource. FindPinNumber, metodo</span><span class="sxs-lookup"><span data-stu-id="4a1b8-103">CSource.FindPinNumber method</span></span>

<span data-ttu-id="4a1b8-104">Il `FindPinNumber` metodo recupera il numero di un PIN specificato sul filtro.</span><span class="sxs-lookup"><span data-stu-id="4a1b8-104">The `FindPinNumber` method retrieves the number of a specified pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a1b8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a1b8-105">Syntax</span></span>


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a><span data-ttu-id="4a1b8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a1b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a1b8-107">*iPin*</span><span class="sxs-lookup"><span data-stu-id="4a1b8-107">*iPin*</span></span> 
</dt> <dd>

<span data-ttu-id="4a1b8-108">Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.</span><span class="sxs-lookup"><span data-stu-id="4a1b8-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a1b8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a1b8-109">Return value</span></span>

<span data-ttu-id="4a1b8-110">Restituisce il numero del PIN oppure 1 se il PIN non viene trovato in questo filtro.</span><span class="sxs-lookup"><span data-stu-id="4a1b8-110">Returns the pin number, or  1 if the pin is not found on this filter.</span></span> <span data-ttu-id="4a1b8-111">Il primo pin è numerato zero.</span><span class="sxs-lookup"><span data-stu-id="4a1b8-111">The first pin is numbered zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a1b8-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a1b8-112">Requirements</span></span>



| <span data-ttu-id="4a1b8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a1b8-113">Requirement</span></span> | <span data-ttu-id="4a1b8-114">Valore</span><span class="sxs-lookup"><span data-stu-id="4a1b8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a1b8-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a1b8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4a1b8-116"><dt>Source. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a1b8-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4a1b8-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a1b8-117">Library</span></span><br/> | <dl> <span data-ttu-id="4a1b8-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4a1b8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a1b8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a1b8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a1b8-120">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="4a1b8-120">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




