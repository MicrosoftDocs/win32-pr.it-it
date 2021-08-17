---
description: L'interfaccia IMonitorEventer fornisce metodi per inviare eventi e allocare e liberare risorse di monitoraggio.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Interfaccia IMonitorEventer (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 2af49529a74c23e0f4d4e77e0d2608cd44d12028d93022750fbbd3af891e2e77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365489"
---
# <a name="imonitoreventer-interface"></a>Interfaccia IMonitorEventer

**L'interfaccia IMonitorEventer** fornisce metodi per inviare eventi e allocare e liberare risorse di monitoraggio.

## <a name="members"></a>Membri

**L'interfaccia IMonitorEventer** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMonitorEventer** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IMonitorEventer** include questi metodi.



| Metodo                                                 | Descrizione                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [**FreeEventData**](imonitoreventer-freeeventdata.md) | Libera lo spazio allocato per i dati di monitoraggio.<br/> |
| [**GetEventData**](imonitoreventer-geteventdata.md)   | Alloca spazio per i dati di monitoraggio.<br/>       |
| [**SendNMEvent**](imonitoreventer-sendnmevent.md)     | Invia eventi a WMI.<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

