---
description: Indica un effetto elevato, medio o basso di un dispositivo che esegue un sistema operativo non aggiornato.
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
title: Enumerazione UpdateImpactLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateImpactLevel
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: c18cc7916abbc1dce595df9a21d2fdef3976af11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308091"
---
# <a name="updateimpactlevel-enumeration"></a>Enumerazione UpdateImpactLevel

Indica un effetto elevato, medio o basso di un dispositivo che esegue un sistema operativo non aggiornato. Questa enumerazione viene in genere utilizzata dalle strutture [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) , che a sua volta sono annidate all'interno dell' [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) restituito da [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).

## <a name="syntax"></a>Sintassi


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**UpdateImpactLevel \_ Nessuna**
</dt> <dd>

Non è previsto alcun effetto sul dispositivo. Questo problema può essere dovuto al fatto che il dispositivo è aggiornato o non è aggiornato perché il dispositivo sta rispettando la Windows Update per i periodi di differimento aziendali oppure è obsoleto ma non ha ancora raggiunto la soglia **daysOutOfDate** per raggiungere un livello di inattività maggiore.

</dd> <dt>

<span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel \_ basso**
</dt> <dd>

Il dispositivo non esegue il sistema operativo più recente, ma ha un aggiornamento recente.

</dd> <dt>

<span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**UpdateImpactLevel \_ Media**
</dt> <dd>

Nel dispositivo è in esecuzione il sistema operativo più recente, ma è presente un aggiornamento moderatamente recente.

</dd> <dt>

<span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel- \_ alto**
</dt> <dd>

Il dispositivo è obsoleto per molto tempo. Questo dispositivo potrebbe avere vulnerabilità di sicurezza e potrebbero mancare correzioni importanti che rendono Windows migliore. Quando un dispositivo esegue una versione di Windows che non è più supportata, viene sempre restituito **UpdateImpactLevel \_ High** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando viene chiamato [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) , viene restituita una struttura [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) . All'interno della struttura sono presenti **assessmentForCurrent** e **assessmentForUpToDate**. Entrambe sono strutture [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) . Entrambi i membri hanno un'enumerazione **UpdateImpactLevel** , che indica un livello elevato, medio, basso o nessun effetto per un dispositivo che esegue un sistema operativo non aggiornato. Questi livelli sono determinati dal valore di **daysOutOfDate**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                   |
| IDL<br/>                      | <dl> <dt>WaaSAPI. idl</dt> </dl> |



 

 




