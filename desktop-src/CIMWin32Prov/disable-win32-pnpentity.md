---
description: Disabilita questo Plug and Play dispositivo.
ms.assetid: 88d60218-7282-4d0e-9a2c-0ad1a8c96650
ms.tgt_platform: multiple
title: Metodo Disable della classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 499e189d7262454e61df9c93a583bc2ed2b62da6bc8a9fa9f12a018c25813de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118419431"
---
# <a name="disable-method-of-the-win32_pnpentity-class"></a>Metodo Disable della classe \_ Win32 PnPEntity

Disabilita questo Plug and Play dispositivo.

## <a name="syntax"></a>Sintassi


```mof
Uint32 Disable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*rebootNeeded* \[ Cambio\]
</dt> <dd>

Indica se è necessario un riavvio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ PnPEntity**](win32-pnpentity.md)
</dt> </dl>

 

 




