---
description: Il metodo iniziale viene chiamato quando cambia la posizione iniziale.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Metodo CSourceSeeking. iniziale (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333272"
---
# <a name="csourceseekingchangestart-method"></a><span data-ttu-id="40a10-103">CSourceSeeking. iniziale, metodo</span><span class="sxs-lookup"><span data-stu-id="40a10-103">CSourceSeeking.ChangeStart method</span></span>

<span data-ttu-id="40a10-104">Il `ChangeStart` metodo viene chiamato quando viene modificata la posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="40a10-104">The `ChangeStart` method is called when the start position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="40a10-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40a10-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a><span data-ttu-id="40a10-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="40a10-106">Parameters</span></span>

<span data-ttu-id="40a10-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="40a10-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40a10-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40a10-108">Return value</span></span>

<span data-ttu-id="40a10-109">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="40a10-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="40a10-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="40a10-110">Remarks</span></span>

<span data-ttu-id="40a10-111">Il metodo [**CSourceSeeking:: Sepositions**](csourceseeking-setpositions.md) chiama questo metodo se la posizione iniziale viene modificata.</span><span class="sxs-lookup"><span data-stu-id="40a10-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the start position changes.</span></span> <span data-ttu-id="40a10-112">Questo metodo è virtuale puro; la classe derivata deve implementarla.</span><span class="sxs-lookup"><span data-stu-id="40a10-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="40a10-113">Dopo un'operazione di ricerca, i timestamp devono essere riavviati da zero.</span><span class="sxs-lookup"><span data-stu-id="40a10-113">After a seek operation, time stamps should restart from zero.</span></span> <span data-ttu-id="40a10-114">I tempi dei supporti devono riflettere la nuova ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="40a10-114">Media times should reflect the new start time.</span></span> <span data-ttu-id="40a10-115">Nell'esempio seguente viene illustrata una possibile implementazione:</span><span class="sxs-lookup"><span data-stu-id="40a10-115">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="40a10-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40a10-116">Requirements</span></span>



| <span data-ttu-id="40a10-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="40a10-117">Requirement</span></span> | <span data-ttu-id="40a10-118">Valore</span><span class="sxs-lookup"><span data-stu-id="40a10-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40a10-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40a10-119">Header</span></span><br/>  | <dl> <span data-ttu-id="40a10-120"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40a10-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="40a10-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="40a10-121">Library</span></span><br/> | <dl> <span data-ttu-id="40a10-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="40a10-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40a10-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40a10-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a10-124">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="40a10-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




