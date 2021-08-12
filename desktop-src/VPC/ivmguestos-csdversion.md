---
title: Proprietà IVMGuestOS CSDVersion (VPCCOMInterfaces.h)
description: CSDVersion del sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: 6f1d8dd6-6feb-4bdf-a553-631d55c18076
keywords:
- Proprietà CSDVersion Virtual PC
- Proprietà CSDVersion Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà CSDVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.CSDVersion
- IVMGuestOS.get_CSDVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4d4d1594311aff0a95795dc2501a7eff9767a233033f76bc1d5c0c9e6c7933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594340"
---
# <a name="ivmguestoscsdversion-property"></a>Proprietà IVMGuestOS::CSDVersion

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera csDVersion del sistema operativo guest in esecuzione nella macchina virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CSDVersion(
  [out, retval] BSTR *csdVersion
);
```



## <a name="property-value"></a>Valore proprietà

Stringa con terminazione Null, ad esempio "Service Pack 3", che indica il Service Pack più recente installato nel sistema. Se non è stato installato alcun Service Pack, la stringa è vuota.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                        |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                            | Il parametro è **NULL.**<br/>                           |
| <dl> <dt>Macchina virtuale \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale non è in esecuzione.<br/>                               |
| <dl> <dt>Macchina virtuale \_ E \_ ADDITIONS \_ FEATURE NOT \_ \_ AVAIL</dt> <dt>0xA0040505</dt> </dl> | I componenti di integrazione non vengono installati in questa macchina virtuale.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                    |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS è definito come \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

