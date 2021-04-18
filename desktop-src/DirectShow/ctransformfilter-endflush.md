---
description: Il metodo EndFlush termina un'operazione di svuotamento.
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Metodo CTransformFilter. EndFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 348675f1369ec9b0deb5415ad14a864a8befef73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328340"
---
# <a name="ctransformfilterendflush-method"></a><span data-ttu-id="1cbb7-103">CTransformFilter. EndFlush, metodo</span><span class="sxs-lookup"><span data-stu-id="1cbb7-103">CTransformFilter.EndFlush method</span></span>

<span data-ttu-id="1cbb7-104">Il `EndFlush` metodo termina un'operazione di svuotamento.</span><span class="sxs-lookup"><span data-stu-id="1cbb7-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cbb7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1cbb7-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="1cbb7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1cbb7-106">Parameters</span></span>

<span data-ttu-id="1cbb7-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1cbb7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cbb7-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1cbb7-108">Return value</span></span>

<span data-ttu-id="1cbb7-109">Restituisce S \_ OK o un altro valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1cbb7-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cbb7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1cbb7-110">Remarks</span></span>

<span data-ttu-id="1cbb7-111">Al termine di un'operazione di scaricamento, il metodo [**CTransformInputPin:: EndFlush**](ctransforminputpin-endflush.md) del PIN di input chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="1cbb7-111">At the end of a flush operation, the input pin's [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) method calls this method.</span></span> <span data-ttu-id="1cbb7-112">Questo metodo passa la `EndFlush` chiamata downstream.</span><span class="sxs-lookup"><span data-stu-id="1cbb7-112">This method passes the `EndFlush` call downstream.</span></span>

<span data-ttu-id="1cbb7-113">Se la classe derivata utilizza un thread di lavoro per recapitare gli esempi, è necessario rimuovere tutti i dati in coda prima di inviare la `EndFlush` chiamata downstream.</span><span class="sxs-lookup"><span data-stu-id="1cbb7-113">If the derived class uses a worker thread to deliver samples, it must discard any queued data before sending the `EndFlush` call downstream.</span></span> <span data-ttu-id="1cbb7-114">Per ulteriori informazioni, vedere [flusso di dati per gli sviluppatori di filtri](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="1cbb7-114">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cbb7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1cbb7-115">Requirements</span></span>



| <span data-ttu-id="1cbb7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cbb7-116">Requirement</span></span> | <span data-ttu-id="1cbb7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1cbb7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbb7-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1cbb7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1cbb7-119"><dt>Transfrm. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cbb7-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1cbb7-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="1cbb7-120">Library</span></span><br/> | <dl> <span data-ttu-id="1cbb7-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1cbb7-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cbb7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cbb7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cbb7-123">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="1cbb7-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




