---
title: Interfaccia IRDVTaskPluginNotifySink
description: L'interfaccia IRDVTaskPluginNotifySink viene usata dall'agente attività per comunicare con l'agente trigger.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88692175fedbad4faf5b2755ce92897cff25fe9d588e6fb446d8174407aa6b5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072391"
---
# <a name="irdvtaskpluginnotifysink-interface"></a>Interfaccia IRDVTaskPluginNotifySink

**L'interfaccia IRDVTaskPluginNotifySink** viene usata dall'agente attività per comunicare con l'agente trigger. Un puntatore a questa interfaccia viene passato all'agente attività nel [**metodo IRDVTaskPlugin::Initialize.**](irdvtaskplugin-initialize.md)

## <a name="members"></a>Membri

**L'interfaccia IRDVTaskPluginNotifySink** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRDVTaskPluginNotifySink** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IRDVTaskPluginNotifySink.**



| Metodo                                                                  | Descrizione                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**DeleteSchedule**](irdvtaskpluginnotifysink-deleteschedule.md)       | Chiamato dall'agente attività per eliminare un'attività pianificata.<br/>                   |
| [**OnTaskStateChange**](irdvtaskpluginnotifysink-ontaskstatechange.md) | Usato per notificare all'agente trigger che lo stato di un'attività è stato modificato.<br/> |
| [**OnTerminated**](irdvtaskpluginnotifysink-onterminated.md)           | Chiamato dall'agente attività per richiedere l'arresto dell'agente attività.<br/>  |
| [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md)           | Chiamato dall'agente attività per pianificare un'attività.<br/>                           |



 

## <a name="remarks"></a>Commenti

Anche se questa interfaccia è supportata nei sistemi operativi identificati nei requisiti seguenti, verrà usata solo se la macchina virtuale è ospitata in Windows Server 2012.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise<br/>   |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/> |



 

