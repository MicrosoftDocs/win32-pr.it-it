---
title: Proprietà IVMGuestOS ScreenLocked (VPCCOMInterfaces. h)
description: Indica se lo schermo del sistema operativo guest è bloccato.
ms.assetid: 5ce2e0ad-b98c-4aa7-99b5-0fc85026a121
keywords:
- Proprietà ScreenLocked Virtual PC
- Proprietà ScreenLocked Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà ScreenLocked
topic_type:
- apiref
api_name:
- IVMGuestOS.ScreenLocked
- IVMGuestOS.get_ScreenLocked
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1f14bf0a61f06e9f36b44d02881cf7edc1f793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048464"
---
# <a name="ivmguestosscreenlocked-property"></a>Proprietà IVMGuestOS:: ScreenLocked

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Indica se lo schermo del sistema operativo guest è bloccato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ScreenLocked(
  [out, retval] VARIANT_BOOL *guestScreenLocked
);
```



## <a name="property-value"></a>Valore proprietà

**Variante \_ TRUE** se la schermata è bloccata nel sistema operativo guest, **Variant \_ false** in caso contrario.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                                                    |
| <dl> <dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt> </dl>                            | Il parametro è **null**.<br/>                                                       |
| <dl> <dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt> </dl>               | Per questa operazione è necessario che la macchina virtuale (VM) sia in esecuzione.<br/>                     |
| <dl> <dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt> </dl> | La funzionalità componenti di integrazione non è abilitata nel sistema operativo guest.<br/> |
| <dl> <dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                                                |



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

 

