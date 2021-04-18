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
# <a name="updateassessmentstatus-enumeration"></a>Enumerazione UpdateAssessmentStatus

Viene descritto come aggiornare il sistema operativo in un dispositivo. **UpdateAssessmentStatus** viene usato dalle strutture [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) e [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) nei membri **assessmentForCurrent**, **assessmentForUpToDate** e **securityStatus** . Viene restituita esattamente una costante.

## <a name="syntax"></a>Sintassi


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



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="____UpdateAssessmentStatus_Latest"></span><span id="____updateassessmentstatus_latest"></span><span id="____UPDATEASSESSMENTSTATUS_LATEST"></span>**UpdateAssessmentStatus \_ Più recente**
</dt> <dd>

Questo risultato in **assessmentForCurrent** implica che il dispositivo si trovi nell'aggiornamento delle funzionalità più recente e nell'aggiornamento qualitativo disponibile per il dispositivo. All'interno di **assessmentForUpToDate**, questo risultato implica che il dispositivo si trovi nell'ultimo aggiornamento qualitativo per la versione di Windows in esecuzione.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestSoftRestriction"></span><span id="____updateassessmentstatus_notlatestsoftrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSOFTRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestSoftRestriction**
</dt> <dd>

L'aggiornamento delle funzionalità più recente non è stato installato a causa di una restrizione flessibile. Quando una restrizione Soft è stata inserita in un aggiornamento, l'aggiornamento non verrà installato automaticamente; un utente deve avviare autonomamente il download all'interno dell'esperienza utente di aggiornamento. Questo stato si applica solo a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestHardRestriction"></span><span id="____updateassessmentstatus_notlatesthardrestriction"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTHARDRESTRICTION"></span>**UpdateAssessmentStatus \_ NotLatestHardRestriction**
</dt> <dd>

L'aggiornamento delle funzionalità più recente non è stato installato a causa di una restrizione rigida. Quando è stata applicata una restrizione rigida a un aggiornamento, l'aggiornamento non è applicabile al dispositivo. Questo stato si applica solo a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestEndOfSupport"></span><span id="____updateassessmentstatus_notlatestendofsupport"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTENDOFSUPPORT"></span>**UpdateAssessmentStatus \_ NotLatestEndOfSupport**
</dt> <dd>

Il dispositivo non si trova nell'aggiornamento più recente perché l'aggiornamento delle funzionalità del dispositivo non è più supportato da Microsoft. Quando Microsoft smette di supportare una versione di funzionalità, questo stato verrà restituito sia per **assessmentForCurrent** che per **assessmentForUpToDate**.

> [!Note]  
> Quando viene restituito **UpdateAssessmentStatus \_ NotLatestEndOfSupport** , il **UpdateImpactLevel** della valutazione è sempre **UpdateImpactLevel \_ elevato**.

 

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestServicingTrain"></span><span id="____updateassessmentstatus_notlatestservicingtrain"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTSERVICINGTRAIN"></span>**UpdateAssessmentStatus \_ NotLatestServicingTrain**
</dt> <dd>

Il dispositivo non si trova nell'aggiornamento delle funzionalità più recente perché il training di manutenzione del dispositivo limita l'aggiornamento del dispositivo all'aggiornamento delle funzionalità più recente. Ad esempio, se un dispositivo è in Current Branch for Business (CBB) ed è stato rilasciato un nuovo aggiornamento della funzionalità per Current Branch (CB), verrà restituito. Questo stato si applica solo a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredFeature"></span><span id="____updateassessmentstatus_notlatestdeferredfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestDeferredFeature**
</dt> <dd>

L'aggiornamento delle funzionalità più recente non è stato installato a causa dei criteri di rinvio degli aggiornamenti delle funzionalità di Windows Update del dispositivo. La determinazione di **daysOutOfDate** prende in considerazione i criteri di rinvio. **daysOutOfDate** non inizierà l'incremento fino alla scadenza del periodo di differimento. Questo stato si applica solo a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestDeferredQuality"></span><span id="____updateassessmentstatus_notlatestdeferredquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTDEFERREDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestDeferredQuality**
</dt> <dd>

Il dispositivo non si trova nell'aggiornamento di qualità più recente a causa dei criteri di rinvio degli aggiornamenti di qualità dell'Windows Update del dispositivo. La determinazione di **daysOutOfDate** prende in considerazione i criteri di rinvio. **daysOutOfDate** non inizierà l'incremento fino alla scadenza del periodo di differimento.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedFeature"></span><span id="____updateassessmentstatus_notlatestpausedfeature"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDFEATURE"></span>**UpdateAssessmentStatus \_ NotLatestPausedFeature**
</dt> <dd>

Il dispositivo non si trova nell'aggiornamento delle funzionalità più recente a causa del dispositivo con aggiornamenti delle funzionalità sospesi. Se un dispositivo è sospeso non viene inserito nel calcolo di **daysOutOfDate**. Questo stato si applica solo a **assessmentForCurrent**.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestPausedQuality"></span><span id="____updateassessmentstatus_notlatestpausedquality"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTPAUSEDQUALITY"></span>**UpdateAssessmentStatus \_ NotLatestPausedQuality**
</dt> <dd>

Il dispositivo non si trova nell'aggiornamento di qualità più recente a causa del dispositivo con aggiornamenti di qualità sospesi. Se un dispositivo è sospeso non viene inserito nel calcolo di **daysOutOfDate**. **daysOutOfDate** non determina se un dispositivo viene sospeso nel calcolo.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestManaged"></span><span id="____updateassessmentstatus_notlatestmanaged"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTMANAGED"></span>**UpdateAssessmentStatus \_ NotLatestManaged**
</dt> <dd>

Il dispositivo non si trova nell'aggiornamento più recente perché l'approvazione degli aggiornamenti non viene eseguita tramite Windows Update.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestUnknown"></span><span id="____updateassessmentstatus_notlatestunknown"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTUNKNOWN"></span>**UpdateAssessmentStatus \_ NotLatestUnknown**
</dt> <dd>

Il dispositivo non si trova nell'aggiornamento più recente a causa di un motivo che non può essere determinato dalla valutazione.

</dd> <dt>

<span id="____UpdateAssessmentStatus_NotLatestTargetedVersion"></span><span id="____updateassessmentstatus_notlatesttargetedversion"></span><span id="____UPDATEASSESSMENTSTATUS_NOTLATESTTARGETEDVERSION"></span>**UpdateAssessmentStatus \_ NotLatestTargetedVersion**
</dt> <dd>

Il dispositivo non si trova nell'aggiornamento delle funzionalità più recente a causa dei criteri della versione di destinazione Windows Update per business del dispositivo. Questo criterio mantiene il dispositivo nella versione di rilascio della funzionalità di destinazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene usata più spesso con le strutture [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) e [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) , che a loro volta vengono usate con il metodo [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) per [**IWaaSAssessor**](/windows/desktop/api/waasapi/nn-waasapi-iwaasassessor).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                   |
| IDL<br/>                      | <dl> <dt>WaaSAPI. idl</dt> </dl> |



 

 




