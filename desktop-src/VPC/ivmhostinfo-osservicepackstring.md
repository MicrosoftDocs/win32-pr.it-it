---
title: Proprietà IVMHostInfo OSServicePackString (VPCCOMInterfaces.h)
description: Recupera le informazioni del Service Pack del sistema operativo in esecuzione nel computer host.
ms.assetid: e5fe51f8-9bcf-49bd-bec6-2538b3e8edfa
keywords:
- Proprietà OSServicePackString Virtual PC
- Proprietà OSServicePackString Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC , proprietà OSServicePackString
topic_type:
- apiref
api_name:
- IVMHostInfo.OSServicePackString
- IVMHostInfo.get_OSServicePackString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c3b42a9c0976ca51196c091d5704bd224ea591cdc7301d7f1387209e7fff83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593503"
---
# <a name="ivmhostinfoosservicepackstring-property"></a>Proprietà IVMHostInfo::OSServicePackString

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera le informazioni del Service Pack del sistema operativo in esecuzione nel computer host.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_OSServicePackString(
  [out, retval] BSTR *OSServicePack
);
```



## <a name="property-value"></a>Valore proprietà

Versione del Service Pack.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                    | Significato                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                       | L'operazione è stata completata.<br/>     |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>         | Il parametro è **NULL.**<br/>        |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl> | Si è verificato un errore imprevisto.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHostInfo è definito come \_ 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

