---
title: Oggetto NetworkSettings
description: Per lo scripting, fornisce le impostazioni utilizzate dal Utilità di pianificazione per ottenere un profilo di rete.
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- Oggetto NetworkSettings Utilità di pianificazione
- Oggetto NetworkSettings Utilità di pianificazione , descritto
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
ms.openlocfilehash: ddc5e247ad3de50268c6075f8956687f92800c4e901788b5098a0cef868bb202
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759693"
---
# <a name="networksettings-object"></a>Oggetto NetworkSettings

Per lo scripting, fornisce le impostazioni utilizzate dal Utilità di pianificazione per ottenere un profilo di rete.

## <a name="members"></a>Membri

**L'oggetto NetworkSettings** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto NetworkSettings** ha queste proprietà.



| Proprietà                                        | Tipo di accesso           | Descrizione                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Id**](networksettings-id.md)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta un valore GUID che identifica un profilo di rete.<br/>                        |
| [**Nome**](networksettings-name.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta il nome di un profilo di rete. Il nome viene usato a scopo di visualizzazione. <br/> |



 

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML personalizzato per un'attività, le impostazioni di rete vengono specificate usando [**l'elemento NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) dello schema Utilità di pianificazione dati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione oggetti](task-scheduler-objects.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





