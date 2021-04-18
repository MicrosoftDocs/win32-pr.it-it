---
description: Il metodo ChangeStop viene chiamato quando viene modificata la posizione di arresto.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: Metodo CSourceSeeking. ChangeStop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eefcc64b4692363c8caa8f39a3a0db9beb0d08b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327531"
---
# <a name="csourceseekingchangestop-method"></a><span data-ttu-id="75004-103">CSourceSeeking. ChangeStop, metodo</span><span class="sxs-lookup"><span data-stu-id="75004-103">CSourceSeeking.ChangeStop method</span></span>

<span data-ttu-id="75004-104">Il `ChangeStop` metodo viene chiamato quando viene modificata la posizione di arresto.</span><span class="sxs-lookup"><span data-stu-id="75004-104">The `ChangeStop` method is called when the stop position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="75004-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75004-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a><span data-ttu-id="75004-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="75004-106">Parameters</span></span>

<span data-ttu-id="75004-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="75004-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75004-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75004-108">Return value</span></span>

<span data-ttu-id="75004-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="75004-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75004-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="75004-110">Remarks</span></span>

<span data-ttu-id="75004-111">Il metodo [**CSourceSeeking:: Sepositions**](csourceseeking-setpositions.md) chiama questo metodo se la posizione di arresto cambia.</span><span class="sxs-lookup"><span data-stu-id="75004-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the stop position changes.</span></span> <span data-ttu-id="75004-112">Questo metodo è virtuale puro; la classe derivata deve implementarla.</span><span class="sxs-lookup"><span data-stu-id="75004-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="75004-113">Nell'esempio seguente viene illustrata una possibile implementazione:</span><span class="sxs-lookup"><span data-stu-id="75004-113">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="75004-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75004-114">Requirements</span></span>



| <span data-ttu-id="75004-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="75004-115">Requirement</span></span> | <span data-ttu-id="75004-116">Valore</span><span class="sxs-lookup"><span data-stu-id="75004-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75004-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75004-117">Header</span></span><br/>  | <dl> <span data-ttu-id="75004-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75004-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="75004-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="75004-119">Library</span></span><br/> | <dl> <span data-ttu-id="75004-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="75004-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75004-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75004-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75004-122">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="75004-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




