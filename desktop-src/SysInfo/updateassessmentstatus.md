---
description: Viene descritto come aggiornare il sistema operativo in un dispositivo.
ms.assetid: 157E241E-E8D8-41F8-9565-5C9298DCD1BE
title: Enumerazione UpdateAssessmentStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateAssessmentStatus
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: 790077118db7704bdd04801758f44cbb50cc54b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308092"
---
# <a name="updateassessmentstatus-enumeration"></a><span data-ttu-id="f4032-103">Enumerazione UpdateAssessmentStatus</span><span class="sxs-lookup"><span data-stu-id="f4032-103">UpdateAssessmentStatus enumeration</span></span>

<span data-ttu-id="f4032-104">Viene descritto come aggiornare il sistema operativo in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4032-104">Describes how up-to-date the OS on a device is.</span></span> <span data-ttu-id="f4032-105">**UpdateAssessmentStatus** viene usato dalle strutture [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) e [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) nei membri **assessmentForCurrent**, **assessmentForUpToDate** e **securityStatus** .</span><span class="sxs-lookup"><span data-stu-id="f4032-105">**UpdateAssessmentStatus** is used by the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, in the **assessmentForCurrent**, **assessmentForUpToDate**, and **securityStatus** members.</span></span> <span data-ttu-id="f4032-106">Viene restituita esattamente una costante.</span><span class="sxs-lookup"><span data-stu-id="f4032-106">Exactly one constant is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4032-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4032-107">Syntax</span></span>


```C++
typedef enum TagUpdateAssessmentStatus { 
      UpdateAssessmentStatus_Latest                    = 0,
      UpdateAssessmentStatus_NotLatestSoftRestriction  = 1,
      UpdateAssessmentStatus_NotLatestHardRestriction  = 2,
      UpdateAssessmentStatus_NotLatestEndOfSupport     = 3,
      UpdateAssessmentStatus_NotLatestServicingTrain   = 4,
      UpdateAssessmentStatus_NotLatestDeferredFeature  = 5,
      UpdateAssessmentStatus_NotLatestDeferredQuality  = 6,
      UpdateAssessmentStatus_NotLatestPausedFeature    = 7,
      UpdateAssessmentStatus_NotLatestPausedQuality    = 8,
      UpdateAssessmentStatus_NotLatestManaged          = 9,
      UpdateAssessmentStatus_NotLatestUnknown          = 10,
      UpdateAssessmentStatus_NotLatestTargetedVersion  = 11
} UpdateAssessmentStatus;
```



## <a name="constants"></a><span data-ttu-id="f4032-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="f4032-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f4032-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**UpdateAssessmentStatus \_ Più recente**</span><span class="sxs-lookup"><span data-stu-id="f4032-109"><span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span> **UpdateAssessmentStatus\_Latest**</span></span>
</dt> <dd>

<span data-ttu-id="f4032-110">Questo risultato in **assessmentForCurrent** implica che il dispositivo si trovi nell'aggiornamento delle funzionalità più recente e nell'aggiornamento qualitativo disponibile per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4032-110">This result within **assessmentForCurrent** implies that the device is on the latest feature update and quality update available for that device.</span></span> <span data-ttu-id="f4032-111">All'interno di **assessmentForUpToDate**, questo risultato implica che il dispositivo si trovi nell'ultimo aggiornamento qualitativo per la versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f4032-111">Within **assessmentForUpToDate**, this result implies that the device is on the latest quality update for the release of Windows it is running.</span></span>

</dd> <dt>

<span data-ttu-id="f4032-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestSoftRestriction**</span><span class="sxs-lookup"><span data-stu-id="f4032-112"><span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestSoftRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="f4032-113">L'aggiornamento delle funzionalità più recente non è stato installato a causa di una restrizione flessibile.</span><span class="sxs-lookup"><span data-stu-id="f4032-113">The latest feature update has not been installed due to a soft restriction.</span></span> <span data-ttu-id="f4032-114">Quando una restrizione Soft è stata inserita in un aggiornamento, l'aggiornamento non verrà installato automaticamente; un utente deve avviare autonomamente il download all'interno dell'esperienza utente di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="f4032-114">When a soft restriction has been placed on an update, the update will not be automatically installed; a user must self-initiate the download within the Update UX.</span></span> <span data-ttu-id="f4032-115">Questo stato si applica solo a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="f4032-115">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="f4032-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestHardRestriction**</span><span class="sxs-lookup"><span data-stu-id="f4032-116"><span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span> **UpdateAssessmentStatus\_NotLatestHardRestriction**</span></span>
</dt> <dd>

