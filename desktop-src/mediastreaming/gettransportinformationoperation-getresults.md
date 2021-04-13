---
title: Metodo GetResults di GetTransportInformationOperation
description: Restituisce i risultati dell'operazione asincrona avviata da GetTransportInformationAsync.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- API di streaming multimediale metodo GetResults
- API di streaming multimediale del metodo GetResults, interfaccia GetTransportInformationOperation
- API di streaming multimediale dell'interfaccia GetTransportInformationOperation, metodo GetResults
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17f846a5824ed07bcaf849a540429eaabe46f3d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398968"
---
# <a name="gettransportinformationoperationgetresults-method"></a><span data-ttu-id="f739c-106">Metodo GetTransportInformationOperation:: GetResults</span><span class="sxs-lookup"><span data-stu-id="f739c-106">GetTransportInformationOperation::GetResults method</span></span>

<span data-ttu-id="f739c-107">Restituisce i risultati dell'operazione asincrona avviata da [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span><span class="sxs-lookup"><span data-stu-id="f739c-107">Returns the results of the asynchronous operation started by [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="f739c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f739c-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a><span data-ttu-id="f739c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f739c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f739c-110">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f739c-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f739c-111">Riferimento a una struttura [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) che contiene i risultati dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f739c-111">A reference to a [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) structure that contains the results of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f739c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f739c-112">Return value</span></span>

<span data-ttu-id="f739c-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f739c-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f739c-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f739c-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f739c-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f739c-115">Return code</span></span>                                                                          | <span data-ttu-id="f739c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f739c-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f739c-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f739c-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f739c-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f739c-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f739c-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f739c-119">Remarks</span></span>

<span data-ttu-id="f739c-120">Il metodo **GetResults** viene in genere chiamato dal gestore eventi registrato impostando la proprietà [**Completed**](gettransportinformationoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="f739c-120">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](gettransportinformationoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="f739c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f739c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f739c-122">**GetTransportInformationOperation**</span><span class="sxs-lookup"><span data-stu-id="f739c-122">**GetTransportInformationOperation**</span></span>](gettransportinformationoperation.md)
</dt> </dl>

 

