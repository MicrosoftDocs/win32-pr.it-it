---
title: Proprietà CmDeviceInstance di IMsRdpDeviceV2
description: Contiene l'istanza del dispositivo di Configuration Manager del dispositivo.
ms.assetid: 2a3e7001-7889-417f-8f9d-cc7a1776249f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà CmDeviceInstance
- Servizi Desktop remoto proprietà CmDeviceInstance, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto, proprietà CmDeviceInstance
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmDeviceInstance
- IMsRdpDeviceV2.get_CmDeviceInstance
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec036d5e2497f45fff389ec8af457a05fcc9fef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300990"
---
# <a name="imsrdpdevicev2cmdeviceinstance-property"></a>Proprietà IMsRdpDeviceV2:: CmDeviceInstance

Contiene l'istanza del dispositivo di Configuration Manager del dispositivo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CmDeviceInstance(
  [out, retval] DWORD *pCmDeviceInstance
);
```



## <a name="property-value"></a>Valore proprietà

Istanza del dispositivo di Configuration Manager del dispositivo.

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

 

 





