---
title: IMsRdpDeviceCollection - proprietà DeviceById
description: Recupera il dispositivo con l'identificatore specificato.
ms.assetid: b64e83fa-5a94-4080-8efa-45cbfe5ceb88
ms.tgt_platform: multiple
keywords:
- Proprietà DeviceById Servizi Desktop remoto
- Proprietà DeviceById Servizi Desktop remoto, interfaccia IMsRdpDeviceCollection
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto , proprietà DeviceById
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceById
- IMsRdpDeviceCollection.get_DeviceById
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fd3fd67afebb4c853d5db71a429dc99f61d3bbc178e9ddd73b91284893108b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117940983"
---
# <a name="imsrdpdevicecollectiondevicebyid-property"></a>Proprietà IMsRdpDeviceCollection::D eviceById

Recupera il dispositivo con l'identificatore specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DeviceById(
  [in]          BSTR devInstanceId,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore [**a interfaccia IMsRdpDevice.**](imsrdpdevice.md)

## <a name="error-codes"></a>Codici di errore

Se il metodo ha esito positivo, **viene restituito S \_ OK.** Qualsiasi altro **valore HRESULT** indica che la chiamata non è riuscita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection è definito come 56540617-d281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





