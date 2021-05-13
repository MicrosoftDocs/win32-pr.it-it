---
description: Implementato dal browser. Espone metodi che gestiscono quale monitoraggio contiene la barra delle applicazioni di Windows in un sistema a più monitor.
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
ms.openlocfilehash: 5ea3461d00c16f7384d7396e2f03946d517c460f
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841892"
---
# <a name="imultimonitordockingsite-interface"></a>Interfaccia IMultiMonitorDockingSite

Implementato dal browser. Espone metodi che gestiscono quale monitoraggio contiene la barra delle applicazioni di Windows in un sistema a più monitor.

## <a name="members"></a>Membri

**L'interfaccia IMultiMonitorDockingSite** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMultiMonitorDockingSite** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IMultiMonitorDockingSite** include questi metodi.



| Metodo                                                            | Descrizione                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetMonitor**](imultimonitordockingsite-getmonitor.md)         | Ottiene il monitoraggio predefinito corrente.<br/>                                               |
| [**RequestMonitor**](imultimonitordockingsite-requestmonitor.md) | Verifica che il monitoraggio sia attivo e disponibile.<br/>                              |
| [**SetMonitor**](imultimonitordockingsite-setmonitor.md)         | Modifica il monitor usato per le barre degli strumenti ancorate in un sistema a più monitor.<br/> |



 

## <a name="remarks"></a>Commenti

In genere non si implementa **l'interfaccia IMultiMonitorDockingSite.** Il browser shell implementa questa interfaccia per supportare più monitor.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, solo app desktop di Windows XP \[\]<br/> |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                   |



 

 
