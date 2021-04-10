---
title: Proprietà Count IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Recupera il numero di macchine virtuali in questa raccolta.
ms.assetid: c1f38528-fd9b-4b86-aac6-de944379b92e
keywords:
- Conteggio proprietà PC virtuale
- Proprietà Count Virtual PC, interfaccia IVMVirtualMachineCollection
- Interfaccia IVMVirtualMachineCollection Virtual PC, proprietà Count
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Count
- IVMVirtualMachineCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f641fad504c6dd593737cf35014813f49609a4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121083"
---
# <a name="ivmvirtualmachinecollectioncount-property"></a>Proprietà IVMVirtualMachineCollection:: count

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera il numero di macchine virtuali in questa raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valore proprietà

Numero di macchine virtuali.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>        |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                     |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                           |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                  |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl>  |
| IID<br/>                      | IID \_ IVMVirtualMachineCollection è definito come 59f31786-2a3d-4FBF-9896-d85338ca0da1<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)
</dt> </dl>

 

