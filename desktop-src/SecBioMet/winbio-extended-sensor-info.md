---
title: Struttura WINBIO_EXTENDED_SENSOR_INFO ( \_ tipi WINBIO. h)
description: Contiene informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- Struttura di WINBIO_EXTENDED_SENSOR_INFO Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_EXTENDED_SENSOR_INFO
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_SENSOR_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c535ef56eeade897aac3c1d0503477da406935b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963866"
---
# <a name="winbio_extended_sensor_info-structure"></a><span data-ttu-id="782eb-105">\_ \_ Struttura info sensore esteso WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="782eb-105">WINBIO\_EXTENDED\_SENSOR\_INFO structure</span></span>

<span data-ttu-id="782eb-106">Contiene informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="782eb-106">Contains information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="782eb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="782eb-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_SENSOR_INFO {
  WINBIO_CAPABILITIES   GenericSensorCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } FacialFeatures;
    struct {
      ULONG32 Reserved;
    } Fingerprint;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO;
```



## <a name="members"></a><span data-ttu-id="782eb-108">Members</span><span class="sxs-lookup"><span data-stu-id="782eb-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="782eb-109">**GenericSensorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="782eb-109">**GenericSensorCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-110">Funzionalità generiche del componente sensore connesso a un'unità biometrica specifica.</span><span class="sxs-lookup"><span data-stu-id="782eb-110">The generic capabilities of the sensor component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="782eb-111">**Fattore**</span><span class="sxs-lookup"><span data-stu-id="782eb-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-112">Tipo di unità biometrica per la quale questa struttura contiene informazioni sulle funzionalità e i requisiti di registrazione della scheda del sensore.</span><span class="sxs-lookup"><span data-stu-id="782eb-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the sensor adapter.</span></span> <span data-ttu-id="782eb-113">Se, ad esempio, il valore del membro **Factor** è **WINBIO \_ , \_** la struttura di **\_ informazioni sul \_ sensore \_ esteso WINBIO** si applica a un lettore di impronte digitali e contiene le informazioni rilevanti nella struttura **specifico. Fingerprint** .</span><span class="sxs-lookup"><span data-stu-id="782eb-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_SENSOR\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="782eb-114">**Specifica**</span><span class="sxs-lookup"><span data-stu-id="782eb-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-115">Informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica correlata a un fattore biometrico specifico.</span><span class="sxs-lookup"><span data-stu-id="782eb-115">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="782eb-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="782eb-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-117">Riservato.</span><span class="sxs-lookup"><span data-stu-id="782eb-117">Reserved.</span></span> <span data-ttu-id="782eb-118">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="782eb-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="782eb-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="782eb-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-120">Informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica correlata alle funzionalità facciali.</span><span class="sxs-lookup"><span data-stu-id="782eb-120">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="782eb-121">**FrameSize**</span><span class="sxs-lookup"><span data-stu-id="782eb-121">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-122">Dimensioni del fotogramma della fotocamera, indicate come lunghezza e larghezza in pixel per i membri **destro** e **inferiore** della struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="782eb-122">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="782eb-123">Il punto (0, 0) rappresenta l'angolo superiore sinistro del frame.</span><span class="sxs-lookup"><span data-stu-id="782eb-123">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="782eb-124">**FrameOffset**</span><span class="sxs-lookup"><span data-stu-id="782eb-124">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-125">Offset del fotogramma della fotocamera per la faccia dalla videocamera, in pixel.</span><span class="sxs-lookup"><span data-stu-id="782eb-125">The offset of the camera frame for the face from the video camera, in pixels.</span></span> <span data-ttu-id="782eb-126">Il valore (0, 0) indica che il fotogramma della fotocamera per la superficie e la videocamera video si sovrappongono completamente.</span><span class="sxs-lookup"><span data-stu-id="782eb-126">A value of (0, 0) indicates that the camera frame for the face and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="782eb-127">**MandatoryOrientation**</span><span class="sxs-lookup"><span data-stu-id="782eb-127">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-128">Orientamento preferito per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="782eb-128">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="782eb-129">**Impronta digitale**</span><span class="sxs-lookup"><span data-stu-id="782eb-129">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-130">Informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica correlata ai modelli di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="782eb-130">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="782eb-131">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="782eb-131">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-132">Riservato.</span><span class="sxs-lookup"><span data-stu-id="782eb-132">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="782eb-133">**Iris**</span><span class="sxs-lookup"><span data-stu-id="782eb-133">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-134">Informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica relativa ai modelli Iris.</span><span class="sxs-lookup"><span data-stu-id="782eb-134">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="782eb-135">**FrameSize**</span><span class="sxs-lookup"><span data-stu-id="782eb-135">**FrameSize**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-136">Dimensioni del fotogramma della fotocamera, indicate come lunghezza e larghezza in pixel per i membri **destro** e **inferiore** della struttura [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="782eb-136">The size of the camera frame, indicated as a length and width in pixels by the **right** and **bottom** members of the [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="782eb-137">Il punto (0, 0) rappresenta l'angolo superiore sinistro del frame.</span><span class="sxs-lookup"><span data-stu-id="782eb-137">The point (0, 0) represents the top-left corner of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="782eb-138">**FrameOffset**</span><span class="sxs-lookup"><span data-stu-id="782eb-138">**FrameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-139">Offset del fotogramma della fotocamera per l'iride dalla videocamera video, espresso in pixel.</span><span class="sxs-lookup"><span data-stu-id="782eb-139">The offset of the camera frame for the iris from the video camera, in pixels.</span></span> <span data-ttu-id="782eb-140">Il valore (0, 0) indica che il fotogramma della fotocamera per l'iride e la videocamera video si sovrappongono completamente.</span><span class="sxs-lookup"><span data-stu-id="782eb-140">A value of (0, 0) indicates that the camera frame for the iris and the video camera completely overlap.</span></span>

</dd> <dt>

<span data-ttu-id="782eb-141">**MandatoryOrientation**</span><span class="sxs-lookup"><span data-stu-id="782eb-141">**MandatoryOrientation**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-142">Orientamento preferito per la fotocamera.</span><span class="sxs-lookup"><span data-stu-id="782eb-142">The preferred orientation for the camera.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="782eb-143">**Chiamata vocale**</span><span class="sxs-lookup"><span data-stu-id="782eb-143">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-144">Informazioni sulle funzionalità e i requisiti di registrazione della scheda sensore per un'unità biometrica relativa ai modelli vocali.</span><span class="sxs-lookup"><span data-stu-id="782eb-144">Information about the capabilities and enrollment requirements of the sensor adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="782eb-145">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="782eb-145">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="782eb-146">Riservato.</span><span class="sxs-lookup"><span data-stu-id="782eb-146">Reserved.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="782eb-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="782eb-147">Requirements</span></span>



| <span data-ttu-id="782eb-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="782eb-148">Requirement</span></span> | <span data-ttu-id="782eb-149">Valore</span><span class="sxs-lookup"><span data-stu-id="782eb-149">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="782eb-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="782eb-150">Minimum supported client</span></span><br/> | <span data-ttu-id="782eb-151">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="782eb-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="782eb-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="782eb-152">Minimum supported server</span></span><br/> | <span data-ttu-id="782eb-153">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="782eb-153">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="782eb-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="782eb-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="782eb-155"><dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="782eb-155"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="782eb-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="782eb-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="782eb-157">**\_Costanti della funzionalità WINBIO**</span><span class="sxs-lookup"><span data-stu-id="782eb-157">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="782eb-158">**\_ \_ Costanti di tipo biometrico WINBIO**</span><span class="sxs-lookup"><span data-stu-id="782eb-158">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="782eb-159">**\_Costanti di orientamento WINBIO**</span><span class="sxs-lookup"><span data-stu-id="782eb-159">**WINBIO\_ORIENTATION Constants**</span></span>](winbio-orientation-constants.md)
</dt> </dl>

 

