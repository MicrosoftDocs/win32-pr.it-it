---
title: Proprietà IVMVirtualMachine Undoable (VPCCOMInterfaces.h)
description: Determina se le unità di annullamento sono abilitate per i dischi rigidi connessi alla macchina virtuale.
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- Proprietà annullabile Virtual PC
- Proprietà annullabile Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà Undoable
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Undoable
- IVMVirtualMachine.get_Undoable
- IVMVirtualMachine.put_Undoable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7663cefb8f94809f0fd016e002102c9956066b64ca21fb79766598b592ec3dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752074"
---
# <a name="ivmvirtualmachineundoable-property"></a>Proprietà IVMVirtualMachine::Undoable

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Determina se le unità di annullamento sono abilitate per i dischi rigidi connessi alla macchina virtuale .

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Undoable(
  [in]          VARIANT_BOOL enableUndo
);

HRESULT get_Undoable(
  [out, retval] VARIANT_BOOL *isUndoable
);
```



## <a name="property-value"></a>Valore proprietà

Specifica **VARIANT \_ TRUE se le** unità di annullamento sono abilitate per i dischi rigidi connessi alla macchina virtuale e VARIANT **\_ FALSE** in caso contrario.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                         | Significato                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                            | L'operazione è stata completata.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>      | Si è verificato un errore imprevisto.<br/> |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>              | Il parametro è **NULL.**<br/>        |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>      | La configurazione è sconosciuta.<br/>     |
| <dl> <dt>Macchina virtuale \_ E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt> </dl> | La macchina virtuale è in esecuzione o salvata.<br/>       |



## <a name="remarks"></a>Commenti

Se le unità di annullamento sono disabilitate, tutti i file di unità di annullamento esistenti verranno eliminati.

Non è possibile impostare questa proprietà se la macchina virtuale è in esecuzione o salvata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

