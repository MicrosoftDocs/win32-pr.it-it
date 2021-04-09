---
title: Struttura WINBIO_EXTENDED_ENGINE_INFO ( \_ tipi WINBIO. h)
description: Contiene informazioni sulle funzionalità e i requisiti di registrazione della scheda del motore per un'unità biometrica.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- Struttura di WINBIO_EXTENDED_ENGINE_INFO Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_EXTENDED_ENGINE_INFO
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENGINE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829bd0423ab6add41b17f59d308aea850c5b2f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874546"
---
# <a name="winbio_extended_engine_info-structure"></a><span data-ttu-id="c1e42-105">\_ \_ Struttura informazioni motore esteso WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="c1e42-105">WINBIO\_EXTENDED\_ENGINE\_INFO structure</span></span>

<span data-ttu-id="c1e42-106">Contiene informazioni sulle funzionalità e i requisiti di registrazione della scheda del motore per un'unità biometrica.</span><span class="sxs-lookup"><span data-stu-id="c1e42-106">Contains information about the capabilities and enrollment requirements of the engine adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1e42-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c1e42-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENGINE_INFO {
  WINBIO_CAPABILITIES   GenericEngineCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG GeneralSamples;
        ULONG Center;
        ULONG TopEdge;
        ULONG BottomEdge;
        ULONG LeftEdge;
        ULONG RightEdge;
      } EnrollmentRequirements;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENGINE_INFO, *PWINBIO_EXTENDED_ENGINE_INFO;
