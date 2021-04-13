---
title: Metodo IMediaRendererActionInformation IsPlayAvailable
description: Recupera un valore che indica se ricevitore sta attualmente accettando i metodi PlayAsync e PlayAtSpeedAsync.
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- API di streaming multimediale del metodo IsPlayAvailable
- API di streaming multimediale del metodo IsPlayAvailable, interfaccia IMediaRendererActionInformation
- API di streaming multimediale dell'interfaccia IMediaRendererActionInformation, metodo IsPlayAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 87fa3a2005772a4d948bafe32d2a0e10cc5a6914
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398966"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a><span data-ttu-id="6426e-106">Metodo IMediaRendererActionInformation:: IsPlayAvailable</span><span class="sxs-lookup"><span data-stu-id="6426e-106">IMediaRendererActionInformation::IsPlayAvailable method</span></span>

<span data-ttu-id="6426e-107">Recupera un valore che indica se ricevitore sta attualmente accettando i metodi [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) e [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) .</span><span class="sxs-lookup"><span data-stu-id="6426e-107">Retrieves a value that indicates whether the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="6426e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6426e-108">Syntax</span></span>


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="6426e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6426e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6426e-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="6426e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6426e-111">Valore booleano che è **true** se ricevitore sta attualmente accettando i metodi accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) e [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6426e-111">A boolean value that is **True** if the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6426e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6426e-112">Return value</span></span>

<span data-ttu-id="6426e-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6426e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6426e-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6426e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6426e-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6426e-115">Return code</span></span>                                                                          | <span data-ttu-id="6426e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6426e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6426e-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6426e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6426e-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6426e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6426e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6426e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6426e-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="6426e-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

