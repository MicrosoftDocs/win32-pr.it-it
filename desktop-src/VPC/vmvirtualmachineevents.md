---
title: Enumerazione VMVirtualMachineEvents (VPCCOMInterfaces.h)
description: Specifica gli eventi della macchina virtuale.
ms.assetid: 158bdada-6fd3-488c-9ff1-e04df9a79127
keywords:
- VMVirtualMachineEvents enumeration Virtual PC
topic_type:
- apiref
api_name:
- VMVirtualMachineEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5079aee6752c260cd6bab9ee9022d22fd891eb6adf36ad0ec4d1c9987b6ff508
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998341"
---
# <a name="vmvirtualmachineevents-enumeration"></a>Enumerazione VMVirtualMachineEvents

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Specifica gli eventi della macchina virtuale( VM).

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  vmVirtualMachineEvent_StateChanged              = 1,
  vmVirtualMachineEvent_RequestShutdown           = 2,
  vmVirtualMachineEvent_Reset                     = 3,
  vmVirtualMachineEvent_TripleFault               = 4,
  vmVirtualMachineEvent_HeartbeatStopped          = 5,
  vmVirtualMachineEvent_ConfigurationChanged      = 6,
  vmVirtualMachineEvent_EnhancedVideoModeChanged  = 7,
  vmVirtualMachineEvent_AdditionsUninstalled      = 8,
  vmVirtualMachineEvent_AdditionsAvailable        = 9,
  vmVirtualMachineEvent_GuestShutdown             = 10,
  vmVirtualMachineEvent_GuestLogoff               = 11,
  vmVirtualMachineEvent_DiskOutOfSpace            = 12
} VMVirtualMachineEvents;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="vmVirtualMachineEvent_StateChanged"></span><span id="vmvirtualmachineevent_statechanged"></span><span id="VMVIRTUALMACHINEEVENT_STATECHANGED"></span>**vmVirtualMachineEvent \_ StateChanged**
</dt> <dd>

Lo stato di una macchina virtuale è stato modificato.

</dd> <dt>

<span id="vmVirtualMachineEvent_RequestShutdown"></span><span id="vmvirtualmachineevent_requestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_REQUESTSHUTDOWN"></span>**Richiesta vmVirtualMachineEventShutdown \_**
</dt> <dd>

È stato richiesto un arresto.

</dd> <dt>

<span id="vmVirtualMachineEvent_Reset"></span><span id="vmvirtualmachineevent_reset"></span><span id="VMVIRTUALMACHINEEVENT_RESET"></span>**VmVirtualMachineEvent \_ Reset**
</dt> <dd>

Una macchina virtuale è stata reimpostata.

</dd> <dt>

<span id="vmVirtualMachineEvent_TripleFault"></span><span id="vmvirtualmachineevent_triplefault"></span><span id="VMVIRTUALMACHINEEVENT_TRIPLEFAULT"></span>**TripleFault vmVirtualMachineEvent \_**
</dt> <dd>

Si è triplicato l'errore di una macchina virtuale.

</dd> <dt>

<span id="vmVirtualMachineEvent_HeartbeatStopped"></span><span id="vmvirtualmachineevent_heartbeatstopped"></span><span id="VMVIRTUALMACHINEEVENT_HEARTBEATSTOPPED"></span>**Heartbeat vmVirtualMachineEventStopped \_**
</dt> <dd>

L'heartbeat di una macchina virtuale è stato arrestato. Ciò indica in genere che il sistema operativo guest si è arrestato in modo anomalo.

</dd> <dt>

<span id="vmVirtualMachineEvent_ConfigurationChanged"></span><span id="vmvirtualmachineevent_configurationchanged"></span><span id="VMVIRTUALMACHINEEVENT_CONFIGURATIONCHANGED"></span>**VmVirtualMachineEvent \_ ConfigurationChanged**
</dt> <dd>

Un valore nella configurazione per questa macchina virtuale è stato modificato

</dd> <dt>

<span id="vmVirtualMachineEvent_EnhancedVideoModeChanged"></span><span id="vmvirtualmachineevent_enhancedvideomodechanged"></span><span id="VMVIRTUALMACHINEEVENT_ENHANCEDVIDEOMODECHANGED"></span>**vmVirtualMachineEvent \_ EnhancedVideoModeChanged**
</dt> <dd>

La modalità video di una macchina virtuale è stata modificata.

</dd> <dt>

<span id="vmVirtualMachineEvent_AdditionsUninstalled"></span><span id="vmvirtualmachineevent_additionsuninstalled"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSUNINSTALLED"></span>**vmVirtualMachineEvent \_ AdditionsUninstalled**
</dt> <dd>

I componenti di integrazione sono stati disinstallati dalla macchina virtuale.

</dd> <dt>

<span id="vmVirtualMachineEvent_AdditionsAvailable"></span><span id="vmvirtualmachineevent_additionsavailable"></span><span id="VMVIRTUALMACHINEEVENT_ADDITIONSAVAILABLE"></span>**Aggiunte vmVirtualMachineEventAvailable \_**
</dt> <dd>

L'integrazione è disponibile nel sistema operativo guest.

</dd> <dt>

<span id="vmVirtualMachineEvent_GuestShutdown"></span><span id="vmvirtualmachineevent_guestshutdown"></span><span id="VMVIRTUALMACHINEEVENT_GUESTSHUTDOWN"></span>**VmVirtualMachineEvent \_ GuestShutdown**
</dt> <dd>

Un sistema operativo guest è in fase di arresto.

</dd> <dt>

<span id="vmVirtualMachineEvent_GuestLogoff"></span><span id="vmvirtualmachineevent_guestlogoff"></span><span id="VMVIRTUALMACHINEEVENT_GUESTLOGOFF"></span>**VmVirtualMachineEvent \_ GuestLogoff**
</dt> <dd>

Utente disconnesso dal sistema operativo guest.

</dd> <dt>

<span id="vmVirtualMachineEvent_DiskOutOfSpace"></span><span id="vmvirtualmachineevent_diskoutofspace"></span><span id="VMVIRTUALMACHINEEVENT_DISKOUTOFSPACE"></span>**vmVirtualMachineEvent \_ DiskOutOfSpace**
</dt> <dd>

Lo spazio su disco richiesto dalla macchina virtuale è insufficiente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)
</dt> </dl>

 

