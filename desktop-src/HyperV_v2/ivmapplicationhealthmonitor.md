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
ms.openlocfilehash: 3cc565c43fd61ebed6183cbfa2f4fdf7ece7d39872f23718fb1a12a3b591d531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694321"
---
# <a name="ivmapplicationhealthmonitor-interface"></a>Interfaccia IVmApplicationHealthMonitor

Segnala lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale ai componenti di integrazione di Hyper-V in esecuzione nella stessa macchina virtuale. Lo stato delle applicazioni in esecuzione nella macchina virtuale si riflette nel valore della proprietà **OperationalStatus** \[ 1 \] della classe [**Msvm \_ HeartbeatComponent.**](msvm-heartbeatcomponent.md) Questa interfaccia consente anche di reimpostare tutto lo stato dell'applicazione accumulato in Hyper-V.

Questa interfaccia viene implementata dal Windows 8 componenti di integrazione di Hyper-V. Un'istanza di questa interfaccia viene ottenuta creando un'istanza del CLSID **397a2e5f-348c-482d-b9a3-57d383b483cd.**

## <a name="members"></a>Membri

**L'interfaccia IVmApplicationHealthMonitor** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVmApplicationHealthMonitor** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IVmApplicationHealthMonitor** include questi metodi.



| Metodo                                                                                   | Descrizione                                                                              |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ResetAllApplicationState**](ivmapplicationhealthmonitor-resetallapplicationstate.md) | Reimposta lo stato di integrità per tutte le applicazioni in una macchina virtuale.<br/>            |
| [**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md)           | Imposta lo stato di integrità di un'applicazione in esecuzione in una macchina virtuale.<br/> |



 

## <a name="remarks"></a>Commenti

Per usare questo elemento di programmazione, è Windows 8 componenti di integrazione di nella macchina virtuale in cui è in esecuzione l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                                                                                                     |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                                                                                           |
| Versione<br/>                  | Componenti di integrazione per Windows 8<br/>                                                                                                                                |
| Idl<br/>                      | <dl> <dt>VmApplicationHealthMonitor.idl</dt> </dl>                                                                      |
| IID<br/>                      | IID \_ IVmApplicationHealthMonitor è definito come 267a0284-848f-447e-a096-5e10a1a76bca<br/> L'identificatore di oggetto è definito come 397a2e5f-348c-482d-b9a3-57d383b483cd<br/> |



 

