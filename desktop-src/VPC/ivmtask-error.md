---
title: Proprietà Error IVMTask (VPCCOMInterfaces. h)
description: Recupera l'errore registrato per questa attività.
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Proprietà errore Virtual PC
- Proprietà Error Virtual PC, interfaccia IVMTask
- Interfaccia IVMTask Virtual PC, proprietà Error
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301844"
---
# <a name="ivmtaskerror-property"></a>Proprietà IVMTask:: Error

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera l'errore registrato per questa attività.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a>Valore proprietà

Errore registrato.

## <a name="error-codes"></a>Codici di errore

Le istanze di [**IVMTask**](ivmtask.md) restituite da altre interfacce possono restituire valori aggiuntivi. Per informazioni dettagliate, vedere la documentazione relativa ai metodi che restituiscono un'istanza di **IVMTask** .



| Nome/valore                                                                                                                                                                        | Significato                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                           | L'operazione è stata completata.<br/>                              |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                             | Il valore del parametro è **null**.<br/>                           |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                     | Si è verificato un errore imprevisto.<br/>                          |
| <dl> <dt>Macchina virtuale \_ E \_ VMVIRTUALPC \_ \_ versione precedente</dt> <dt>0xA0040952</dt> </dl>     | Sono installati sia Virtual PC 2007 che Windows Virtual PC.<br/> |
| <dl> <dt>Macchina virtuale \_ E \_ altri \_ \_ software di virtualizzazione</dt> <dt>0xA0040953</dt> </dl> | È installato altro software di virtualizzazione.<br/>                |



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

 

