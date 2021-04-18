---
description: Segnala lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale ai componenti di integrazione di Hyper-V in esecuzione nella stessa macchina virtuale.
ms.assetid: C463391B-669C-4CBA-9EC7-7E0ABC5A63A1
title: Interfaccia IVmApplicationHealthMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: ac9f6574dd8261a120e434cc0351fd07985c71a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309505"
---
# <a name="ivmapplicationhealthmonitor-interface"></a>Interfaccia IVmApplicationHealthMonitor

Segnala lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale ai componenti di integrazione di Hyper-V in esecuzione nella stessa macchina virtuale. Lo stato delle applicazioni in esecuzione nella macchina virtuale si riflette nel  \[ \] valore della proprietà OperationalStatus 1 della classe [**MSVM \_ HeartbeatComponent**](msvm-heartbeatcomponent.md) . Questa interfaccia fornisce anche un modo per reimpostare lo stato dell'applicazione accumulato in Hyper-V.

Questa interfaccia viene implementata dai componenti di integrazione di Hyper-V per Windows 8. Un'istanza di questa interfaccia viene ottenuta creando un'istanza del CLSID **397a2e5f-348c-482d-b9a3-57d383b483cd** .

## <a name="members"></a>Membri

L'interfaccia **IVmApplicationHealthMonitor** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVmApplicationHealthMonitor** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IVmApplicationHealthMonitor** dispone di questi metodi.



| Metodo                                                                                   | Descrizione                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ResetAllApplicationState**](ivmapplicationhealthmonitor-resetallapplicationstate.md) | Reimposta lo stato di integrità di tutte le applicazioni in una macchina virtuale.<br/>            |
| [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md)           | Imposta lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale.<br/> |



 

## <a name="remarks"></a>Commenti

Per utilizzare questo elemento di programmazione, è necessario installare i componenti di integrazione di Windows 8 nella macchina virtuale in cui è in esecuzione l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                                                                                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                                                                                           |
| Versione<br/>                  | Componenti di integrazione per Windows 8<br/>                                                                                                                                |
| IDL<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl>                                                                      |
| IID<br/>                      | IID \_ IVmApplicationHealthMonitor è definito come 267a0284-848f-447e-A096-5e10a1a76bca<br/> Identificatore di oggetto definito come 397a2e5f-348c-482d-b9a3-57d383b483cd<br/> |



 

