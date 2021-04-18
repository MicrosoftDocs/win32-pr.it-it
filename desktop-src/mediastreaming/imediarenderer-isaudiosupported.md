---
title: Metodo IMediaRenderer IsAudioSupported
description: Recupera un valore che indica se ricevitore è in grado di riprodurre contenuto audio.
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- API di streaming multimediale del metodo IsAudioSupported
- API di streaming multimediale del metodo IsAudioSupported, interfaccia IMediaRenderer
- API di streaming multimediale dell'interfaccia IMediaRenderer, metodo IsAudioSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7670d0a2818cf5518bee0b2586531caeea20fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299023"
---
# <a name="imediarendererisaudiosupported-method"></a><span data-ttu-id="1ea99-106">Metodo IMediaRenderer:: IsAudioSupported</span><span class="sxs-lookup"><span data-stu-id="1ea99-106">IMediaRenderer::IsAudioSupported method</span></span>

<span data-ttu-id="1ea99-107">Recupera un valore che indica se ricevitore è in grado di riprodurre contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="1ea99-107">Retrieves a value that indicates whether the DMR is capable of playing audio content.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ea99-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ea99-108">Syntax</span></span>


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="1ea99-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ea99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ea99-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="1ea99-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ea99-111">Valore booleano che è **true** se ricevitore è in grado di riprodurre contenuto audio e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1ea99-111">A boolean value that is **True** if the DMR is capable of playing audio content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ea99-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ea99-112">Return value</span></span>

<span data-ttu-id="1ea99-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1ea99-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1ea99-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1ea99-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1ea99-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1ea99-115">Return code</span></span>                                                                          | <span data-ttu-id="1ea99-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ea99-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="1ea99-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1ea99-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="1ea99-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="1ea99-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1ea99-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ea99-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ea99-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="1ea99-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





