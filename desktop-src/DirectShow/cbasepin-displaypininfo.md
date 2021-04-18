---
description: Il metodo DisplayPinInfo traccia una connessione pin durante il debug.
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: Metodo CBasePin. DisplayPinInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ea563ca07eaea6b6974a831726918866414a33b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329540"
---
# <a name="cbasepindisplaypininfo-method"></a><span data-ttu-id="98f3b-103">CBasePin. DisplayPinInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="98f3b-103">CBasePin.DisplayPinInfo method</span></span>

<span data-ttu-id="98f3b-104">Il `DisplayPinInfo` Metodo traccia una connessione pin durante il debug.</span><span class="sxs-lookup"><span data-stu-id="98f3b-104">The `DisplayPinInfo` method traces a pin connection during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="98f3b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98f3b-105">Syntax</span></span>


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="98f3b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="98f3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98f3b-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="98f3b-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="98f3b-108">Puntatore al pin di ricezione.</span><span class="sxs-lookup"><span data-stu-id="98f3b-108">Pointer to the receiving pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98f3b-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="98f3b-109">Return value</span></span>

<span data-ttu-id="98f3b-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="98f3b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="98f3b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="98f3b-111">Remarks</span></span>

<span data-ttu-id="98f3b-112">Nelle compilazioni di debug questo metodo chiama la funzione [**DbgLog**](dbglog.md) per tracciare un tentativo di connessione.</span><span class="sxs-lookup"><span data-stu-id="98f3b-112">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to trace a connection attempt.</span></span> <span data-ttu-id="98f3b-113">Nelle compilazioni finali, questo metodo non esegue alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="98f3b-113">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="98f3b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98f3b-114">Requirements</span></span>



| <span data-ttu-id="98f3b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="98f3b-115">Requirement</span></span> | <span data-ttu-id="98f3b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="98f3b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98f3b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="98f3b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="98f3b-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98f3b-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="98f3b-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="98f3b-119">Library</span></span><br/> | <dl> <span data-ttu-id="98f3b-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="98f3b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98f3b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98f3b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98f3b-122">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="98f3b-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




