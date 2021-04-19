---
title: Proprietà MMX IVMHostInfo (VPCCOMInterfaces. h)
description: Determina se il processore supporta il set di istruzioni MMX. | Proprietà MMX IVMHostInfo (VPCCOMInterfaces. h)
ms.assetid: 2f556289-c752-4af2-a6d0-abb6e717e609
keywords:
- Proprietà MMX Virtual PC
- Proprietà MMX Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà MMX
topic_type:
- apiref
api_name:
- IVMHostInfo.MMX
- IVMHostInfo.get_MMX
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e224ed6a0f15da9143a884dd1c1dfacc1634fce7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321552"
---
# <a name="ivmhostinfommx-property"></a>Proprietà IVMHostInfo:: MMX

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Determina se il processore supporta il set di istruzioni MMX.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MMX(
  [out, retval] VARIANT_BOOL *mmxEnabled
);
```



## <a name="property-value"></a>Valore proprietà

**True** se le istruzioni MMX sono supportate; in caso contrario, **false** .

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **null**.<br/>        |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

