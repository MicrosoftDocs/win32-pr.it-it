---
title: Proprietà IVMAccountant NetworkBytesReceived (VPCCOMInterfaces.h)
description: Numero totale di byte ricevuti da tutte le schede di rete virtuali per questa macchina virtuale.
ms.assetid: 6f6b32e6-d99b-405c-a788-ed646b3a7593
keywords:
- Proprietà NetworkBytesReceived Virtual PC
- Proprietà NetworkBytesReceived Virtual PC, interfaccia IVMAccountant
- Interfaccia IVMAccountant Virtual PC, proprietà NetworkBytesReceived
topic_type:
- apiref
api_name:
- IVMAccountant.NetworkBytesReceived
- IVMAccountant.get_NetworkBytesReceived
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 483bc038622278e23bd46688fa55695c6b11e91d7b602377ae8eb9ddaeab86c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473751"
---
# <a name="ivmaccountantnetworkbytesreceived-property"></a>Proprietà IVMAccountant::NetworkBytesReceived

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il numero totale di byte ricevuti da tutte le schede di rete virtuali per questa macchina virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_NetworkBytesReceived(
  [out, retval] VARIANT *bytesReceived
);
```



## <a name="property-value"></a>Valore proprietà

Numero totale di byte ricevuti. Questi dati vengono restituiti come **VARIANT di** tipo **VT \_ DECIMAL.**

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

 

