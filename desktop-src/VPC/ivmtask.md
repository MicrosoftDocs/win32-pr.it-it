---
title: Interfaccia IVMTask (VPCCOMInterfaces.h)
description: Usare l'interfaccia IVMTask per monitorare e controllare le attività asincrone per vari metodi COM.
ms.assetid: 9b593444-80f5-43e9-9b95-1a2150c66efd
keywords:
- Interfaccia IVMTask Virtual PC
- Interfaccia IVMTask Virtual PC , descritta
topic_type:
- apiref
api_name:
- IVMTask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6e7afa39e8e95ac2a961212b3a3fe7b74e73bc8b1100ac44b34d09700ab58bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998721"
---
# <a name="ivmtask-interface"></a>Interfaccia IVMTask

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Usare **l'interfaccia IVMTask** per monitorare e controllare le attività asincrone per vari metodi COM.

## <a name="members"></a>Membri

**L'interfaccia IVMTask** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMTask** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IVMTask** include questi metodi.



| Metodo                                                 | Descrizione                                                                                 |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Annulla**](ivmtask-cancel.md)                       | Annulla l'attività.<br/>                                                                |
| [**WaitForCompletion**](ivmtask-waitforcompletion.md) | Attende il completamento dell'attività o la scadenza dell'intervallo di timeout specificato.<br/> |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IVMTask** ha queste proprietà.



| Proprietà                                                        | Tipo di accesso          | Descrizione                                                        |
|:----------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [**Descrizione**](ivmtask-description.md)<br/>           | Sola lettura<br/> | Descrizione dell'attività.<br/>                              |
| [**Errore**](ivmtask-error.md)<br/>                       | Sola lettura<br/> | Errore registrato per questa attività.<br/>                       |
| [**ErrorDescription**](ivmtask-errordescription.md)<br/> | Sola lettura<br/> | Descrizione dell'errore localizzata registrata per questa attività.<br/> |
| [**ID**](ivmtask-id.md)<br/>                             | Sola lettura<br/> | Identificatore univoco per questa attività.<br/>                      |
| [**IsCancelable**](ivmtask-iscancelable.md)<br/>         | Sola lettura<br/> | Indica se l'attività può essere annullata.<br/>             |
| [**IsComplete**](ivmtask-iscomplete.md)<br/>             | Sola lettura<br/> | Indica se l'attività è stata completata.<br/>               |
| [**PercentCompleted**](ivmtask-percentcompleted.md)<br/> | Sola lettura<br/> | Percentuale di completamento dell'attività.<br/>                  |
| [**Risultato**](ivmtask-result.md)<br/>                     | Sola lettura<br/> | Risultato dell'attività.<br/>                                 |



 

## <a name="remarks"></a>Commenti

Un **oggetto IVMTask** viene restituito da metodi che potrebbero potenzialmente richiedere una quantità significativa di tempo per il completamento. In questo modo l'applicazione può monitorare lo stato dell'operazione desiderata senza forzarla a bloccare l'ulteriore esecuzione in attesa del completamento dell'operazione.

I metodi seguenti restituiscono un **oggetto IVMTask** che può essere usato per tenere traccia dello stato di avanzamento:

-   [**IVMGuestOS::Logoff**](ivmguestos-logoff.md)
-   [**IVMGuestOS::Restart**](ivmguestos-restart.md)
-   [**IVMGuestOS::Shutdown**](ivmguestos-shutdown.md)
-   [**IVMHardDisk::Compact**](ivmharddisk-compact.md)
-   [**IVMHardDisk::Convert**](ivmharddisk-convert.md)
-   [**IVMHardDisk::Merge**](ivmharddisk-merge.md)
-   [**IVMHardDisk::MergeTo**](ivmharddisk-mergeto.md)
-   [**IVMVirtualMachine::MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)
-   [**IVMVirtualMachine::Reset**](ivmvirtualmachine-reset.md)
-   [**IVMVirtualMachine::Save**](ivmvirtualmachine-save.md)
-   [**IVMVirtualMachine::Startup**](ivmvirtualmachine-startup.md)
-   [**IVMVirtualMachine::Startup2**](ivmvirtualmachine-startup2.md)
-   [**IVMVirtualMachine::TurnOff**](ivmvirtualmachine-turnoff.md)
-   [**IVMVirtualPC::CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md)
-   [**IVMVirtualPC::CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)
-   [**IVMVirtualPC::CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



 

