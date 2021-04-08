---
title: Metodo IMsRdpDeviceCollection2 AddDeviceByInstanceId
description: Aggiunge un dispositivo non in elenco alla raccolta di dispositivi.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddDeviceByInstanceId
- Metodo AddDeviceByInstanceId Servizi Desktop remoto, interfaccia IMsRdpDeviceCollection2
- Interfaccia IMsRdpDeviceCollection2 Servizi Desktop remoto, metodo AddDeviceByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f817a5beb4d8762787c4bf2f8a3995d3918e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047880"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a>Metodo IMsRdpDeviceCollection2:: AddDeviceByInstanceId

Aggiunge un dispositivo non in elenco alla raccolta di dispositivi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tipo* \[ di in\]
</dt> <dd>

Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**

Valore dell'enumerazione [**RedirectDeviceType**](redirectdevicetype.md) che specifica il tipo di dispositivo da aggiungere.

</dd> <dt>

*ID* \[ istanza in\]
</dt> <dd>

Tipo: **BSTR**

Identificatore dell'istanza del dispositivo da aggiungere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RedirectDeviceType**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





