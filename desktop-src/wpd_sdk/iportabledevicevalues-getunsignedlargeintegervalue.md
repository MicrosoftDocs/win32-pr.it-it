---
description: Il metodo GetUnsignedLargeIntegerValue recupera un valore ULONGLONG (di tipo VT \_ UI8) specificato da una chiave.
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: 'Metodo IPortableDeviceValues:: GetUnsignedLargeIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 48f6093f32d43737b1999c3474f74569ecd3f8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325812"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a>Metodo IPortableDeviceValues:: GetUnsignedLargeIntegerValue

Il metodo **GetUnsignedLargeIntegerValue** recupera un valore **ULONGLONG** (di tipo VT \_ UI8) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ di in\]
</dt> <dd>

Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Puntatore al valore **ULONGLONG** recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                        |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *Key* non è di tipo **ULONGLONG** .<br/> |
| <dl> <dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt> </dl> | La proprietà specificata dalla *chiave* non è presente nella raccolta.<br/>    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetUnsignedLargeIntegerValue**](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




