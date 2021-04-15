---
title: Proprietà IsOptionalDevice di IMsRdpDeviceV2
description: Specifica se il dispositivo è facoltativo per il reindirizzamento USB.
ms.assetid: a7226c40-7e22-48af-9895-b1fb1f861b58
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà IsOptionalDevice
- Servizi Desktop remoto proprietà IsOptionalDevice, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, proprietà IsOptionalDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsOptionalDevice
- IMsRdpDeviceV2.get_IsOptionalDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad0e459a91e88573515128ca37033768f7839ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477741"
---
# <a name="imsrdpdevicev2isoptionaldevice-property"></a>Proprietà IMsRdpDeviceV2:: IsOptionalDevice

Specifica se il dispositivo è facoltativo per il reindirizzamento USB.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_IsOptionalDevice(
  [out, retval] VARIANT_BOOL *pvboolOptionalDevice
);
```



## <a name="property-value"></a>Valore proprietà

**true** se il dispositivo è facoltativo; in caso contrario, **false**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 con SP1<br/>                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2 con SP1<br/>                                             |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 è definito come 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





