---
title: Metodo IMediaRendererActionInformation IsPauseAvailable
description: Recupera un valore che indica se ricevitore sta attualmente accettando il metodo PauseAsync.
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- API di streaming multimediale del metodo IsPauseAvailable
- API di streaming multimediale del metodo IsPauseAvailable, interfaccia IMediaRendererActionInformation
- API di streaming multimediale dell'interfaccia IMediaRendererActionInformation, metodo IsPauseAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9eb0b750f5a04528aef830d87376c276bdaf6674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872466"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a><span data-ttu-id="bb0fd-106">Metodo IMediaRendererActionInformation:: IsPauseAvailable</span><span class="sxs-lookup"><span data-stu-id="bb0fd-106">IMediaRendererActionInformation::IsPauseAvailable method</span></span>

<span data-ttu-id="bb0fd-107">Recupera un valore che indica se ricevitore sta attualmente accettando il metodo [**PauseAsync**](imediarenderer-pauseasync.md) .</span><span class="sxs-lookup"><span data-stu-id="bb0fd-107">Retrieves a value that indicates whether the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb0fd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb0fd-108">Syntax</span></span>


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="bb0fd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb0fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb0fd-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="bb0fd-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb0fd-111">Valore booleano che è **true** se ricevitore sta attualmente accettando il metodo [**PauseAsync**](imediarenderer-pauseasync.md) e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bb0fd-111">A boolean value that is **True** if the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb0fd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb0fd-112">Return value</span></span>

<span data-ttu-id="bb0fd-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bb0fd-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bb0fd-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bb0fd-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bb0fd-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bb0fd-115">Return code</span></span>                                                                          | <span data-ttu-id="bb0fd-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb0fd-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bb0fd-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb0fd-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bb0fd-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="bb0fd-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="bb0fd-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb0fd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb0fd-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="bb0fd-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

