---
title: Metodo IWMDRMDevice IsWMDRMDevice
description: Il metodo IsWMDRMDevice determina se il dispositivo supporta Windows Media DRM 10 per i dispositivi portatili.
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- Metodo IsWMDRMDevice Windows Media Gestione dispositivi
- Metodo IsWMDRMDevice Windows Media Gestione dispositivi, interfaccia IWMDRMDevice
- Interfaccia IWMDRMDevice Windows Media Gestione dispositivi, metodo IsWMDRMDevice
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
ms.openlocfilehash: ca9cb79598ea41a996748e383c8fdfc63364dd6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327401"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a>Metodo IWMDRMDevice:: IsWMDRMDevice

Il metodo **IsWMDRMDevice** determina se il dispositivo supporta Windows Media DRM 10 per i dispositivi portatili.

## <a name="syntax"></a>Sintassi


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pdwVersion* \[ out\]
</dt> <dd>

Versione di Windows Media DRM 10 per dispositivi portatili, il cui valore è 0x00010000.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Libreria<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





