---
title: Metodo IMsRdpDeviceCollection RescanDevices
description: Aggiorna l'elenco di oggetti nella raccolta. | Metodo IMsRdpDeviceCollection RescanDevices
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- Metodo RescanDevices Servizi Desktop remoto
- Metodo RescanDevices Servizi Desktop remoto, interfaccia IMsRdpDeviceCollection
- Interfaccia IMsRdpDeviceCollection Servizi Desktop remoto metodo , RescanDevices
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62011697b21171f8de326689ca35195ad4057e2e6edd01a5159fcf89c32d0f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959241"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a>Metodo IMsRdpDeviceCollection::RescanDevices

Aggiorna l'elenco di oggetti nella raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vboolDynRedir* \[ Pollici\]
</dt> <dd>

Stato di reindirizzamento predefinito che verrà applicato a tutti i dispositivi o le unità appena individuati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

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

 

 





