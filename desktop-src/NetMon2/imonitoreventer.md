---
description: L'interfaccia IMonitorEventer fornisce metodi per l'invio di eventi e l'allocazione e la liberazione di risorse di monitoraggio.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Interfaccia IMonitorEventer (Netmon. h)
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
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879054"
---
# <a name="imonitoreventer-interface"></a>Interfaccia IMonitorEventer

L'interfaccia **IMonitorEventer** fornisce metodi per l'invio di eventi e l'allocazione e la liberazione di risorse di monitoraggio.

## <a name="members"></a>Membri

L'interfaccia **IMonitorEventer** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMonitorEventer** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IMonitorEventer** dispone di questi metodi.



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
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

