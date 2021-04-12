---
title: Proprietà IVMGuestOS ServicePackMajor (VPCCOMInterfaces. h)
description: La versione principale del Service Pack del sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: 87dbc4cc-8a8d-468f-9a29-e5047029b032
keywords:
- Proprietà ServicePackMajor Virtual PC
- Proprietà ServicePackMajor Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, Proprietà ServicePackMajor
topic_type:
- apiref
api_name:
- IVMGuestOS.ServicePackMajor
- IVMGuestOS.get_ServicePackMajor
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1fa89b51e26354ce2983ad42025b1b9a3922d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120058"
---
# <a name="ivmguestosservicepackmajor-property"></a>Proprietà IVMGuestOS:: ServicePackMajor

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

La versione principale del Service Pack del sistema operativo guest in esecuzione nella macchina virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ServicePackMajor(
  [out, retval] BSTR *servicePackMajor
);
```



## <a name="property-value"></a>Valore proprietà

Il numero di versione principale del Service Pack più recente installato.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                        |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                            | Il parametro è **null**.<br/>                           |
| <dl> <dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale non è in esecuzione.<br/>                               |
| <dl> <dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt> </dl> | I componenti di integrazione non sono installati in questa macchina virtuale.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                    |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

