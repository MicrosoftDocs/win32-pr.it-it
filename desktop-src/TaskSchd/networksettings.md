---
title: Oggetto NetworkSettings
description: Per gli script, fornisce le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Utilità di pianificazione oggetto NetworkSettings
- Oggetto NetworkSettings Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1eecfbbdd4e3ea00c8d2412ae912594f2ec297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477201"
---
# <a name="networksettings-object"></a>Oggetto NetworkSettings

Per gli script, fornisce le impostazioni utilizzate dal servizio Utilità di pianificazione per ottenere un profilo di rete.

## <a name="members"></a>Membri

L'oggetto **NetworkSettings** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **NetworkSettings** dispone di queste proprietà.



| Proprietà                                        | Tipo di accesso           | Descrizione                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**ID**](networksettings-id.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta un valore GUID che identifica un profilo di rete.<br/>                        |
| [**Nome**](networksettings-name.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il nome di un profilo di rete. Il nome viene usato a scopo di visualizzazione. <br/> |



 

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, le impostazioni di rete vengono specificate usando l'elemento [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Utilità di pianificazione](task-scheduler-objects.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





