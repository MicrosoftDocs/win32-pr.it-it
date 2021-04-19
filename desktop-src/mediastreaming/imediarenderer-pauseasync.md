---
title: Metodo IMediaRenderer PauseAsync
description: Indica a ricevitore in modo asincrono di sospendere la riproduzione del contenuto corrente. | Metodo IMediaRenderer PauseAsync
ms.assetid: 2EADD9BE-2306-4CDA-AD5C-8342C06EAF1B
keywords:
- API di streaming multimediale del metodo PauseAsync
- API di streaming multimediale del metodo PauseAsync, interfaccia IMediaRenderer
- API di streaming multimediale dell'interfaccia IMediaRenderer, metodo PauseAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8713fa4b2fe46a694024c2873cd50a0ec89ce898
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321898"
---
# <a name="imediarendererpauseasync-method"></a><span data-ttu-id="ca88d-107">IMediaRenderer::P metodo auseAsync</span><span class="sxs-lookup"><span data-stu-id="ca88d-107">IMediaRenderer::PauseAsync method</span></span>

<span data-ttu-id="ca88d-108">Indica a ricevitore in modo asincrono di sospendere la riproduzione del contenuto corrente.</span><span class="sxs-lookup"><span data-stu-id="ca88d-108">Instructs the DMR asynchronously to pause playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca88d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca88d-109">Syntax</span></span>


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="ca88d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca88d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca88d-111">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ca88d-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca88d-112">Riceve un riferimento a un oggetto [**PlaybackOperation**](playbackoperation.md) usato per ottenere risultati dall'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="ca88d-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca88d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca88d-113">Return value</span></span>

<span data-ttu-id="ca88d-114">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ca88d-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ca88d-115">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ca88d-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ca88d-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ca88d-116">Return code</span></span>                                                                          | <span data-ttu-id="ca88d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca88d-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ca88d-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca88d-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ca88d-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ca88d-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ca88d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca88d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca88d-121">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="ca88d-121">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





