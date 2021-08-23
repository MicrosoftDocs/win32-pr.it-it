---
title: Enumerazione VMShutdownAction (VPCCOMInterfaces.h)
description: Specifica come arrestare una macchina virtuale quando l'host si arresta o il vpc.exe chiusura del processo.
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- Enumerazione VMShutdownAction Virtual PC
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
ms.openlocfilehash: df1f8b5bc21021e7771c14c0c3c6399e1d6342d7ebe3803759c8adb5c45024cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119248411"
---
# <a name="vmshutdownaction-enumeration"></a>Enumerazione VMShutdownAction

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Specifica come arrestare una macchina virtuale (VM) quando l'host si arresta o il vpc.exe termina.

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

<span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction \_ Save**
</dt> <dd>

Salvare lo stato della macchina virtuale.

</dd> <dt>

<span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**VmShutdownAction \_ TurnOff**
</dt> <dd>

Spegnere la macchina virtuale senza annullare le unità.

</dd> <dt>

<span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**Arresto di vmShutdownAction \_**
</dt> <dd>

Arrestare il sistema operativo guest nella macchina virtuale senza annullare le unità se i componenti di integrazione sono disponibili e in caso contrario la macchina virtuale verrà salvata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Product<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Enumerazioni di PC virtuali](virtual-pc-enumerations.md)
</dt> <dt>

[**IVMVirtualMachine::ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

