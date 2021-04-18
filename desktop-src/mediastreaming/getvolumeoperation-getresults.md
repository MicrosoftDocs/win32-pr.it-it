---
title: Metodo GetVolumeOperation. GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da GetVolumeAsync.
ms.assetid: 71DC4D76-4CC2-4D40-960F-AF56E1F33557
keywords:
- API di streaming multimediale metodo GetResults
- API di streaming multimediale del metodo GetResults, interfaccia GetVolumeOperation
- API di streaming multimediale dell'interfaccia GetVolumeOperation, metodo GetResults
topic_type:
- apiref
api_name:
- GetVolumeOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 444eaf590e5afc5d4f5185bcd3793698d6fe4535
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299745"
---
# <a name="getvolumeoperationgetresults-method"></a><span data-ttu-id="09267-106">Metodo GetVolumeOperation. GetResults</span><span class="sxs-lookup"><span data-stu-id="09267-106">GetVolumeOperation.GetResults method</span></span>

<span data-ttu-id="09267-107">Restituisce i risultati dell'operazione asincrona avviata da [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span><span class="sxs-lookup"><span data-stu-id="09267-107">Returns the results of the asynchronous operation started by [**GetVolumeAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getvolumeasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="09267-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09267-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="09267-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="09267-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09267-110">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="09267-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="09267-111">Volume.</span><span class="sxs-lookup"><span data-stu-id="09267-111">The volume.</span></span> <span data-ttu-id="09267-112">Valore compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="09267-112">A value between 0 and 100.</span></span> <span data-ttu-id="09267-113">0 indica il volume minimo e 100 indica il volume massimo.</span><span class="sxs-lookup"><span data-stu-id="09267-113">0 indicates minimum volume, and 100 indicates maximum volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09267-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09267-114">Return value</span></span>

<span data-ttu-id="09267-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="09267-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="09267-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="09267-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="09267-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="09267-117">Return code</span></span>                                                                          | <span data-ttu-id="09267-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09267-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="09267-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="09267-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="09267-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="09267-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="09267-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="09267-121">Remarks</span></span>

<span data-ttu-id="09267-122">Il metodo **GetResults** viene in genere chiamato dal gestore eventi registrato impostando la proprietà [**Completed**](getvolumeoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="09267-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getvolumeoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="09267-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09267-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09267-124">**GetVolumeOperation**</span><span class="sxs-lookup"><span data-stu-id="09267-124">**GetVolumeOperation**</span></span>](getvolumeoperation.md)
</dt> </dl>

 

