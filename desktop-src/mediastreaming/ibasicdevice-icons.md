---
title: IBasicDevice icons (metodo)
description: Restituisce un vettore di interfacce IDeviceIcon.
ms.assetid: 0C083AF3-FE22-4A8E-87B7-0FFA7B65ADBD
keywords:
- API flusso multimediale metodo icone
- API di streaming multimediale del metodo icons, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo icons
topic_type:
- apiref
api_name:
- IBasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fb6e4b708b4e38ffb39f152308cec7b885a772f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724986"
---
# <a name="ibasicdeviceicons-method"></a><span data-ttu-id="301f1-106">Metodo IBasicDevice:: icons</span><span class="sxs-lookup"><span data-stu-id="301f1-106">IBasicDevice::Icons method</span></span>

<span data-ttu-id="301f1-107">Restituisce un vettore di interfacce [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="301f1-107">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="301f1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="301f1-108">Syntax</span></span>


```C++
HRESULT Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="parameters"></a><span data-ttu-id="301f1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="301f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="301f1-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="301f1-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="301f1-111">Riceve una raccolta enumerabile di puntatori dell'interfaccia [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="301f1-111">Receives an enumerable collection of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="301f1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="301f1-112">Return value</span></span>

<span data-ttu-id="301f1-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="301f1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="301f1-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="301f1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="301f1-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="301f1-115">Return code</span></span>                                                                          | <span data-ttu-id="301f1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="301f1-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="301f1-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="301f1-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="301f1-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="301f1-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="301f1-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="301f1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="301f1-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="301f1-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

