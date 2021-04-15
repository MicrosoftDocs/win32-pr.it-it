---
title: Interfaccia IVMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Definisce l'interfaccia evento in uscita per l'interfaccia IVMVirtualMachine.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- Interfaccia IVMVirtualMachineEvents Virtual PC
- Interfaccia IVMVirtualMachineEvents Virtual PC, descritta
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2ded96f5a39a520d3b5a712e63fbb0a65d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478670"
---
# <a name="ivmvirtualmachineevents-interface"></a>Interfaccia IVMVirtualMachineEvents

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Definisce l'interfaccia evento in uscita per l'interfaccia [**IVMVirtualMachine**](ivmvirtualmachine.md) . Il client implementa questi metodi per ricevere gli eventi inviati da [**IVMVirtualMachine**](ivmvirtualmachine.md).

## <a name="members"></a>Membri

L'interfaccia **IVMVirtualMachineEvents** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachineEvents** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IVMVirtualMachineEvents** dispone di questi metodi.



| Metodo                                                                                   | Descrizione                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdditionsAvailable**](ivmvirtualmachineevents-onadditionsavailable.md)             | Riceve la notifica che i componenti di integrazione sono disponibili in una macchina virtuale.<br/>                                                |
| [**OnAdditionsUninstalled**](ivmvirtualmachineevents-onadditionsuninstalled.md)         | Riceve una notifica di disinstallazione dei componenti di integrazione in una macchina virtuale.<br/>                                              |
| [**OnConfigurationChanged**](ivmvirtualmachineevents-onconfigurationchanged.md)         | Riceve la notifica che un valore nella configurazione per questa macchina virtuale è stato modificato.<br/>                                        |
| [**OnDiskOutOfSpace**](ivmvirtualmachineevents-ondiskoutofspace.md)                     | Riceve una notifica che indica che un disco richiesto per una macchina virtuale è insufficiente e non è possibile eseguire la macchina virtuale.<br/>           |
| [**OnEnhancedVideoModeChanged**](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | Riceve una notifica della modifica del supporto di una macchina virtuale per la modalità video avanzata.<br/>                                          |
| [**OnGuestLogoff**](ivmvirtualmachineevents-onguestlogoff.md)                           | Riceve la notifica che un utente si è disconnesso dal sistema operativo guest.<br/>                                                    |
| [**OnGuestShutdown**](ivmvirtualmachineevents-onguestshutdown.md)                       | Riceve la notifica che il sistema operativo guest è stato arrestato.<br/>                                                                     |
| [**OnHeartbeatStopped**](ivmvirtualmachineevents-onheartbeatstopped.md)                 | Riceve una notifica di arresto dell'heartbeat di una macchina virtuale. Ciò indica in genere che si è verificato un arresto anomalo del sistema operativo guest.<br/> |
| [**OnRequestShutdown**](ivmvirtualmachineevents-onrequestshutdown.md)                   | Riceve la notifica che è stata effettuata una richiesta di arresto.<br/>                                                                         |
| [**OnReset**](ivmvirtualmachineevents-onreset.md)                                       | Riceve la notifica che una macchina virtuale è stata reimpostata.<br/>                                                                         |
| [**OnStateChange**](ivmvirtualmachineevents-onstatechange.md)                           | Riceve una notifica che lo stato di una macchina virtuale è stato modificato.<br/>                                                                    |
| [**OnTripleFault**](ivmvirtualmachineevents-ontriplefault.md)                           | Riceve una notifica che una macchina virtuale presenta tre errori.<br/>                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4<br/>   |



 

