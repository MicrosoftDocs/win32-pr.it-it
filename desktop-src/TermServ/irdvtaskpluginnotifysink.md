---
title: Interfaccia IRDVTaskPluginNotifySink
description: L'interfaccia IRDVTaskPluginNotifySink viene utilizzata dall'agente attività per comunicare con l'agente di trigger.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0dadaf387fcf6e8381404440e0d31dd210b9f8a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742071"
---
# <a name="irdvtaskpluginnotifysink-interface"></a>Interfaccia IRDVTaskPluginNotifySink

L'interfaccia **IRDVTaskPluginNotifySink** viene utilizzata dall'agente attività per comunicare con l'agente di trigger. Un puntatore a questa interfaccia viene passato all'agente attività nel metodo [**IRDVTaskPlugin:: Initialize**](irdvtaskplugin-initialize.md) .

## <a name="members"></a>Membri

L'interfaccia **IRDVTaskPluginNotifySink** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRDVTaskPluginNotifySink** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IRDVTaskPluginNotifySink** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**DeleteSchedule**](irdvtaskpluginnotifysink-deleteschedule.md)       | Chiamato dall'agente attività per eliminare un'attività pianificata.<br/>                   |
| [**OnTaskStateChange**](irdvtaskpluginnotifysink-ontaskstatechange.md) | Utilizzato per notificare all'agente del trigger che lo stato di un'attività è stato modificato.<br/> |
| [**Con terminazione**](irdvtaskpluginnotifysink-onterminated.md)           | Chiamato dall'agente attività per richiedere l'arresto dell'agente attività.<br/>  |
| [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md)           | Chiamato dall'agente attività per pianificare un'attività.<br/>                           |



 

## <a name="remarks"></a>Commenti

Sebbene questa interfaccia sia supportata nei sistemi operativi indicati nei requisiti indicati di seguito, verrà usata solo se la macchina virtuale è ospitata in Windows Server 2012.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise<br/>   |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/> |



 

