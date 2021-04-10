---
title: Proprietà Count IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Numero di porte parallele in questa raccolta.
ms.assetid: f2f4cac4-bb63-4ac2-ba6e-321a8a29c6d4
keywords:
- Conteggio proprietà PC virtuale
- Proprietà Count Virtual PC, interfaccia IVMParallelPortCollection
- Interfaccia IVMParallelPortCollection Virtual PC, proprietà Count
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Count
- IVMParallelPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0bb1af40f0e4d15b7eae65e18a8d9910deb769c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964312"
---
# <a name="ivmparallelportcollectioncount-property"></a>Proprietà IVMParallelPortCollection:: count

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera il numero di porte parallele in questa raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>Valore proprietà

Numero di porte parallele.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                            | Significato                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>               | L'operazione è stata completata.<br/> |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl> | Il parametro è **null**.<br/>    |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPortCollection è definito come 27c3e036-198f-430C-8735-6e652f7203fd<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMParallelPortCollection**](ivmparallelportcollection.md)
</dt> </dl>

 

