---
title: Proprietà IVMKeyboard HasExclusiveAccess (VPCCOMInterfaces. h)
description: Indica se questo oggetto ha un controllo esclusivo sul dispositivo della tastiera della macchina virtuale.
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
ms.openlocfilehash: f62c235f3b4325a70a939239ac1e44360b3b5d9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121103"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a>Proprietà IVMKeyboard:: HasExclusiveAccess

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Indica se questo oggetto dispone del controllo esclusivo sul dispositivo della tastiera della macchina virtuale (VM).

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

**True** se l'accesso esclusivo al dispositivo della tastiera della macchina virtuale è stato acquisito; in caso contrario, **false** .

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                   | Significato                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                      | L'operazione è stata completata.<br/>                                                                                                                                                                                                        |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                        | Il parametro *Noexclusive* è **null**.<br/>                                                                                                                                                                                             |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                   | La modalità esclusiva richiesta è già impostata per questo dispositivo. Questo problema può verificarsi quando si tenta di impostare la modalità esclusiva quando è già stata acquisita o quando si tenta di rilasciare la modalità esclusiva quando non è stata acquisita in precedenza.<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ imposta \_ \_ modalità esclusiva \_ non riuscita</dt> <dt>0xA0040825</dt> </dl> | Non è stato possibile impostare o rilasciare la modalità esclusiva come richiesto. Questo potrebbe essere dovuto al fatto che la macchina virtuale non è più in esecuzione o perché un altro processo ha già acquisito la modalità esclusiva sul dispositivo della tastiera della macchina virtuale.<br/>                                 |
| <dl> <dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG </dl>                     | La stringa specificata è vuota o contiene un codice chiave non valido.<br/>                                                                                                                                                                      |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                | Si è verificato un errore imprevisto.<br/>                                                                                                                                                                                                    |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

