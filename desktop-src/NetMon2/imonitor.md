---
description: L'interfaccia IMonitor fornisce metodi che controllano l'operazione di monitoraggio. Questi metodi vengono chiamati dal servizio di controllo di monitoraggio (MCSVC).
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Interfaccia IMonitor (Netmon. h)
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
ms.openlocfilehash: 1b6ba91860905010fd14a46cd4608eaee3da80fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879914"
---
# <a name="imonitor-interface"></a>Interfaccia IMonitor

L'interfaccia **Imonitor** fornisce metodi che controllano l'operazione di monitoraggio. Questi metodi vengono chiamati dal [*servizio di controllo di monitoraggio*](m.md) (MCSVC).

## <a name="members"></a>Membri

L'interfaccia **Imonitor** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Imonitor** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **Imonitor** dispone di questi metodi.



| Metodo                                        | Descrizione                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**DoConfigure**](imonitor-doconfigure.md)   | Configurazione di monitoraggio aggiornamenti.<br/>                                                                           |
| [**DoInitialize**](imonitor-doinitialize.md) | Inizializza un monitoraggio.<br/>                                                                                   |
| [**Onframe**](imonitor-onframes.md)         | Indica lo stato di un evento frame.<br/>                                                                   |
| [**OnStart**](imonitor-onstart.md)           | Indica che il monitoraggio è stato configurato correttamente e che l'acquisizione dei dati sta per iniziare.<br/> |
| [**OnStatus**](imonitor-onstatus.md)         | Indica un evento di stato NPP.<br/>                                                                           |
| [**OnStop**](imonitor-onstop.md)             | Indica il completamento dell'acquisizione dei dati.<br/>                                                                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

