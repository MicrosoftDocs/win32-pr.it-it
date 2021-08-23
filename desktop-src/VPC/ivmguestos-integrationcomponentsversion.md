---
title: Proprietà IntegrationComponentsVersion IVMGuestOS (VPCCOMInterfaces.h)
description: Recupera la versione dei componenti di integrazione installati nel sistema operativo guest.
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- IntegrationComponentsVersion - proprietà Virtual PC
- Proprietà IntegrationComponentsVersion Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà IntegrationComponentsVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854cb86817f461085c72a437fa962649e50ab11b65a847d0756dc8e9c7b18177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999051"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a>Proprietà IVMGuestOS::IntegrationComponentsVersion

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera la versione dei componenti di integrazione installati nel sistema operativo guest.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a>Valore proprietà

Versione.

## <a name="error-codes"></a>Codici di errore



| Nome/valore                                                                                                                                                              | Significato                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                 | L'operazione è stata completata.<br/>                                                     |
| <dl> <dt>E \_ Puntatore</dt> <dt>0x80004003</dt> </dl>                   | Il parametro è **NULL.**<br/>                                                        |
| <dl> <dt>Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SCONOSCIUTA</dt> <dt>0xA0040207</dt> </dl>           | Non è stato possibile trovare la macchina virtuale .<br/>                                      |
| <dl> <dt>Macchina virtuale \_ E \_ ADDITIONS \_ NOT \_ AVAIL</dt> <dt>0xA0040504</dt> </dl> | I componenti di integrazione non sono installati in questa macchina virtuale o la macchina virtuale non è mai stata avviata.<br/> |
| <dl> <dt>DISP \_ E \_ ECCEZIONE</dt> <dt>0x80020009</dt> </dl>           | Si è verificato un errore imprevisto.<br/>                                                 |



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

 

