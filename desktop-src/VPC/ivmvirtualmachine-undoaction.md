---
title: Proprietà IVMVirtualMachine UndoAction (VPCCOMInterfaces.h)
description: Azione predefinita da eseguire su tutte le unità di annullamento quando la macchina virtuale viene arrestata.
ms.assetid: fcdd5217-4909-435a-b11d-63578ab46e37
keywords:
- Proprietà UndoAction Virtual PC
- Proprietà UndoAction Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà UndoAction
topic_type:
- apiref
api_name:
- IVMVirtualMachine.UndoAction
- IVMVirtualMachine.get_UndoAction
- IVMVirtualMachine.put_UndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed32b0864e1a22b196001c5f75ba7e58711e7a9b6d6b2781a5f75ae0c3ced5ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344546"
---
# <a name="ivmvirtualmachineundoaction-property"></a>Proprietà IVMVirtualMachine::UndoAction

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera e imposta l'azione predefinita da eseguire su tutte le unità di annullamento quando la macchina virtuale (VM) viene spenta usando il metodo [**TurnOff**](ivmvirtualmachine-turnoff.md) o arrestata con il metodo [**Shutdown**](ivmguestos-shutdown.md) o disattivata dall'interno del sistema operativo guest.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_UndoAction(
  [in]          VMUndoAction undoAction
);

HRESULT get_UndoAction(
  [out, retval] VMUndoAction *undoAction
);
```



## <a name="property-value"></a>Valore proprietà

Specifica l'azione predefinita da eseguire su tutte le unità di annullamento quando la macchina virtuale viene arrestata dall'interno del sistema operativo guest. Per un elenco di valori, vedere [**VMUndoAction**](vmundoaction.md).

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>        |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>      | Il parametro non è valido.<br/>       |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl> | La configurazione è sconosciuta.<br/>     |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/> |



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

 

