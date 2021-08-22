---
title: Proprietà OSName IVMGuestOS (VPCCOMInterfaces.h)
description: Nome del sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: 6381fc15-a6ab-429b-809d-7f89e7ec666d
keywords:
- Proprietà OSName Virtual PC
- Proprietà OSName Virtual PC , interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà OSName
topic_type:
- apiref
api_name:
- IVMGuestOS.OSName
- IVMGuestOS.get_OSName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5df969058facebd99e7438b10ed3021d9033df7f30874d4b1c23a8339cc9994
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512421"
---
# <a name="ivmguestososname-property"></a>Proprietà IVMGuestOS::OSName

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il nome del sistema operativo guest in esecuzione nella macchina virtuale .

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_OSName(
  [out, retval] BSTR *guestOSName
);
```



## <a name="property-value"></a>Valore proprietà

Nome completo (incluso il nome della suite) del sistema operativo guest.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                                       | Significato                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | L'operazione è stata completata.<br/>                        |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                            | Il parametro è **NULL.**<br/>                           |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE</dt> <dt>0xA0040206</dt> </dl>               | La macchina virtuale non è in esecuzione.<br/>                               |
| <dl> <dt>Macchina virtuale \_ FUNZIONALITÀ \_ DELLE AGGIUNTE E NON \_ \_ \_ 0XA0040505</dt> <dt></dt> </dl> | I componenti di integrazione non sono installati in questa macchina virtuale.<br/> |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>                    | Si è verificato un errore imprevisto.<br/>                    |



## <a name="remarks"></a>Commenti

Quando viene richiamato questo metodo, è necessario che la macchina virtuale sia in esecuzione, ovvero sia completamente avviato e non in fase di arresto, e che i componenti di integrazione siano installati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

