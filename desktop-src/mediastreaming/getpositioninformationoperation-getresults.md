---
title: Metodo GetPositionInformationOperation. GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da GetPositionInformationAsync.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- API di streaming multimediale metodo GetResults
- API di streaming multimediale del metodo GetResults, interfaccia GetPositionInformationOperation
- API di streaming multimediale dell'interfaccia GetPositionInformationOperation, metodo GetResults
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a0b4311c3be814a73ddb1e2a9b18d8e19aea9ee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726759"
---
# <a name="getpositioninformationoperationgetresults-method"></a><span data-ttu-id="8d404-106">Metodo GetPositionInformationOperation. GetResults</span><span class="sxs-lookup"><span data-stu-id="8d404-106">GetPositionInformationOperation.GetResults method</span></span>

<span data-ttu-id="8d404-107">Restituisce i risultati dell'operazione asincrona avviata da [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span><span class="sxs-lookup"><span data-stu-id="8d404-107">Returns the results of the asynchronous operation started by [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="8d404-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d404-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="8d404-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d404-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d404-110">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8d404-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8d404-111">Riferimento a una struttura [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) che contiene i risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="8d404-111">A reference to a [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d404-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d404-112">Return value</span></span>

<span data-ttu-id="8d404-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8d404-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8d404-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8d404-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8d404-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8d404-115">Return code</span></span>                                                                          | <span data-ttu-id="8d404-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d404-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8d404-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8d404-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8d404-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="8d404-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8d404-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d404-119">Remarks</span></span>

<span data-ttu-id="8d404-120">Il metodo **GetResults** viene in genere chiamato dal gestore eventi registrato impostando la proprietà [**Completed**](getpositioninformationoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="8d404-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getpositioninformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d404-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d404-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d404-122">**GetPositionInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="8d404-122">**GetPositionInformationOperation**</span></span>](getpositioninformationoperation.md)
</dt> </dl>

 

