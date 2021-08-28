---
title: Proprietà IVMGuestOS ProductType (VPCCOMInterfaces.h)
description: Recupera il tipo di prodotto del sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- Proprietà ProductType Virtual PC
- Proprietà ProductType Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà ProductType
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c31b3b91cf75687d82e02e3b97c78dd0e40f724756b609a3e2b60c73812ee5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512311"
---
# <a name="ivmguestosproducttype-property"></a>Proprietà IVMGuestOS::P roductType

\[Windows Virtual PC non è più disponibile per l'uso a Windows 8. Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera il tipo di prodotto del sistema operativo guest in esecuzione nella macchina virtuale.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a>Valore proprietà

Tipo di prodotto. Sono supportati i valori stringa seguenti.



| Valore                                                                                  | Significato                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"0x0000002"</dt> </dl> | Il sistema è un controller di dominio e il sistema operativo è Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.<br/>                                                                                                   |
| <dl> <dt>"0x0000003"</dt> </dl> | Il sistema operativo è Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.<br/> Si noti che un server che è anche un controller di dominio viene segnalato come **\_ VER NT DOMAIN \_ \_ CONTROLLER**, non **VER NT \_ \_ SERVER**.<br/> |
| <dl> <dt>"0x0000001"</dt> </dl> | Il sistema operativo è Windows 7, Windows Vista, Windows XP o Windows 2000 Professional.<br/>                                                                                                                                                                                       |



 

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

 

