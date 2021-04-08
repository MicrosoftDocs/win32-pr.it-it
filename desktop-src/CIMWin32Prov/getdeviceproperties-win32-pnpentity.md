---
description: Ottiene le proprietà specificate del dispositivo Plug and Play.
ms.assetid: 63327a4f-7d4a-4041-b58d-7a852ba08d5b
ms.tgt_platform: multiple
title: Metodo GetDeviceProperties della classe Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.GetDeviceProperties
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6aa9f6cad17fe48617b5bf7d28ba19d6f5370834
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049153"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a>Metodo GetDeviceProperties della \_ classe PnPEntity Win32

Ottiene le proprietà specificate del dispositivo Plug and Play.

## <a name="syntax"></a>Sintassi


```mof
Uint32 GetDeviceProperties(
  [in, optional] string                  devicePropertyKeys[],
  [out]          Win32_PnPDeviceProperty deviceProperties[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*devicePropertyKeys* \[ in, facoltativo\]
</dt> <dd>

Proprietà da restituire.

</dd> <dt>

*deviceProperties* \[ out\]
</dt> <dd>

Proprietà richieste nei sottotipi appropriati della classe astratta [**Win32 \_ PnPDeviceProperty**](win32-pnpdeviceproperty.md) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_PnPEntity Win32**](win32-pnpentity.md)
</dt> </dl>

 

 




