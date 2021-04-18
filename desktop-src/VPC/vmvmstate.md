---
title: Enumerazione VMVMState (VPCCOMInterfaces. h)
description: Specifica lo stato di una macchina virtuale.
ms.assetid: 952dab9d-3d38-4cc5-ab75-4ee5096f7923
keywords:
- VMVMState enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMVMState
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45505e4fb4b444b15697afca4576e889f2da9a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302409"
---
# <a name="vmvmstate-enumeration"></a>Enumerazione VMVMState

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Specifica lo stato di una macchina virtuale.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  vmVMState_Invalid        = 0,
  vmVMState_TurnedOff      = 1,
  vmVMState_Saved          = 2,
  vmVMState_TurningOn      = 3,
  vmVMState_Restoring      = 4,
  vmVMState_Running        = 5,
  vmVMState_Paused         = 6,
  vmVMState_Saving         = 7,
  vmVMState_TurningOff     = 8,
  vmVMState_MergingDrives  = 9,
  vmVMState_DeleteMachine  = 10
} VMVMState;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="vmVMState_Invalid"></span><span id="vmvmstate_invalid"></span><span id="VMVMSTATE_INVALID"></span>**vmVMState \_ non valido**
</dt> <dd>

Uno stato non valido (non deve verificarsi se la macchina virtuale esiste).

</dd> <dt>

<span id="vmVMState_TurnedOff"></span><span id="vmvmstate_turnedoff"></span><span id="VMVMSTATE_TURNEDOFF"></span>**\_turnedOff vmVMState**
</dt> <dd>

Disattivato e non salvato.

</dd> <dt>

<span id="vmVMState_Saved"></span><span id="vmvmstate_saved"></span><span id="VMVMSTATE_SAVED"></span>**vmVMState \_ salvato**
</dt> <dd>

Ma il Guest viene salvato.

</dd> <dt>

<span id="vmVMState_TurningOn"></span><span id="vmvmstate_turningon"></span><span id="VMVMSTATE_TURNINGON"></span>**\_TurningOn vmVMState**
</dt> <dd>

In fase di attivazione.

</dd> <dt>

<span id="vmVMState_Restoring"></span><span id="vmvmstate_restoring"></span><span id="VMVMSTATE_RESTORING"></span>**\_ripristino vmVMState**
</dt> <dd>

Ripristino dello stato.

</dd> <dt>

<span id="vmVMState_Running"></span><span id="vmvmstate_running"></span><span id="VMVMSTATE_RUNNING"></span>**vmVMState \_ in esecuzione**
</dt> <dd>

In esecuzione e non in pausa.

</dd> <dt>

<span id="vmVMState_Paused"></span><span id="vmvmstate_paused"></span><span id="VMVMSTATE_PAUSED"></span>**vmVMState \_ sospeso**
</dt> <dd>

In esecuzione e sospesa.

</dd> <dt>

<span id="vmVMState_Saving"></span><span id="vmvmstate_saving"></span><span id="VMVMSTATE_SAVING"></span>**\_salvataggio vmVMState**
</dt> <dd>

Salvataggio dello stato.

</dd> <dt>

<span id="vmVMState_TurningOff"></span><span id="vmvmstate_turningoff"></span><span id="VMVMSTATE_TURNINGOFF"></span>**\_TurningOff vmVMState**
</dt> <dd>

In fase di disattivazione.

</dd> <dt>

<span id="vmVMState_MergingDrives"></span><span id="vmvmstate_mergingdrives"></span><span id="VMVMSTATE_MERGINGDRIVES"></span>**\_MergingDrives vmVMState**
</dt> <dd>

Durante il processo di Unione delle unità di annullamento.

</dd> <dt>

<span id="vmVMState_DeleteMachine"></span><span id="vmvmstate_deletemachine"></span><span id="VMVMSTATE_DELETEMACHINE"></span>**\_DeleteMachine vmVMState**
</dt> <dd>

Eliminazione della macchina virtuale.

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

[**IVMVirtualMachine:: state**](ivmvirtualmachine-state.md)
</dt> <dt>

[**IVMVirtualMachineEvents:: OnStateChange**](ivmvirtualmachineevents-onstatechange.md)
</dt> <dt>

[**IVMVirtualPCEvents::OnVMStateChange**](ivmvirtualpcevents-onvmstatechange.md)
</dt> </dl>

 

