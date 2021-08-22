---
title: Proprietà IVMKeyboard HasExclusiveAccess (VPCCOMInterfaces.h)
description: Indica se questo oggetto ha il controllo esclusivo sul dispositivo tastiera della macchina virtuale.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- Proprietà HasExclusiveAccess Virtual PC
- Proprietà HasExclusiveAccess Virtual PC, interfaccia IVMKeyboard
- Interfaccia IVMKeyboard Virtual PC, proprietà HasExclusiveAccess
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c01e13e331824a0d1b6834cbb27da7eb4b5420a3cd3dbec94cdbdd494c79c95b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136724"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a>Proprietà IVMKeyboard::HasExclusiveAccess

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Indica se questo oggetto ha il controllo esclusivo sul dispositivo tastiera (VM) della macchina virtuale.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a>Valore proprietà

**TRUE** se è stato acquisito l'accesso esclusivo al dispositivo tastiera della macchina virtuale, **FALSE in caso** contrario.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                   | Significato                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                      | L'operazione è stata completata.<br/>                                                                                                                                                                                                        |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                        | Il *parametro isExclusive* è **NULL.**<br/>                                                                                                                                                                                             |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                   | La modalità esclusiva richiesta è già impostata per questo dispositivo. Ciò può verificarsi quando si tenta di impostare la modalità esclusiva quando è già stata acquisita o quando si tenta di rilasciare la modalità esclusiva quando non è stata acquisita in precedenza.<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ SET EXCLUSIVE MODE FAIL \_ \_ \_ 0xA0040825</dt> <dt></dt> </dl> | Impossibile impostare o rilasciare la modalità esclusiva come richiesto. Ciò potrebbe essere dovuto al fatto che la macchina virtuale non è più in esecuzione o perché un altro processo ha già acquisito la modalità esclusiva nel dispositivo tastiera della macchina virtuale.<br/>                                 |
| <dl> <dt>E \_ InvalidARG</dt> <dt>0x80000003</dt> </dl>                     | La stringa specificata è vuota o contiene un codice di chiave non valido.<br/>                                                                                                                                                                      |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>                | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                                                    |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

