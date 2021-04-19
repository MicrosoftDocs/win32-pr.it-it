---
description: "L'enumerazione CallQualityProperty viene usata dai metodi ITCallQualityControl:: GetRange, ITCallQualityControl:: Get e ITCallQualityControl:: set per indicare la proprietà della qualità della chiamata da risolvere."
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: Enumerazione CallQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ca3af31e0b85a443bb34ac1992b3d3b5c89bfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329089"
---
# <a name="callqualityproperty-enumeration"></a><span data-ttu-id="03d16-103">Enumerazione CallQualityProperty</span><span class="sxs-lookup"><span data-stu-id="03d16-103">CallQualityProperty enumeration</span></span>

<span data-ttu-id="03d16-104">\[ Questa enumerazione non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="03d16-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="03d16-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="03d16-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="03d16-106">L'enumerazione **CallQualityProperty** viene usata dai metodi [**ITCallQualityControl:: GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl:: Get**](itcallqualitycontrol-get.md)e [**ITCallQualityControl:: set**](itcallqualitycontrol-set.md) per indicare la proprietà della qualità della chiamata da risolvere.</span><span class="sxs-lookup"><span data-stu-id="03d16-106">The **CallQualityProperty** enum is used by the [**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl::Get**](itcallqualitycontrol-get.md), and [**ITCallQualityControl::Set**](itcallqualitycontrol-set.md) methods to indicate the call quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d16-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03d16-107">Syntax</span></span>


```C++
} CallQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="03d16-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="03d16-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="03d16-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**\_ControlInterval CallQuality**</span><span class="sxs-lookup"><span data-stu-id="03d16-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality\_ControlInterval**</span></span>
</dt> <dd>

<span data-ttu-id="03d16-110">Intervallo di controllo.</span><span class="sxs-lookup"><span data-stu-id="03d16-110">Control interval.</span></span>

</dd> <dt>

<span data-ttu-id="03d16-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**\_ConfBitrate CallQuality**</span><span class="sxs-lookup"><span data-stu-id="03d16-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality\_ConfBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="03d16-112">Velocità in bit per la conferenza.</span><span class="sxs-lookup"><span data-stu-id="03d16-112">Bit rate for conference.</span></span>

</dd> <dt>

<span data-ttu-id="03d16-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**\_MaxInputBitrate CallQuality**</span><span class="sxs-lookup"><span data-stu-id="03d16-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality\_MaxInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="03d16-114">Velocità in bit di input massima.</span><span class="sxs-lookup"><span data-stu-id="03d16-114">Maximum input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="03d16-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**\_CurrInputBitrate CallQuality**</span><span class="sxs-lookup"><span data-stu-id="03d16-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality\_CurrInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="03d16-116">Velocità in bit di input corrente.</span><span class="sxs-lookup"><span data-stu-id="03d16-116">Current input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="03d16-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**\_MaxOutputBitrate CallQuality**</span><span class="sxs-lookup"><span data-stu-id="03d16-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality\_MaxOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="03d16-118">Velocità in bit di output massima.</span><span class="sxs-lookup"><span data-stu-id="03d16-118">Maximum output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="03d16-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**\_CurrOutputBitrate CallQuality**</span><span class="sxs-lookup"><span data-stu-id="03d16-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality\_CurrOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="03d16-120">Velocità in bit di output corrente.</span><span class="sxs-lookup"><span data-stu-id="03d16-120">Current output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="03d16-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**\_MaxCPULoad CallQuality**</span><span class="sxs-lookup"><span data-stu-id="03d16-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality\_MaxCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="03d16-122">Carico massimo della CPU.</span><span class="sxs-lookup"><span data-stu-id="03d16-122">Maximum CPU load.</span></span>

</dd> <dt>

<span data-ttu-id="03d16-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**\_CurrCPULoad CallQuality**</span><span class="sxs-lookup"><span data-stu-id="03d16-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality\_CurrCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="03d16-124">Carico corrente della CPU.</span><span class="sxs-lookup"><span data-stu-id="03d16-124">Current CPU load.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03d16-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03d16-125">Requirements</span></span>



| <span data-ttu-id="03d16-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="03d16-126">Requirement</span></span> | <span data-ttu-id="03d16-127">Valore</span><span class="sxs-lookup"><span data-stu-id="03d16-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03d16-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="03d16-128">TAPI version</span></span><br/> | <span data-ttu-id="03d16-129">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="03d16-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="03d16-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03d16-130">Header</span></span><br/>       | <dl> <span data-ttu-id="03d16-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="03d16-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03d16-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03d16-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d16-133">**ITCallQualityControl:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="03d16-133">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="03d16-134">**ITCallQualityControl:: Get**</span><span class="sxs-lookup"><span data-stu-id="03d16-134">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="03d16-135">**ITCallQualityControl:: set**</span><span class="sxs-lookup"><span data-stu-id="03d16-135">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> </dl>

 

 




