---
title: Metodo IMediaRendererFactory CreateMediaRendererAsync
description: Crea in modo asincrono una nuova istanza di un oggetto che implementa l'interfaccia IMediaRenderer usando il nome univoco del dispositivo (UDN) specificato.
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- API di streaming multimediale del metodo CreateMediaRendererAsync
- API di streaming multimediale del metodo CreateMediaRendererAsync, interfaccia IMediaRendererFactory
- API di streaming multimediale dell'interfaccia IMediaRendererFactory, metodo CreateMediaRendererAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725882"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a><span data-ttu-id="992ee-106">Metodo IMediaRendererFactory:: CreateMediaRendererAsync</span><span class="sxs-lookup"><span data-stu-id="992ee-106">IMediaRendererFactory::CreateMediaRendererAsync method</span></span>

<span data-ttu-id="992ee-107">Crea in modo asincrono una nuova istanza di un oggetto che implementa l'interfaccia [**IMediaRenderer**](imediarenderer.md) usando il nome univoco del dispositivo (UDN) specificato.</span><span class="sxs-lookup"><span data-stu-id="992ee-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified Unique Device Name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="992ee-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="992ee-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="992ee-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="992ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="992ee-110">*DeviceIdentifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="992ee-110">*deviceIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="992ee-111">Un HSTRING contenente un UDN che identifica il dispositivo ricevitore DLNA per cui verrà creata un'istanza di [**IMediaRenderer**](imediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="992ee-111">An HSTRING containing a UDN that identifies the DLNA DMR device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="992ee-112">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="992ee-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="992ee-113">Riceve un riferimento a un oggetto [**CreateMediaRendererOperation**](createmediarendereroperation.md) usato per ottenere risultati dall'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="992ee-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="992ee-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="992ee-114">Return value</span></span>

<span data-ttu-id="992ee-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="992ee-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="992ee-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="992ee-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="992ee-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="992ee-117">Return code</span></span>                                                                          | <span data-ttu-id="992ee-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="992ee-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="992ee-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="992ee-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="992ee-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="992ee-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="992ee-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="992ee-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992ee-122">**IMediaRendererFactory**</span><span class="sxs-lookup"><span data-stu-id="992ee-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

