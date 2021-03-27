---
description: Implementato dal browser. Espone metodi che gestiscono il monitoraggio che contiene la barra delle applicazioni di Windows in un sistema a più monitor.
title: Interfaccia IMultiMonitorDockingSite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: 3aa1ccb1c25fd2896ce9e18ba52ea3f46b1882af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995197"
---
# <a name="imultimonitordockingsite-interface"></a>Interfaccia IMultiMonitorDockingSite

Implementato dal browser. Espone metodi che gestiscono il monitoraggio che contiene la barra delle applicazioni di Windows in un sistema a più monitor.

## <a name="members"></a>Membri

L'interfaccia **IMultiMonitorDockingSite** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMultiMonitorDockingSite** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IMultiMonitorDockingSite** dispone di questi metodi.



| Metodo                                                            | Descrizione                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Getmonitor**](imultimonitordockingsite-getmonitor.md)         | Ottiene il monitoraggio predefinito corrente.<br/>                                               |
| [**RequestMonitor**](imultimonitordockingsite-requestmonitor.md) | Verifica che il monitoraggio sia attivo e disponibile.<br/>                              |
| [**Monitoraggio di**](imultimonitordockingsite-setmonitor.md)         | Modifica il monitoraggio usato per le barre degli strumenti ancorate in un sistema a più monitor.<br/> |



 

## <a name="remarks"></a>Commenti

In genere l'interfaccia **IMultiMonitorDockingSite** non viene implementata. Il browser della shell implementa questa interfaccia per supportare più monitor.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                   |



 

 
