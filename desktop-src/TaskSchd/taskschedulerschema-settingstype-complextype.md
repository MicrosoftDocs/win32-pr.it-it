---
title: Tipo complesso settingsType
description: Definisce gli elementi figlio e le informazioni di sequenziazione per Impostazioni elemento (taskType).
ms.assetid: dba6b82d-aaa4-4f77-aeb1-c5a8f81aec25
keywords:
- Tipo complesso settingsType Utilità di pianificazione
topic_type:
- apiref
api_name:
- settingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a48a124230a27a0c23cc9c2a9fa983b6ef3088b8ec22e8ac03fc371caadf0f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356353"
---
# <a name="settingstype-complex-type"></a>Tipo complesso settingsType

Definisce gli elementi figlio e le informazioni di sequenziazione per [**Impostazioni elemento (taskType).**](taskschedulerschema-settings-tasktype-element.md)

``` syntax
<xs:complexType name="settingsType">
    <xs:all>
        <xs:element name="AllowStartOnDemand"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnFailure"
            type="restartType"
            minOccurs="0"
         />
        <xs:element name="MultipleInstancesPolicy"
            type="multipleInstancesPolicyType"
            default="IgnoreNew"
            minOccurs="0"
         />
        <xs:element name="DisallowStartIfOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StopIfGoingOnBatteries"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="AllowHardTerminate"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="StartWhenAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="NetworkProfileName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfNetworkAvailable"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="WakeToRun"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="Enabled"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="Hidden"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DeleteExpiredTaskAfter"
            type="duration"
            default="PT0S"
            minOccurs="0"
         />
        <xs:element name="IdleSettings"
            type="idleSettingsType"
            minOccurs="0"
         />
        <xs:element name="NetworkSettings"
            type="networkSettingsType"
            minOccurs="0"
         />
        <xs:element name="ExecutionTimeLimit"
            type="duration"
            minOccurs="0"
         />
        <xs:element name="Priority"
            type="priorityType"
            default="7"
            minOccurs="0"
         />
        <xs:element name="RunOnlyIfIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="UseUnifiedSchedulingEngine"
            type="boolean"
            default="false"
            minOccurs="0"
         />
        <xs:element name="DisallowStartOnRemoteAppSession"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                                             | Tipo                                                                                              | Descrizione                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md)                           | boolean                                                                                           | Specifica se il servizio Utilità di pianificazione consente la terminazione rigida dell'attività.<br/>                                                                                                                                                                                                                             |
| [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md)                           | boolean                                                                                           | Specifica che l'attività può essere avviata usando il comando Esegui o il menu di scelta rapida. <br/>                                                                                                                                                                                                             |
| [**DeleteExpiredTaskAfter**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md)                   | duration                                                                                          | Specifica la quantità di tempo di attesa del Utilità di pianificazione prima di eliminare l'attività dopo la scadenza. Se non viene specificato alcun valore per questo elemento, il Utilità di pianificazione non eliminerà l'attività.<br/>                                                                                           |
| [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md)           | boolean                                                                                           | Specifica che l'attività non verrà avviata se il computer è alimentato a batteria.<br/>                                                                                                                                                                                                                 |
| [**DisallowStartOnRemoteAppSession**](taskschedulerschema-disallowstartonremoteappsession-settingstype-element.md) | boolean                                                                                           | Specifica che l'attività non deve essere avviata se l'attività viene attivata per l'esecuzione in una sessione RAIL (Remote Applications Integrated Locally).<br/>                                                                                                                                                                     |
| [**Abilitato**](taskschedulerschema-enabled-settingstype-element.md)                                                 | boolean                                                                                           | Specifica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è **True.**<br/>                                                                                                                                                                                                        |
| [**ExecutionTimeLimit**](taskschedulerschema-executiontimelimit-settingstype-element.md)                           | duration                                                                                          | Specifica la quantità di tempo consentita per completare l'attività.<br/>                                                                                                                                                                                                                                               |
| [**Nascosto**](taskschedulerschema-hidden-settingstype-element.md)                                                   | boolean                                                                                           | Specifica, per impostazione predefinita, che l'attività non sarà visibile nell'interfaccia utente.<br/>                                                                                                                                                                                                                     |
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md)                                       | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md)                      | Specifica il modo in cui Utilità di pianificazione le attività quando il computer è in uno stato di inattività.<br/>                                                                                                                                                                                                                   |
| [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)                 | [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) | Specifica i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività. <br/>                                                                                                                                                                                                     |
| [**NetworkProfileName**](taskschedulerschema-networkprofilename-settingstype-element.md)                           | string                                                                                            | Specifica il nome di un profilo di rete. Il Utilità di pianificazione verifica la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **True.** Il nome viene usato a scopo di visualizzazione.<br/>        |
| [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md)                                 | [**networkSettingsType**](taskschedulerschema-networksettingstype-complextype.md)                | Specifica le impostazioni utilizzate dal Utilità di pianificazione per ottenere un profilo di rete. Il Utilità di pianificazione controlla la disponibilità di questa rete quando l'elemento [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md) è impostato su **True.**<br/> |
| [**Priority**](taskschedulerschema-priority-settingstype-element.md)                                               | [**priorityType**](taskschedulerschema-prioritytype-simpletype.md)                               | Specifica il livello di priorità per l'attività.<br/>                                                                                                                                                                                                                                                               |
| [**RestartOnFailure**](taskschedulerschema-restartonfailure-settingstype-element.md)                               | [**restartType**](taskschedulerschema-restarttype-complextype.md)                                | Specifica che il Utilità di pianificazione tenterà di riavviare l'attività se per qualsiasi motivo ha esito negativo. <br/>                                                                                                                                                                                                          |
| [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md)                                     | boolean                                                                                           | Specifica che l'attività viene eseguita solo quando il computer è in uno stato di inattività.<br/>                                                                                                                                                                                                                               |
| [**RunOnlyIfNetworkAvailable**](taskschedulerschema-runonlyifnetworkavailable-settingstype-element.md)             | boolean                                                                                           | Specifica che il Utilità di pianificazione eseguirà l'attività solo quando è disponibile una rete.<br/>                                                                                                                                                                                                                    |
| [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md)                           | boolean                                                                                           | Specifica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorsa l'ora pianificata.<br/>                                                                                                                                                                                                    |
| [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md)                   | boolean                                                                                           | Specifica che l'attività verrà arrestata se il computer passa all'alimentazione a batteria. <br/>                                                                                                                                                                                                                      |
| [**UseUnifiedSchedulingEngine**](taskschedulerschema-useunifiedschedulingengine-settingstype-element.md)           | boolean                                                                                           | Specifica che l'attività viene eseguita tramite il motore di pianificazione unificato.<br/>                                                                                                                                                                                                                                   |
| [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md)                                             | boolean                                                                                           | Specifica che Utilità di pianificazione riattiva il computer prima di eseguire l'attività.<br/>                                                                                                                                                                                                                            |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione complessi dello schema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





