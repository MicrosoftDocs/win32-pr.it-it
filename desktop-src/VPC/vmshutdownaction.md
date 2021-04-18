---
title: Enumerazione VMShutdownAction (VPCCOMInterfaces. h)
description: Specifica come arrestare una macchina virtuale all'arresto dell'host o alla chiusura del vpc.exe processo.
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- VMShutdownAction enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMShutdownAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b939954042a446f7ad9f128580e804d73e9d29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301558"
---
# <a name="vmshutdownaction-enumeration"></a>Enumerazione VMShutdownAction

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Specifica come arrestare una macchina virtuale (VM) quando l'host viene arrestato o il processo vpc.exe viene chiuso.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  vmShutdownAction_Save      = 0,
  vmShutdownAction_TurnOff   = 1,
  vmShutdownAction_Shutdown  = 2
} VMShutdownAction;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**\_Salva vmShutdownAction**
</dt> <dd>

Salvare lo stato della macchina virtuale.

</dd> <dt>

<span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction \_ deviazione**
</dt> <dd>

Spegnere la macchina virtuale senza eseguire la disattivazione delle unità.

</dd> <dt>

<span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**\_arresto vmShutdownAction**
</dt> <dd>

Arrestare il sistema operativo guest nella macchina virtuale senza annotare le unità se i componenti di integrazione sono disponibili e la VM verrà salvata in altro modo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Virtual PC Windows](virtual-pc-enumerations.md)
</dt> <dt>

[**IVMVirtualMachine::ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

