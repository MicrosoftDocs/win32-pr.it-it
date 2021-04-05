---
title: Metodo GetMuteOperation. GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da GetMuteAsync.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- API di streaming multimediale metodo GetResults
- API di streaming multimediale del metodo GetResults, interfaccia GetMuteOperation
- API di streaming multimediale dell'interfaccia GetMuteOperation, metodo GetResults
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33c43dc7fee228b1808ff4f607ee6a72faf1e770
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117623"
---
# <a name="getmuteoperationgetresults-method"></a><span data-ttu-id="f1ab0-106">Metodo GetMuteOperation. GetResults</span><span class="sxs-lookup"><span data-stu-id="f1ab0-106">GetMuteOperation.GetResults method</span></span>

<span data-ttu-id="f1ab0-107">Restituisce i risultati dell'operazione asincrona avviata da [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span><span class="sxs-lookup"><span data-stu-id="f1ab0-107">Returns the results of the asynchronous operation started by [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ab0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1ab0-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="f1ab0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1ab0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1ab0-110">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f1ab0-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f1ab0-111">Valore di silenziamento.</span><span class="sxs-lookup"><span data-stu-id="f1ab0-111">The mute value.</span></span> <span data-ttu-id="f1ab0-112">Il valore true indica che l'audio è attualmente disattivato.</span><span class="sxs-lookup"><span data-stu-id="f1ab0-112">A value of true indicates that audio is currently muted.</span></span> <span data-ttu-id="f1ab0-113">Il valore false indica che l'audio non è disattivato.</span><span class="sxs-lookup"><span data-stu-id="f1ab0-113">A value of false indicates that audio is not muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1ab0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1ab0-114">Return value</span></span>

<span data-ttu-id="f1ab0-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f1ab0-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f1ab0-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f1ab0-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f1ab0-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f1ab0-117">Return code</span></span>                                                                          | <span data-ttu-id="f1ab0-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1ab0-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f1ab0-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f1ab0-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f1ab0-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f1ab0-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1ab0-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1ab0-121">Remarks</span></span>

<span data-ttu-id="f1ab0-122">Il metodo **GetResults** viene in genere chiamato dal gestore eventi registrato impostando la proprietà [**Completed**](getmuteoperation-completed.md) .</span><span class="sxs-lookup"><span data-stu-id="f1ab0-122">The **GetResults** method is typically called from the event handler that was registered by setting the [**Completed**](getmuteoperation-completed.md) property.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1ab0-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1ab0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ab0-124">**GetMuteOperation**</span><span class="sxs-lookup"><span data-stu-id="f1ab0-124">**GetMuteOperation**</span></span>](getmuteoperation.md)
</dt> </dl>

 

