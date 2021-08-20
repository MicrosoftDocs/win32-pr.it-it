---
title: Proprietà IVMTask ID (VPCCOMInterfaces.h)
description: Recupera un identificatore univoco per questa attività.
ms.assetid: 56a63b94-139b-4445-aef6-1b988e548b4b
keywords:
- Proprietà ID Virtual PC
- Proprietà ID Virtual PC , interfaccia IVMTask
- Interfaccia IVMTask Virtual PC, proprietà ID
topic_type:
- apiref
api_name:
- IVMTask.ID
- IVMTask.get_ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45bb5efed1e7c0398113b20e1bf2b9de6edc81bf39958a34895219e7250facbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123241"
---
# <a name="ivmtaskid-property"></a>Proprietà IVMTask::ID

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera un identificatore univoco per questa attività.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ID(
  [out, retval] long *ID
);
```



## <a name="property-value"></a>Valore proprietà

Identificatore univoco.

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

 

