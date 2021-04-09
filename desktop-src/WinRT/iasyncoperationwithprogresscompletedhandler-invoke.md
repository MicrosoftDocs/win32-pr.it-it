---
description: Richiama il metodo che viene chiamato quando l'operazione asincrona specificata segnala lo stato di avanzamento.
ms.assetid: FB60DDC0-7521-4999-8DD8-175556004198
title: 'IAsyncOperationWithProgressCompletedHandler<TResult, TProgress metodo>:: Invoke'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>.Invoke
api_type:
- COM
api_location: ''
ms.openlocfilehash: 469686cbd96dedc7f816fdd1f482d3474362688e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129235"
---
# <a name="iasyncoperationwithprogresscompletedhandlertresulttprogressinvoke-method"></a><span data-ttu-id="4a2fe-103">IAsyncOperationWithProgressCompletedHandler<TResult, TProgress metodo>:: Invoke</span><span class="sxs-lookup"><span data-stu-id="4a2fe-103">IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>::Invoke method</span></span>

<span data-ttu-id="4a2fe-104">Richiama il metodo che viene chiamato quando l'operazione asincrona specificata segnala lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="4a2fe-104">Invokes the method that is called when the specified asynchronous operation reports progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2fe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a2fe-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncOperationWithProgress<TResult,TProgress> *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4a2fe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a2fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a2fe-107">*AsyncInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a2fe-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a2fe-108">Tipo: \**[**IAsyncOperationWithProgress<TResult, TProgress>**](/previous-versions//br205807(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="4a2fe-108">Type: \**[**IAsyncOperationWithProgress<TResult,TProgress>**](/previous-versions//br205807(v=vs.85))\** _</span></span>

<span data-ttu-id="4a2fe-109">Azione asincrona che segnala il completamento.</span><span class="sxs-lookup"><span data-stu-id="4a2fe-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a2fe-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a2fe-110">Return value</span></span>

<span data-ttu-id="4a2fe-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="4a2fe-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="4a2fe-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4a2fe-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4a2fe-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4a2fe-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a2fe-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a2fe-114">Requirements</span></span>



| <span data-ttu-id="4a2fe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a2fe-115">Requirement</span></span> | <span data-ttu-id="4a2fe-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4a2fe-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4a2fe-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a2fe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4a2fe-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4a2fe-118">Windows 8</span></span><br/>           |
| <span data-ttu-id="4a2fe-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a2fe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4a2fe-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4a2fe-120">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a2fe-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a2fe-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="4a2fe-122">[**IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>**](/previous-versions//br205808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4a2fe-122">[**IAsyncOperationWithProgressCompletedHandler<TResult,TProgress>**](/previous-versions//br205808(v=vs.85))</span></span>
</dt> </dl>

 

 
