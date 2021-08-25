---
title: Proprietà _NewEnum IVMParallelPortCollection (VPCCOMInterfaces.h)
description: Recupera un enumeratore per l'insieme. | Proprietà _NewEnum IVMParallelPortCollection (VPCCOMInterfaces.h)
ms.assetid: 2e26fba7-bcc0-4bb3-bf89-3c62cbd2b37e
keywords:
- _NewEnum proprietà Virtual PC
- _NewEnum proprietà Virtual PC , interfaccia IVMParallelPortCollection
- Interfaccia IVMParallelPortCollection Virtual PC, _NewEnum proprietà
topic_type:
- apiref
api_name:
- IVMParallelPortCollection._NewEnum
- IVMParallelPortCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa415000e828ff4d484f66ce7765328638e5980ec202c328dffac3b2d844827
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973861"
---
# <a name="ivmparallelportcollection_newenum-property"></a>Proprietà IVMParallelPortCollection:: \_ NewEnum

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
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPortCollection è definito come 27c3e036-198f-430c-8735-6e652f7203fd<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMParallelPortCollection**](ivmparallelportcollection.md)
</dt> </dl>

 

