---
title: Proprietà IMsRdpDeviceV2 CmClassGuid
description: Contiene il GUID della classe di installazione di Configuration Manager per il dispositivo.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- Proprietà CmClassGuid Servizi Desktop remoto
- Proprietà CmClassGuid Servizi Desktop remoto, interfaccia IMsRdpDeviceV2
- Interfaccia IMsRdpDeviceV2 Servizi Desktop remoto , proprietà CmClassGuid
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 372d30ad6dc906b421a6f4a125d3f6fddb88addead17ea27f43369ceee758465
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099391"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a>Proprietà IMsRdpDeviceV2::CmClassGuid

Contiene il GUID della classe di installazione di Configuration Manager per il dispositivo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a>Valore proprietà

GUID della classe di installazione di Configuration Manager per il dispositivo.

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

 

 





