---
title: Metodo IMediaRendererActionInformation IsSetNextSourceAvailable
description: Recupera un valore che indica se ricevitore sta attualmente accettando il metodo SetNextSourceFromUriAsync, il metodo SetNextSourceFromStreamAsync o il metodo SetNextSourceFromMediaSourceAsync.
ms.assetid: 7588E992-4070-4E0F-8C4B-7DFC097A5076
keywords:
- API di streaming multimediale del metodo IsSetNextSourceAvailable
- API di streaming multimediale del metodo IsSetNextSourceAvailable, interfaccia IMediaRendererActionInformation
- API di streaming multimediale dell'interfaccia IMediaRendererActionInformation, metodo IsSetNextSourceAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSetNextSourceAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 265a9a96d5229e47008c60813fd6c0e3bc567800
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725890"
---
# <a name="imediarendereractioninformationissetnextsourceavailable-method"></a><span data-ttu-id="3de3a-106">Metodo IMediaRendererActionInformation:: IsSetNextSourceAvailable</span><span class="sxs-lookup"><span data-stu-id="3de3a-106">IMediaRendererActionInformation::IsSetNextSourceAvailable method</span></span>

<span data-ttu-id="3de3a-107">Recupera un valore che indica se ricevitore sta attualmente accettando il metodo [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , il metodo [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) o il metodo [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) .</span><span class="sxs-lookup"><span data-stu-id="3de3a-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de3a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3de3a-108">Syntax</span></span>


```C++
HRESULT IsSetNextSourceAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="3de3a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3de3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de3a-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="3de3a-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3de3a-111">Valore booleano che è **true** se ricevitore sta attualmente accettando il metodo [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) , il metodo [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) o il metodo [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3de3a-111">A boolean value that is **True** if the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de3a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3de3a-112">Return value</span></span>

<span data-ttu-id="3de3a-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3de3a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3de3a-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3de3a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3de3a-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3de3a-115">Return code</span></span>                                                                          | <span data-ttu-id="3de3a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3de3a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3de3a-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3de3a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3de3a-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3de3a-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="3de3a-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3de3a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de3a-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="3de3a-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

