---
title: IMsRdpDeviceCollection DeviceByIndex - proprietà
description: Recupera il dispositivo in corrispondenza dell'indice specificato.
ms.assetid: fcfc459b-46e1-4f26-a331-745fcf06638b
ms.tgt_platform: multiple
keywords:
- Proprietà DeviceByIndex Servizi Desktop remoto
- Proprietà DeviceByIndex Servizi Desktop remoto, interfaccia IMsRdpDeviceCollection
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto , proprietà DeviceByIndex
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceByIndex
- IMsRdpDeviceCollection.get_DeviceByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f13279cdf5bed0cd56921dde2344918262abed7e5473290560757e76f4c595c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606440"
---
# <a name="imsrdpdevicecollectiondevicebyindex-property"></a>Proprietà IMsRdpDeviceCollection::D eviceByIndex

Recupera il dispositivo in corrispondenza dell'indice specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_DeviceByIndex(
  [in]          ULONG index,
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
| IID<br/>                      | IMSRdpDeviceCollection IID è definito come \_ 56540617-d281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





