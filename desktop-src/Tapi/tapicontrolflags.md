---
description: L'enumerazione TAPIControlFlags viene usata da diversi metodi per indicare se una determinata proprietà viene controllata automaticamente o manualmente.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Enumerazione TAPIControlFlags (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cc3e931c69a408d996fa28e6002b6c53c9df87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331772"
---
# <a name="tapicontrolflags-enumeration"></a><span data-ttu-id="af1cd-103">Enumerazione TAPIControlFlags</span><span class="sxs-lookup"><span data-stu-id="af1cd-103">TAPIControlFlags enumeration</span></span>

<span data-ttu-id="af1cd-104">\[ Questa enumerazione non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="af1cd-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="af1cd-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="af1cd-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="af1cd-106">L'enumerazione **TAPIControlFlags** viene usata da diversi metodi per indicare se una determinata proprietà viene controllata automaticamente o manualmente.</span><span class="sxs-lookup"><span data-stu-id="af1cd-106">The **TAPIControlFlags** enum is used by a number of methods to indicate whether a given property is controlled automatically or manually.</span></span>

## <a name="syntax"></a><span data-ttu-id="af1cd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af1cd-107">Syntax</span></span>


```C++
} TAPIControlFlags;
```



## <a name="constants"></a><span data-ttu-id="af1cd-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="af1cd-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="af1cd-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**\_Flag TAPIControl \_ None**</span><span class="sxs-lookup"><span data-stu-id="af1cd-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl\_Flags\_None**</span></span>
</dt> <dd>

<span data-ttu-id="af1cd-110">TAPI non ha flag di controllo per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="af1cd-110">TAPI has no control flags for the property.</span></span>

</dd> <dt>

<span data-ttu-id="af1cd-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**\_Flag TAPIControl \_ automatici**</span><span class="sxs-lookup"><span data-stu-id="af1cd-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl\_Flags\_Auto**</span></span>
</dt> <dd>

<span data-ttu-id="af1cd-112">La proprietà viene controllata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="af1cd-112">The property is controlled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="af1cd-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**\_Manuale flag \_ TAPIControl**</span><span class="sxs-lookup"><span data-stu-id="af1cd-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**TAPIControl\_Flags\_Manual**</span></span>
</dt> <dd>

<span data-ttu-id="af1cd-114">La proprietà viene controllata manualmente.</span><span class="sxs-lookup"><span data-stu-id="af1cd-114">The property is controlled manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af1cd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af1cd-115">Requirements</span></span>



| <span data-ttu-id="af1cd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="af1cd-116">Requirement</span></span> | <span data-ttu-id="af1cd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="af1cd-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="af1cd-118">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="af1cd-118">TAPI version</span></span><br/> | <span data-ttu-id="af1cd-119">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="af1cd-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="af1cd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af1cd-120">Header</span></span><br/>       | <dl> <span data-ttu-id="af1cd-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="af1cd-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af1cd-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af1cd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af1cd-123">**ITAudioDeviceControl:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="af1cd-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="af1cd-124">**ITAudioDeviceControl:: Get**</span><span class="sxs-lookup"><span data-stu-id="af1cd-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="af1cd-125">**ITAudioDeviceControl:: set**</span><span class="sxs-lookup"><span data-stu-id="af1cd-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> <dt>

[<span data-ttu-id="af1cd-126">**ITAudioSettings:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="af1cd-126">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="af1cd-127">**ITAudioSettings:: Get**</span><span class="sxs-lookup"><span data-stu-id="af1cd-127">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="af1cd-128">**ITAudioSettings:: set**</span><span class="sxs-lookup"><span data-stu-id="af1cd-128">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> <dt>

[<span data-ttu-id="af1cd-129">**ITCallQualityControl:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="af1cd-129">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="af1cd-130">**ITCallQualityControl:: Get**</span><span class="sxs-lookup"><span data-stu-id="af1cd-130">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="af1cd-131">**ITCallQualityControl:: set**</span><span class="sxs-lookup"><span data-stu-id="af1cd-131">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> <dt>

[<span data-ttu-id="af1cd-132">**ITStreamQualityControl:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="af1cd-132">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="af1cd-133">**ITStreamQualityControl:: Get**</span><span class="sxs-lookup"><span data-stu-id="af1cd-133">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="af1cd-134">**ITStreamQualityControl:: set**</span><span class="sxs-lookup"><span data-stu-id="af1cd-134">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




