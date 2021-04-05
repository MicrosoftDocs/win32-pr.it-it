---
title: Metodo IMediaRenderer StopAsync
description: Indica a ricevitore in modo asincrono di arrestare la riproduzione del contenuto corrente. | Metodo IMediaRenderer StopAsync
ms.assetid: B6B0F3F2-E95E-4A58-9CBD-CF4CB24FDAD0
keywords:
- API di streaming multimediale del Metodo StopAsync
- API di streaming multimediale del Metodo StopAsync, interfaccia IMediaRenderer
- API di streaming multimediale dell'interfaccia IMediaRenderer, Metodo StopAsync
topic_type:
- apiref
api_name:
- IMediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5f73d534fdd786038a242614a981f4915d92c13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886233"
---
# <a name="imediarendererstopasync-method"></a><span data-ttu-id="6284d-107">Metodo IMediaRenderer:: StopAsync</span><span class="sxs-lookup"><span data-stu-id="6284d-107">IMediaRenderer::StopAsync method</span></span>

<span data-ttu-id="6284d-108">Indica a ricevitore in modo asincrono di arrestare la riproduzione del contenuto corrente.</span><span class="sxs-lookup"><span data-stu-id="6284d-108">Instructs the DMR asynchronously to stop playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="6284d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6284d-109">Syntax</span></span>


```C++
HRESULT StopAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="6284d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6284d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6284d-111">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="6284d-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6284d-112">Riceve un riferimento a un oggetto [**PlaybackOperation**](playbackoperation.md) usato per ottenere risultati dall'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="6284d-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6284d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6284d-113">Return value</span></span>

<span data-ttu-id="6284d-114">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6284d-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6284d-115">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6284d-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6284d-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6284d-116">Return code</span></span>                                                                          | <span data-ttu-id="6284d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6284d-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6284d-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6284d-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6284d-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6284d-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6284d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6284d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6284d-121">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="6284d-121">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





