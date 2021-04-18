---
title: MediaRenderer. PauseAsync, metodo
description: Indica a ricevitore in modo asincrono di sospendere la riproduzione del contenuto corrente. | MediaRenderer. PauseAsync, metodo
ms.assetid: 1bd36349-0551-44e8-9550-3fd80900de9a
keywords:
- API di streaming multimediale del metodo PauseAsync
- API di streaming multimediale del metodo PauseAsync, interfaccia MediaRenderer
- API di streaming multimediale dell'interfaccia MediaRenderer, metodo PauseAsync
topic_type:
- apiref
api_name:
- MediaRenderer.PauseAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2bbbc55931c7cc7fc5e2e5ec39ba63fe7a064478
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321935"
---
# <a name="mediarendererpauseasync-method"></a><span data-ttu-id="f68bd-107">MediaRenderer. PauseAsync, metodo</span><span class="sxs-lookup"><span data-stu-id="f68bd-107">MediaRenderer.PauseAsync method</span></span>

<span data-ttu-id="f68bd-108">Indica a ricevitore in modo asincrono di sospendere la riproduzione del contenuto corrente.</span><span class="sxs-lookup"><span data-stu-id="f68bd-108">Instructs the DMR asynchronously to pause playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="f68bd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f68bd-109">Syntax</span></span>


```C++
HRESULT PauseAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="f68bd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f68bd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f68bd-111">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f68bd-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f68bd-112">Riceve un riferimento a un oggetto [**PlaybackOperation**](playbackoperation.md) usato per ottenere risultati dall'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="f68bd-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f68bd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f68bd-113">Return value</span></span>

<span data-ttu-id="f68bd-114">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f68bd-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f68bd-115">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f68bd-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f68bd-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f68bd-116">Return code</span></span>                                                                          | <span data-ttu-id="f68bd-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f68bd-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f68bd-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f68bd-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f68bd-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f68bd-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f68bd-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f68bd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f68bd-121">**MediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="f68bd-121">**MediaRenderer**</span></span>](mediarenderer.md)
</dt> </dl>

 

 





