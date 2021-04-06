---
title: Metodo IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync
description: Crea in modo asincrono una nuova istanza di un oggetto che implementa l'interfaccia IMediaRenderer utilizzando l'interfaccia IBasicDevice specificata.
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- API di streaming multimediale del metodo CreateMediaRendererFromBasicDeviceAsync
- API di streaming multimediale del metodo CreateMediaRendererFromBasicDeviceAsync, interfaccia IMediaRendererFactory
- API di streaming multimediale dell'interfaccia IMediaRendererFactory, metodo CreateMediaRendererFromBasicDeviceAsync
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4ee614cca9a03ca203ecde9203e019fab38ab4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046645"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a><span data-ttu-id="fde86-106">Metodo IMediaRendererFactory:: CreateMediaRendererFromBasicDeviceAsync</span><span class="sxs-lookup"><span data-stu-id="fde86-106">IMediaRendererFactory::CreateMediaRendererFromBasicDeviceAsync method</span></span>

<span data-ttu-id="fde86-107">Crea in modo asincrono una nuova istanza di un oggetto che implementa l'interfaccia [**IMediaRenderer**](imediarenderer.md) utilizzando l'interfaccia [**IBasicDevice**](ibasicdevice.md) specificata.</span><span class="sxs-lookup"><span data-stu-id="fde86-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified [**IBasicDevice**](ibasicdevice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="fde86-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fde86-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="fde86-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fde86-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde86-110">*basicDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fde86-110">*basicDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fde86-111">Puntatore a un'interfaccia [**IBasicDevice**](ibasicdevice.md) che rappresenta il dispositivo per cui verrà creata un'istanza di [**IMediaRenderer**](imediarenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="fde86-111">A pointer to an [**IBasicDevice**](ibasicdevice.md) interface representing the device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="fde86-112">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="fde86-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fde86-113">Riceve un riferimento a un oggetto [**CreateMediaRendererOperation**](createmediarendereroperation.md) usato per ottenere risultati dall'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="fde86-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde86-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fde86-114">Return value</span></span>

<span data-ttu-id="fde86-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fde86-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fde86-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fde86-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fde86-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fde86-117">Return code</span></span>                                                                          | <span data-ttu-id="fde86-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fde86-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fde86-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fde86-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fde86-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="fde86-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="fde86-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fde86-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fde86-122">**IMediaRendererFactory**</span><span class="sxs-lookup"><span data-stu-id="fde86-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