<span data-ttu-id="f4032-117">L'aggiornamento delle funzionalità più recente non è stato installato a causa di una restrizione rigida.</span><span class="sxs-lookup"><span data-stu-id="f4032-117">The latest feature update has not been installed due to a hard restriction.</span></span> <span data-ttu-id="f4032-118">Quando è stata applicata una restrizione rigida a un aggiornamento, l'aggiornamento non è applicabile al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4032-118">When a hard restriction has been placed on an update, the update is not applicable to the device.</span></span> <span data-ttu-id="f4032-119">Questo stato si applica solo a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="f4032-119">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="f4032-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**UpdateAssessmentStatus \_ NotLatestEndOfSupport**</span><span class="sxs-lookup"><span data-stu-id="f4032-120"><span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span> **UpdateAssessmentStatus\_NotLatestEndOfSupport**</span></span>
</dt> <dd>

<span data-ttu-id="f4032-121">Il dispositivo non si trova nell'aggiornamento più recente perché l'aggiornamento delle funzionalità del dispositivo non è più supportato da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f4032-121">The device is not on the latest update because the device's feature update is no longer supported by Microsoft.</span></span> <span data-ttu-id="f4032-122">Quando Microsoft smette di supportare una versione di funzionalità, questo stato verrà restituito sia per **assessmentForCurrent** che per **assessmentForUpToDate**.</span><span class="sxs-lookup"><span data-stu-id="f4032-122">When Microsoft stops supporting a feature release, this status will be returned for both **assessmentForCurrent** and **assessmentForUpToDate**.</span></span>

> [!Note]  
> <span data-ttu-id="f4032-123">Quando viene restituito **UpdateAssessmentStatus \_ NotLatestEndOfSupport** , il **UpdateImpactLevel** della valutazione è sempre **UpdateImpactLevel \_ elevato**.</span><span class="sxs-lookup"><span data-stu-id="f4032-123">When **UpdateAssessmentStatus\_NotLatestEndOfSupport** is returned, the assessment's **UpdateImpactLevel** is always **UpdateImpactLevel\_High**.</span></span>

 

</dd> <dt>

<span data-ttu-id="f4032-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**UpdateAssessmentStatus \_ NotLatestServicingTrain**</span><span class="sxs-lookup"><span data-stu-id="f4032-124"><span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span> **UpdateAssessmentStatus\_NotLatestServicingTrain**</span></span>
</dt> <dd>

<span data-ttu-id="f4032-125">Il dispositivo non si trova nell'aggiornamento delle funzionalità più recente perché il training di manutenzione del dispositivo limita l'aggiornamento del dispositivo all'aggiornamento delle funzionalità più recente.</span><span class="sxs-lookup"><span data-stu-id="f4032-125">The device is not on the latest feature update because the device's servicing train limits the device from updating to the latest feature update.</span></span> <span data-ttu-id="f4032-126">Ad esempio, se un dispositivo è in Current Branch for Business (CBB) ed è stato rilasciato un nuovo aggiornamento della funzionalità per Current Branch (CB), verrà restituito.</span><span class="sxs-lookup"><span data-stu-id="f4032-126">For example: if a device is on Current Branch for Business (CBB) and a new feature update has been released for Current Branch (CB), this will be returned.</span></span> <span data-ttu-id="f4032-127">Questo stato si applica solo a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="f4032-127">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="f4032-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestDeferredFeature**</span><span class="sxs-lookup"><span data-stu-id="f4032-128"><span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestDeferredFeature**</span></span>
</dt> <dd>

<span data-ttu-id="f4032-129">L'aggiornamento delle funzionalità più recente non è stato installato a causa dei criteri di rinvio degli aggiornamenti delle funzionalità di Windows Update del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4032-129">The latest feature update has not been installed due to the device's Windows Update for Business Feature Update Deferral policy.</span></span> <span data-ttu-id="f4032-130">La determinazione di **daysOutOfDate** prende in considerazione i criteri di rinvio. **daysOutOfDate** non inizierà l'incremento fino alla scadenza del periodo di differimento.</span><span class="sxs-lookup"><span data-stu-id="f4032-130">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span> <span data-ttu-id="f4032-131">Questo stato si applica solo a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="f4032-131">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="f4032-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestDeferredQuality**</span><span class="sxs-lookup"><span data-stu-id="f4032-132"><span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestDeferredQuality**</span></span>
</dt> <dd>

<span data-ttu-id="f4032-133">Il dispositivo non si trova nell'aggiornamento di qualità più recente a causa dei criteri di rinvio degli aggiornamenti di qualità dell'Windows Update del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4032-133">The device is not on the latest quality update due to the device's Windows Update for Business Quality Update Deferral policy.</span></span> <span data-ttu-id="f4032-134">La determinazione di **daysOutOfDate** prende in considerazione i criteri di rinvio. **daysOutOfDate** non inizierà l'incremento fino alla scadenza del periodo di differimento.</span><span class="sxs-lookup"><span data-stu-id="f4032-134">Determining **daysOutOfDate** takes into account deferral policies; **daysOutOfDate** will not begin incrementing until the deferral period has expired.</span></span>

</dd> <dt>

<span data-ttu-id="f4032-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestPausedFeature**</span><span class="sxs-lookup"><span data-stu-id="f4032-135"><span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span> **UpdateAssessmentStatus\_NotLatestPausedFeature**</span></span>
</dt> <dd>

