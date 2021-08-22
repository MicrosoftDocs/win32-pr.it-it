---
title: Proprietà IVMAccountant UpTime (VPCCOMInterfaces.h)
description: Recupera il numero di secondi di esecuzione della macchina virtuale.
ms.assetid: 0c62d51b-fdf1-43f6-81d8-a5f0538c510f
keywords:
- Proprietà UpTime Virtual PC
- Proprietà UpTime Virtual PC, interfaccia IVMAccountant
- Interfaccia IVMAccountant Virtual PC, proprietà UpTime
topic_type:
- apiref
api_name:
- IVMAccountant.UpTime
- IVMAccountant.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df0c7731ab50d1967d59eb7178fb6bcee008b6d45fed69ab66279ae3fd8beb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654381"
---
# <a name="ivmaccountantuptime-property"></a>Proprietà IVMAccountant::UpTime

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il numero di secondi di esecuzione della macchina virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a>Valore proprietà

numero di secondi.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>       |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>          |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                    | La macchina virtuale non è in esecuzione.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/>   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMAccountant è definito come \_ 6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

