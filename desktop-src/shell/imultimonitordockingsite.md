---
description: Implementato dal browser. Espone i metodi che gestiscono quale monitoraggio contiene il Windows barra delle applicazioni in un sistema a più monitor.
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
ms.openlocfilehash: a5a17e8206af8f0821833f4b2ea250606de29b6fbe74b7a29ced6c5b5dc13ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458221"
---
# <a name="imultimonitordockingsite-interface"></a>Interfaccia IMultiMonitorDockingSite

Implementato dal browser. Espone i metodi che gestiscono quale monitoraggio contiene il Windows barra delle applicazioni in un sistema a più monitor.

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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                   |



 

 
