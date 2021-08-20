---
title: Enumerazione VMUndoAction (VPCCOMInterfaces.h)
description: Specifica cosa accade all'annullamento delle unità quando una macchina virtuale viene arrestata o spenta.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- VMUndoAction enumeration Virtual PC
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f62c4ab00b30300b2951a5a6b1c300bf34b1b3797f036f28a66e82dc2cad22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998331"
---
# <a name="vmundoaction-enumeration"></a>Enumerazione VMUndoAction

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Specifica cosa accade all'annullamento delle unità quando una macchina virtuale viene arrestata o spenta.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**VmUndoAction \_ Discard**
</dt> <dd>

Rimuovere le unità di annullamento. le unità padre rimangono invariate.

</dd> <dt>

<span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**VmUndoAction \_ Keep**
</dt> <dd>

Mantenere le unità di annullamento; le unità padre rimangono invariate, ma le modifiche verranno mantenute al successivo avvio della macchina virtuale.

</dd> <dt>

<span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**Commit vmUndoAction \_**
</dt> <dd>

Eseguire il commit delle modifiche alle unità padre.

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

[**IVMVirtualMachine::UndoAction**](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

