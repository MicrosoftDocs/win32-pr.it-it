---
title: Metodo IMediaRendererActionInformation IsStopAvailable
description: Recupera un valore che indica se ricevitore sta attualmente accettando il Metodo StopAsync.
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- API di streaming multimediale del metodo IsStopAvailable
- API di streaming multimediale del metodo IsStopAvailable, interfaccia IMediaRendererActionInformation
- API di streaming multimediale dell'interfaccia IMediaRendererActionInformation, metodo IsStopAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e0a031bafc9a755dfec2498f4e2a52cdd9ef5b1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117691"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a><span data-ttu-id="17c91-106">Metodo IMediaRendererActionInformation:: IsStopAvailable</span><span class="sxs-lookup"><span data-stu-id="17c91-106">IMediaRendererActionInformation::IsStopAvailable method</span></span>

<span data-ttu-id="17c91-107">Recupera un valore che indica se ricevitore sta attualmente accettando il metodo [**StopAsync**](imediarenderer-stopasync.md) .</span><span class="sxs-lookup"><span data-stu-id="17c91-107">Retrieves a value that indicates whether the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c91-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17c91-108">Syntax</span></span>


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="17c91-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="17c91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c91-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="17c91-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17c91-111">Valore booleano che è **true** se ricevitore sta attualmente accettando il metodo [**StopAsync**](imediarenderer-stopasync.md) e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="17c91-111">A boolean value that is **True** if the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c91-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17c91-112">Return value</span></span>

<span data-ttu-id="17c91-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="17c91-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="17c91-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="17c91-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="17c91-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="17c91-115">Return code</span></span>                                                                          | <span data-ttu-id="17c91-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17c91-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="17c91-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="17c91-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="17c91-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="17c91-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="17c91-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17c91-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c91-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="17c91-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

