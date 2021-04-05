---
title: Proprietà ID IVMTask (VPCCOMInterfaces. h)
description: Recupera un identificatore univoco per questa attività.
ms.assetid: 56a63b94-139b-4445-aef6-1b988e548b4b
keywords:
- ID proprietà PC virtuale
- ID proprietà Virtual PC, interfaccia IVMTask
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
ms.openlocfilehash: 821650fcec725a43d86e539bd7f6cc9e7a6e2677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874373"
---
# <a name="ivmtaskid-property"></a>Proprietà IVMTask:: ID

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>         | Il valore del parametro è **null**.<br/>  |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMTask è definito come ab72b222-6e9c-48ae-aa54-85e3e635767c<br/>                    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMTask**](ivmtask.md)
</dt> </dl>

 