```



## <a name="members"></a><span data-ttu-id="c1e42-108">Members</span><span class="sxs-lookup"><span data-stu-id="c1e42-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1e42-109">**GenericEngineCapabilities**</span><span class="sxs-lookup"><span data-stu-id="c1e42-109">**GenericEngineCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-110">Funzionalità generiche del componente motore connesso a un'unità biometrica specifica.</span><span class="sxs-lookup"><span data-stu-id="c1e42-110">The generic capabilities of the engine component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="c1e42-111">**Fattore**</span><span class="sxs-lookup"><span data-stu-id="c1e42-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-112">Tipo di unità biometrica per la quale questa struttura contiene informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore del motore.</span><span class="sxs-lookup"><span data-stu-id="c1e42-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="c1e42-113">Se, ad esempio, il valore del membro **Factor** è **WINBIO \_ , \_** la struttura di **\_ informazioni del \_ motore \_ esteso WINBIO** si applica a un lettore di impronte digitali e contiene le informazioni rilevanti nella struttura **specifico. Fingerprint** .</span><span class="sxs-lookup"><span data-stu-id="c1e42-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_ENGINE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="c1e42-114">**Specifica**</span><span class="sxs-lookup"><span data-stu-id="c1e42-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-115">Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore del motore per un'unità biometrica correlata a un fattore biometrico specifico.</span><span class="sxs-lookup"><span data-stu-id="c1e42-115">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="c1e42-116">**Null**</span><span class="sxs-lookup"><span data-stu-id="c1e42-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-117">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c1e42-117">Reserved.</span></span> <span data-ttu-id="c1e42-118">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c1e42-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1e42-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="c1e42-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-120">Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore del motore per un'unità biometrica correlata alle funzionalità facciali.</span><span class="sxs-lookup"><span data-stu-id="c1e42-120">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="c1e42-121">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c1e42-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-122">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c1e42-122">Reserved.</span></span> <span data-ttu-id="c1e42-123">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c1e42-123">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1e42-124">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="c1e42-124">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1e42-125">**Null**</span><span class="sxs-lookup"><span data-stu-id="c1e42-125">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-126">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c1e42-126">Reserved.</span></span> <span data-ttu-id="c1e42-127">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c1e42-127">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="c1e42-128">**Impronta digitale**</span><span class="sxs-lookup"><span data-stu-id="c1e42-128">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-129">Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore del motore per un'unità biometrica relativa ai modelli di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="c1e42-129">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="c1e42-130">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c1e42-130">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-131">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c1e42-131">Reserved.</span></span> <span data-ttu-id="c1e42-132">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c1e42-132">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1e42-133">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="c1e42-133">**EnrollmentRequirements**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-134">Il numero di campioni validi necessari per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="c1e42-134">The number of good samples required to create a new fingerprint template.</span></span>

<dl> <dt>

<span data-ttu-id="c1e42-135">**GeneralSamples**</span><span class="sxs-lookup"><span data-stu-id="c1e42-135">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-136">Numero totale di campioni validi necessari per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="c1e42-136">The total number of good samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="c1e42-137">**Center**</span><span class="sxs-lookup"><span data-stu-id="c1e42-137">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-138">Il numero di campioni validi per il centro dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="c1e42-138">The number of good samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="c1e42-139">**TopEdge**</span><span class="sxs-lookup"><span data-stu-id="c1e42-139">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-140">Il numero di campioni validi per il bordo superiore dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="c1e42-140">The number of good samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="c1e42-141">**BottomEdge**</span><span class="sxs-lookup"><span data-stu-id="c1e42-141">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-142">Il numero di campioni validi per il bordo inferiore dell'impronta digitale necessario per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="c1e42-142">The number of good samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="c1e42-143">**LeftEdge**</span><span class="sxs-lookup"><span data-stu-id="c1e42-143">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-144">Il numero di campioni validi per il bordo sinistro dell'impronta digitale necessaria per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="c1e42-144">The number of good samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="c1e42-145">**RightEdge**</span><span class="sxs-lookup"><span data-stu-id="c1e42-145">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-146">Il numero di campioni validi per il bordo destro dell'impronta digitale necessaria per creare un nuovo modello di impronta digitale.</span><span class="sxs-lookup"><span data-stu-id="c1e42-146">The number of good samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="c1e42-147">**Iris**</span><span class="sxs-lookup"><span data-stu-id="c1e42-147">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-148">Informazioni sulle funzionalità e i requisiti di registrazione dell'adattatore del motore per un'unità biometrica relativa ai modelli Iris.</span><span class="sxs-lookup"><span data-stu-id="c1e42-148">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="c1e42-149">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c1e42-149">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-150">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c1e42-150">Reserved.</span></span> <span data-ttu-id="c1e42-151">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c1e42-151">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1e42-152">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="c1e42-152">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1e42-153">**Null**</span><span class="sxs-lookup"><span data-stu-id="c1e42-153">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-154">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c1e42-154">Reserved.</span></span> <span data-ttu-id="c1e42-155">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c1e42-155">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="c1e42-156">**Chiamata vocale**</span><span class="sxs-lookup"><span data-stu-id="c1e42-156">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-157">Informazioni sulle funzionalità e sui requisiti di registrazione dell'adattatore del motore per un'unità biometrica relativa ai modelli vocali.</span><span class="sxs-lookup"><span data-stu-id="c1e42-157">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="c1e42-158">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c1e42-158">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-159">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c1e42-159">Reserved.</span></span> <span data-ttu-id="c1e42-160">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c1e42-160">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c1e42-161">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="c1e42-161">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c1e42-162">**Null**</span><span class="sxs-lookup"><span data-stu-id="c1e42-162">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="c1e42-163">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c1e42-163">Reserved.</span></span> <span data-ttu-id="c1e42-164">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c1e42-164">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c1e42-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1e42-165">Requirements</span></span>



| <span data-ttu-id="c1e42-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1e42-166">Requirement</span></span> | <span data-ttu-id="c1e42-167">Valore</span><span class="sxs-lookup"><span data-stu-id="c1e42-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e42-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1e42-168">Minimum supported client</span></span><br/> | <span data-ttu-id="c1e42-169">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c1e42-169">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="c1e42-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1e42-170">Minimum supported server</span></span><br/> | <span data-ttu-id="c1e42-171">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="c1e42-171">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="c1e42-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1e42-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1e42-173"><dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="c1e42-173"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1e42-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1e42-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e42-175">**\_Costanti della funzionalità WINBIO**</span><span class="sxs-lookup"><span data-stu-id="c1e42-175">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="c1e42-176">**\_ \_ Costanti di tipo biometrico WINBIO**</span><span class="sxs-lookup"><span data-stu-id="c1e42-176">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> </dl>

 

 





