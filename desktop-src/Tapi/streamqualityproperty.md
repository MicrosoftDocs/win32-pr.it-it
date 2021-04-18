---
description: 'Enumerazione StreamQualityProperty usata dai metodi ITStreamQualityControl:: GetRange, ITStreamQualityControl:: Get e ITStreamQualityControl:: set per indicare la proprietà della qualità del flusso da risolvere.'
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: Enumerazione StreamQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f552641cd0847bb3ff8eec9d528a03171a78c2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333863"
---
# <a name="streamqualityproperty-enumeration"></a><span data-ttu-id="ab08b-103">Enumerazione StreamQualityProperty</span><span class="sxs-lookup"><span data-stu-id="ab08b-103">StreamQualityProperty enumeration</span></span>

<span data-ttu-id="ab08b-104">\[ Questa enumerazione non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ab08b-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ab08b-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="ab08b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ab08b-106">Enumerazione **StreamQualityProperty** usata dai metodi [**ITStreamQualityControl:: GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl:: Get**](itstreamqualitycontrol-get.md)e [**ITStreamQualityControl:: set**](itstreamqualitycontrol-set.md) per indicare la proprietà della qualità del flusso da risolvere.</span><span class="sxs-lookup"><span data-stu-id="ab08b-106">The **StreamQualityProperty** enum used by the [**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl::Get**](itstreamqualitycontrol-get.md), and [**ITStreamQualityControl::Set**](itstreamqualitycontrol-set.md) methods to indicate the stream quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab08b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab08b-107">Syntax</span></span>


```C++
} StreamQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="ab08b-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="ab08b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ab08b-109"><span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**\_MaxBitrate StreamQuality**</span><span class="sxs-lookup"><span data-stu-id="ab08b-109"><span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality\_MaxBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="ab08b-110">Velocità in bit massima.</span><span class="sxs-lookup"><span data-stu-id="ab08b-110">Maximum bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="ab08b-111"><span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**\_CurrBitrate StreamQuality**</span><span class="sxs-lookup"><span data-stu-id="ab08b-111"><span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality\_CurrBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="ab08b-112">Velocità in bit minima.</span><span class="sxs-lookup"><span data-stu-id="ab08b-112">Minimum bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="ab08b-113"><span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**\_MinFrameInterval StreamQuality**</span><span class="sxs-lookup"><span data-stu-id="ab08b-113"><span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality\_MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="ab08b-114">Intervallo massimo di frame.</span><span class="sxs-lookup"><span data-stu-id="ab08b-114">Maximum frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="ab08b-115"><span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**\_AvgFrameInterval StreamQuality**</span><span class="sxs-lookup"><span data-stu-id="ab08b-115"><span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality\_AvgFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="ab08b-116">Intervallo minimo frame.</span><span class="sxs-lookup"><span data-stu-id="ab08b-116">Minimum frame interval.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab08b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab08b-117">Requirements</span></span>



| <span data-ttu-id="ab08b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab08b-118">Requirement</span></span> | <span data-ttu-id="ab08b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ab08b-119">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab08b-120">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="ab08b-120">TAPI version</span></span><br/> | <span data-ttu-id="ab08b-121">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="ab08b-121">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="ab08b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab08b-122">Header</span></span><br/>       | <dl> <span data-ttu-id="ab08b-123"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab08b-123"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab08b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab08b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab08b-125">**ITStreamQualityControl:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="ab08b-125">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="ab08b-126">**ITStreamQualityControl:: Get**</span><span class="sxs-lookup"><span data-stu-id="ab08b-126">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="ab08b-127">**ITStreamQualityControl:: set**</span><span class="sxs-lookup"><span data-stu-id="ab08b-127">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




