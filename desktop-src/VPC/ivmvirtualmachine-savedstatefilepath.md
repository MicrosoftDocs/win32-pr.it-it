---
title: Proprietà IVMVirtualMachine SavedStateFilePath (VPCCOMInterfaces.h)
description: Recupera il percorso completo del file di stato salvato.
ms.assetid: 01bd5491-4d08-4558-ac33-01b096f057a2
keywords:
- Proprietà SavedStateFilePath Virtual PC
- Proprietà SavedStateFilePath Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà SavedStateFilePath
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SavedStateFilePath
- IVMVirtualMachine.get_SavedStateFilePath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc97bbb55ed4a784dad897fad480a2d9175db2759bba754308dc9b845f7190c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117752233"
---
# <a name="ivmvirtualmachinesavedstatefilepath-property"></a>Proprietà IVMVirtualMachine::SavedStateFilePath

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il percorso completo del file di stato salvato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SavedStateFilePath(
  [out, retval] BSTR *savedStateFilePath
);
```



## <a name="property-value"></a>Valore proprietà

Percorso completo del file di stato salvato della macchina virtuale.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                              | Significato                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | L'operazione è stata completata.<br/>                           |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                   | Il parametro è **NULL.**<br/>                              |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>           | La configurazione è sconosciuta.<br/>                           |
| <dl> <dt>Macchina virtuale \_ E \_ VM NO SAVED \_ \_ \_ STATE</dt> <dt>0xA00400501</dt> </dl> | Alla macchina virtuale non è associato alcun file di stato salvato.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>           | Si è verificato un errore imprevisto.<br/>                       |



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

 

