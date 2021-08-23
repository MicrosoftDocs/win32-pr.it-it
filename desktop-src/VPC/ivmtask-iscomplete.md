---
title: Proprietà IVMTask IsComplete (VPCCOMInterfaces.h)
description: Determina se l'attività è stata completata.
ms.assetid: 181fa220-4de2-4ab3-950b-fffc4fe4de64
keywords:
- Proprietà IsComplete Virtual PC
- Proprietà IsComplete Virtual PC, interfaccia IVMTask
- Interfaccia IVMTask Virtual PC, proprietà IsComplete
topic_type:
- apiref
api_name:
- IVMTask.IsComplete
- IVMTask.get_IsComplete
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60c4c347abf9f1cee52990fe779593083b5cbcaadede8c663175e677c8c1f793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998731"
---
# <a name="ivmtaskiscomplete-property"></a>Proprietà IVMTask::IsComplete

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Determina se l'attività è stata completata.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_IsComplete(
  [out, retval] VARIANT_BOOL *isComplete
);
```



## <a name="property-value"></a>Valore proprietà

**TRUE** se l'attività è stata completata e **FALSE in caso contrario.**

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il valore del parametro è **NULL.**<br/>  |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attività IVM**](ivmtask.md)
</dt> </dl>

 

