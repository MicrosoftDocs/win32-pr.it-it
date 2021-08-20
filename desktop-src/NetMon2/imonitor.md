---
description: L'interfaccia IMonitor fornisce metodi che controllano l'operazione di monitoraggio. Questi metodi vengono chiamati dal Servizio di controllo di monitoraggio (MCSVC).
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Interfaccia IMonitor (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 16199568473315fb61e53428d01c72032f3efff6ea0591bfd72ca2475f854fb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133102"
---
# <a name="imonitor-interface"></a>Interfaccia IMonitor

**L'interfaccia IMonitor** fornisce metodi che controllano l'operazione di monitoraggio. Questi metodi vengono chiamati dal [*Servizio di controllo di monitoraggio*](m.md) (MCSVC).

## <a name="members"></a>Membri

**L'interfaccia IMonitor** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMonitor** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IMonitor** include questi metodi.



| Metodo                                        | Descrizione                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**DoConfigure**](imonitor-doconfigure.md)   | Aggiorna la configurazione del monitoraggio.<br/>                                                                           |
| [**DoInitialize**](imonitor-doinitialize.md) | Inizializza un monitoraggio.<br/>                                                                                   |
| [**OnFrame**](imonitor-onframes.md)         | Indica lo stato di un evento frame.<br/>                                                                   |
| [**Onstart**](imonitor-onstart.md)           | Indica che il monitoraggio è stato configurato correttamente e che l'acquisizione dati sta per iniziare.<br/> |
| [**OnStatus**](imonitor-onstatus.md)         | Indica un evento di stato NPP.<br/>                                                                           |
| [**Onstop**](imonitor-onstop.md)             | Indica il completamento dell'acquisizione dati.<br/>                                                                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

