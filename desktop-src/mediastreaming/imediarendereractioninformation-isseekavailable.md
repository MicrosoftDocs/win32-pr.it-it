---
title: Metodo IMediaRendererActionInformation IsSeekAvailable
description: Recupera un valore che indica se ricevitore sta attualmente accettando il Metodo SeekAsync.
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- API di streaming multimediale del metodo IsSeekAvailable
- API di streaming multimediale del metodo IsSeekAvailable, interfaccia IMediaRendererActionInformation
- API di streaming multimediale dell'interfaccia IMediaRendererActionInformation, metodo IsSeekAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 700afb72efbab01bbd3a8f5e15fa444eb6b06272
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872465"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a><span data-ttu-id="41627-106">Metodo IMediaRendererActionInformation:: IsSeekAvailable</span><span class="sxs-lookup"><span data-stu-id="41627-106">IMediaRendererActionInformation::IsSeekAvailable method</span></span>

<span data-ttu-id="41627-107">Recupera un valore che indica se ricevitore sta attualmente accettando il metodo [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) .</span><span class="sxs-lookup"><span data-stu-id="41627-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="41627-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41627-108">Syntax</span></span>


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="41627-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="41627-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41627-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="41627-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="41627-111">Valore booleano che è **true** se ricevitore sta attualmente accettando il metodo [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="41627-111">A boolean value that is **True** if the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41627-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41627-112">Return value</span></span>

<span data-ttu-id="41627-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="41627-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="41627-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="41627-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="41627-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="41627-115">Return code</span></span>                                                                          | <span data-ttu-id="41627-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41627-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="41627-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="41627-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="41627-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="41627-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="41627-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41627-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41627-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="41627-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

