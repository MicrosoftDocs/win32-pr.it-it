---
description: Ottiene le proprietà specificate di questo Plug and Play dispositivo.
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
ms.openlocfilehash: 855c3c0644d8c7b5c5300c8d12d5a6f98073a4511f8d0d65f4058da7fb9d0f24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077511"
---
# <a name="getdeviceproperties-method-of-the-win32_pnpentity-class"></a>Metodo GetDeviceProperties della classe \_ Win32 PnPEntity

Ottiene le proprietà specificate di questo Plug and Play dispositivo.

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

*proprietà del dispositivo* \[ Cambio\]
</dt> <dd>

Proprietà richieste nei sottotipi appropriati della [**classe astratta \_ Win32 PnPDeviceProperty.**](win32-pnpdeviceproperty.md)

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

 

 




