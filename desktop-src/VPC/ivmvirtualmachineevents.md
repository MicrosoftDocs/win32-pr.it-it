---
title: Interfaccia IVMVirtualMachineEvents (VPCCOMInterfaces.h)
description: Definisce l'interfaccia eventi in uscita per l'interfaccia IVMVirtualMachine.
ms.assetid: 52901a95-0f4f-4503-97c5-1459179feeb8
keywords:
- Interfaccia IVMVirtualMachineEvents Virtual PC
- Interfaccia IVMVirtualMachineEvents Virtual PC , descritta
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
ms.openlocfilehash: c6686585333f33d4732284ab448a82ac722fea03315b08aaa276f2eeabaf2e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122621"
---
# <a name="ivmvirtualmachineevents-interface"></a>Interfaccia IVMVirtualMachineEvents

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Definisce l'interfaccia eventi in uscita per [**l'interfaccia IVMVirtualMachine.**](ivmvirtualmachine.md) Il client implementa questi metodi per ricevere gli eventi inviati da [**IVMVirtualMachine.**](ivmvirtualmachine.md)

## <a name="members"></a>Membri

**L'interfaccia IVMVirtualMachineEvents** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMVirtualMachineEvents** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IVMVirtualMachineEvents.**



| Metodo                                                                                   | Descrizione                                                                                                                                     |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdditionsAvailable**](ivmvirtualmachineevents-onadditionsavailable.md)             | Riceve la notifica che i componenti di integrazione sono disponibili in una macchina virtuale.<br/>                                                |
| [**OnAdditionsUninstalled**](ivmvirtualmachineevents-onadditionsuninstalled.md)         | Riceve la notifica che i componenti di integrazione vengono disinstallati in una macchina virtuale.<br/>                                              |
| [**OnConfigurationChanged**](ivmvirtualmachineevents-onconfigurationchanged.md)         | Riceve la notifica che un valore nella configurazione per questa macchina virtuale è stato modificato.<br/>                                        |
| [**OnDiskOutOfSpace**](ivmvirtualmachineevents-ondiskoutofspace.md)                     | Riceve una notifica che un disco necessario per una macchina virtuale non è disponibile e che la macchina virtuale non è in grado di eseguire.<br/>           |
| [**OnEnhancedVideoModeChanged**](ivmvirtualmachineevents-onenhancedvideomodechanged.md) | Riceve una notifica che indica che il supporto di una macchina virtuale per la modalità video avanzata è stato modificato.<br/>                                          |
| [**OnGuestLogoff**](ivmvirtualmachineevents-onguestlogoff.md)                           | Riceve la notifica che un utente si è disconnesso dal sistema operativo guest.<br/>                                                    |
| [**OnGuestShutdown**](ivmvirtualmachineevents-onguestshutdown.md)                       | Riceve la notifica che il sistema operativo guest è stato arrestato.<br/>                                                                     |
| [**OnHeartbeatStopped**](ivmvirtualmachineevents-onheartbeatstopped.md)                 | Riceve una notifica che indica che l'heartbeat di una macchina virtuale è stato arrestato. Ciò indica in genere che il sistema operativo guest si è arrestato in modo anomalo.<br/> |
| [**OnRequestShutdown**](ivmvirtualmachineevents-onrequestshutdown.md)                   | Riceve la notifica che è stata effettuata una richiesta di arresto.<br/>                                                                         |
| [**OnReset**](ivmvirtualmachineevents-onreset.md)                                       | Riceve la notifica che una macchina virtuale è stata reimpostata.<br/>                                                                         |
| [**OnStateChange**](ivmvirtualmachineevents-onstatechange.md)                           | Riceve una notifica che indica che lo stato di una macchina virtuale è stato modificato.<br/>                                                                    |
| [**OnTripleFault**](ivmvirtualmachineevents-ontriplefault.md)                           | Riceve una notifica che indica che si è triplicato l'errore di una macchina virtuale.<br/>                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-bb67-4961-bd12-a4da780c67e4<br/>   |



 

