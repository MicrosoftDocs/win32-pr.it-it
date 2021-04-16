---
title: Metodo PlaybackOperation. GetResults
description: Restituisce i risultati di un'operazione asincrona avviata da uno dei metodi di riproduzione MediaRenderer.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- API di streaming multimediale metodo GetResults
- API di streaming multimediale del metodo GetResults, interfaccia PlaybackOperation
- API di streaming multimediale dell'interfaccia PlaybackOperation, metodo GetResults
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f146876966cc4e003bd88ad295c9938e5240abfe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397191"
---
# <a name="playbackoperationgetresults-method"></a><span data-ttu-id="765d6-106">Metodo PlaybackOperation. GetResults</span><span class="sxs-lookup"><span data-stu-id="765d6-106">PlaybackOperation.GetResults method</span></span>

<span data-ttu-id="765d6-107">Restituisce i risultati di un'operazione asincrona avviata da uno dei metodi di riproduzione [**MediaRenderer**](mediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="765d6-107">Returns the results of an asynchronous operation started by one of the [**MediaRenderer**](mediarenderer.md) playback methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="765d6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="765d6-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="765d6-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="765d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="765d6-110">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="765d6-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="765d6-111">Risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="765d6-111">The result of the operation.</span></span> <span data-ttu-id="765d6-112">Il valore 0 indica che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="765d6-112">A value of 0 indicates that the operation completed.</span></span> <span data-ttu-id="765d6-113">Altri valori sono riservati.</span><span class="sxs-lookup"><span data-stu-id="765d6-113">Other values are reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="765d6-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="765d6-114">Return value</span></span>

<span data-ttu-id="765d6-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="765d6-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="765d6-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="765d6-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="765d6-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="765d6-117">Return code</span></span>                                                                          | <span data-ttu-id="765d6-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="765d6-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="765d6-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="765d6-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="765d6-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="765d6-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="765d6-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="765d6-121">Remarks</span></span>

<span data-ttu-id="765d6-122">Il metodo **GetResults** viene in genere chiamato dal gestore eventi registrato impostando la proprietà [**Completed**](playbackoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="765d6-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](playbackoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="765d6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="765d6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="765d6-124">**PlaybackOperation**</span><span class="sxs-lookup"><span data-stu-id="765d6-124">**PlaybackOperation**</span></span>](playbackoperation.md)
</dt> </dl>

 

 