<span data-ttu-id="f4032-136">Il dispositivo non si trova nell'aggiornamento delle funzionalità più recente a causa del dispositivo con aggiornamenti delle funzionalità sospesi.</span><span class="sxs-lookup"><span data-stu-id="f4032-136">The device is not on the latest feature update due to the device having paused Feature Updates.</span></span> <span data-ttu-id="f4032-137">Se un dispositivo è sospeso non viene inserito nel calcolo di **daysOutOfDate**.</span><span class="sxs-lookup"><span data-stu-id="f4032-137">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="f4032-138">Questo stato si applica solo a **assessmentForCurrent**.</span><span class="sxs-lookup"><span data-stu-id="f4032-138">This status only applies to **assessmentForCurrent**.</span></span>

</dd> <dt>

<span data-ttu-id="f4032-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestPausedQuality**</span><span class="sxs-lookup"><span data-stu-id="f4032-139"><span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span> **UpdateAssessmentStatus\_NotLatestPausedQuality**</span></span>
</dt> <dd>

<span data-ttu-id="f4032-140">Il dispositivo non si trova nell'aggiornamento di qualità più recente a causa del dispositivo con aggiornamenti di qualità sospesi.</span><span class="sxs-lookup"><span data-stu-id="f4032-140">The device is not on the latest quality update due to the device having paused Quality Updates.</span></span> <span data-ttu-id="f4032-141">Se un dispositivo è sospeso non viene inserito nel calcolo di **daysOutOfDate**.</span><span class="sxs-lookup"><span data-stu-id="f4032-141">Whether a device is paused is not factored into the calculation of **daysOutOfDate**.</span></span> <span data-ttu-id="f4032-142">**daysOutOfDate** non determina se un dispositivo viene sospeso nel calcolo.</span><span class="sxs-lookup"><span data-stu-id="f4032-142">**daysOutOfDate** does not factor whether a device is paused into its calculation.</span></span>

</dd> <dt>

<span data-ttu-id="f4032-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**UpdateAssessmentStatus \_ NotLatestManaged**</span><span class="sxs-lookup"><span data-stu-id="f4032-143"><span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span> **UpdateAssessmentStatus\_NotLatestManaged**</span></span>
</dt> <dd>

<span data-ttu-id="f4032-144">Il dispositivo non si trova nell'aggiornamento più recente perché l'approvazione degli aggiornamenti non viene eseguita tramite Windows Update.</span><span class="sxs-lookup"><span data-stu-id="f4032-144">The device is not on the latest update because the approval of updates is not done through Windows Update.</span></span>

</dd> <dt>

<span data-ttu-id="f4032-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**UpdateAssessmentStatus \_ NotLatestUnknown**</span><span class="sxs-lookup"><span data-stu-id="f4032-145"><span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span> **UpdateAssessmentStatus\_NotLatestUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="f4032-146">Il dispositivo non si trova nell'aggiornamento più recente a causa di un motivo che non può essere determinato dalla valutazione.</span><span class="sxs-lookup"><span data-stu-id="f4032-146">The device is not on the latest update due to a reason that cannot be determined by the assessment.</span></span>

</dd> <dt>

<span data-ttu-id="f4032-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**UpdateAssessmentStatus \_ NotLatestTargetedVersion**</span><span class="sxs-lookup"><span data-stu-id="f4032-147"><span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span> **UpdateAssessmentStatus\_NotLatestTargetedVersion**</span></span>
</dt> <dd>

<span data-ttu-id="f4032-148">Il dispositivo non si trova nell'aggiornamento delle funzionalità più recente a causa dei criteri della versione di destinazione Windows Update per business del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4032-148">The device is not on the latest feature update due to the device's Windows Update for Business Target Version policy.</span></span> <span data-ttu-id="f4032-149">Questo criterio mantiene il dispositivo nella versione di rilascio della funzionalità di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f4032-149">This policy is keeping the device on the targeted feature release version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4032-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4032-150">Remarks</span></span>

<span data-ttu-id="f4032-151">Questa enumerazione viene usata più spesso con le strutture [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) e [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , che a loro volta vengono usate con il metodo [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) per [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).</span><span class="sxs-lookup"><span data-stu-id="f4032-151">This enumeration is used most often with the [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) and [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structures, which are in turn used with the [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) method for [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4032-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4032-152">Requirements</span></span>



| <span data-ttu-id="f4032-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4032-153">Requirement</span></span> | <span data-ttu-id="f4032-154">Valore</span><span class="sxs-lookup"><span data-stu-id="f4032-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4032-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4032-155">Minimum supported client</span></span><br/> | <span data-ttu-id="f4032-156">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4032-156">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f4032-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4032-157">Minimum supported server</span></span><br/> | <span data-ttu-id="f4032-158">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="f4032-158">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f4032-159">IDL</span><span class="sxs-lookup"><span data-stu-id="f4032-159">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f4032-160"><dt>WaaSAPI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f4032-160"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




