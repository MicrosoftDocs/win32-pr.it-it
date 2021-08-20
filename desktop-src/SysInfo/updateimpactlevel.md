---
description: Indica un impatto alto, medio o basso di un dispositivo che esegue un sistema operativo non aggiornato.
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
ms.openlocfilehash: 3b0d2145f649cfdbd6c652213b95f0051a1d9d408d5ad4ef17a703c86b83781a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957669"
---
# <a name="updateimpactlevel-enumeration"></a>Enumerazione UpdateImpactLevel

Indica un impatto alto, medio o basso di un dispositivo che esegue un sistema operativo non aggiornato. Questa enumerazione viene in genere usata dalle strutture [**UpdateAssessment,**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) che a loro volta sono annidate all'interno dell'oggetto [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) restituito da [**GetOSUpdateAssessment.**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment)

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

<span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**UpdateImpactLevel \_ Nessuno**
</dt> <dd>

Non vi è alcun impatto prevedibile sul dispositivo. Ciò può essere dovuto al fatto che il dispositivo è aggiornato o non è aggiornato perché il dispositivo rispetta i periodi di differimento di Windows Update for Business oppure non è aggiornato ma non ha ancora raggiunto la soglia **daysOutOfDate** per raggiungere un livello di impatto superiore.

</dd> <dt>

<span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel \_ Low**
</dt> <dd>

Il dispositivo non esegue il sistema operativo più recente, ma ha un aggiornamento recente.

</dd> <dt>

<span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**UpdateImpactLevel \_ Media**
</dt> <dd>

Il dispositivo esegue il sistema operativo più recente, ma ha un aggiornamento moderatamente recente.

</dd> <dt>

<span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel \_ High**
</dt> <dd>

Il dispositivo non è aggiornato da molto tempo. Questo dispositivo può avere vulnerabilità di sicurezza e potrebbe non essere in grado di apportare correzioni importanti che Windows migliori. Quando un dispositivo esegue una versione di Windows non più supportata, viene sempre restituito **UpdateImpactLevel \_ High.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando [**viene chiamato GetOSUpdateAssessment,**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) viene [**restituita una struttura OSUpdateAssessment.**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) All'interno della struttura sono presenti **assessmentForCurrent** e **assessmentForUpToDate.** Entrambe sono [**strutture UpdateAssessment.**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) Entrambi i membri hanno **un'enumerazione UpdateImpactLevel,** che indica un impatto alto, medio, basso o nessun impatto per un dispositivo che esegue un sistema operativo non aggiornato. Questi livelli sono determinati dal valore di **daysOutOfDate.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                              |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                   |
| Idl<br/>                      | <dl> <dt>WaaSAPI.idl</dt> </dl> |



 

 




