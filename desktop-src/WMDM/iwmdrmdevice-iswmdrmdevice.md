---
title: Metodo IWMDRMDevice IsWMDRMDevice
description: Il metodo IsWMDRMDevice determina se il dispositivo supporta Windows Media DRM 10 per dispositivi portatili.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Metodo IsWMDRMDevice windows Media Device Manager
- Metodo IsWMDRMDevice windows Media Device Manager , interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice windows Media Device Manager , metodo IsWMDRMDevice
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60ee225267ce2301e9a2dad392d72ce72b0e698872cd3fd54ab3e50a07043477
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957261"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a>Metodo IWMDRMDevice::IsWMDRMDevice

Il **metodo IsWMDRMDevice** determina se il dispositivo supporta Windows Media DRM 10 per dispositivi portatili.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdwVersion* \[ Cambio\]
</dt> <dd>

Versione di Windows Media DRM 10 per dispositivi portatili, il cui valore è 0x00010000.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





