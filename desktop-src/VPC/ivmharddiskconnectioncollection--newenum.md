---
title: Proprietà _NewEnum IVMHardDiskConnectionCollection (VPCCOMInterfaces.h)
description: Recupera un enumeratore per l'insieme. | Proprietà _NewEnum IVMHardDiskConnectionCollection (VPCCOMInterfaces.h)
ms.assetid: 9302f536-de25-4aac-88cf-9f4af6efcda7
keywords:
- _NewEnum proprietà Virtual PC
- _NewEnum proprietà Virtual PC , interfaccia IVMHardDiskConnectionCollection
- Interfaccia IVMHardDiskConnectionCollection Virtual PC, _NewEnum proprietà
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection._NewEnum
- IVMHardDiskConnectionCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02c4bbd5d0d54d5116adc09c3a0a23c4594834b48b1b28d1700d41e5525b5d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510801"
---
# <a name="ivmharddiskconnectioncollection_newenum-property"></a>Proprietà IVMHardDiskConnectionCollection:: \_ NewEnum

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera un enumeratore per l'insieme.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a>Valore proprietà

[Enumeratore IEnumVARIANT.](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/> |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>    |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                          |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                               |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                      |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection è definito come b9f2caf4-0aeb-4085-b105-ceddb90dbf62<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

