---
title: Proprietà IVMAccountant NetworkBytesSent (VPCCOMInterfaces.h)
description: Numero totale di byte inviati da tutte le schede di rete virtuali per questa macchina virtuale.
ms.assetid: 3b5c3fa2-48c6-46c8-bbb6-5d1a9769308a
keywords:
- Proprietà NetworkBytesSent Virtual PC
- Proprietà NetworkBytesSent Virtual PC, interfaccia IVMAccountant
- Interfaccia IVMAccountant Virtual PC, proprietà NetworkBytesSent
topic_type:
- apiref
api_name:
- IVMAccountant.NetworkBytesSent
- IVMAccountant.get_NetworkBytesSent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581aa5ec031674a7784a1d1da36b439a70b5122fe630f97dfe1f09f0670c9781
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473691"
---
# <a name="ivmaccountantnetworkbytessent-property"></a>Proprietà IVMAccountant::NetworkBytesSent

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il numero totale di byte inviati da tutte le schede di rete virtuali per questa macchina virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_NetworkBytesSent(
  [out, retval] VARIANT *bytesSent
);
```



## <a name="property-value"></a>Valore proprietà

Numero totale di byte inviati da tutte le schede di interfaccia di rete virtuale per questa macchina virtuale. Viene restituito come **VARIANT di** tipo **VT \_ DECIMAL.**

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>       |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>          |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | La macchina virtuale non è in esecuzione.<br/> |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/>   |



## <a name="remarks"></a>Commenti

Si noti che le statistiche di I/O di rete vengono reimpostate su zero quando una macchina virtuale viene spenta, reimpostata o ripristinata dallo stato salvato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant è definito come 6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

