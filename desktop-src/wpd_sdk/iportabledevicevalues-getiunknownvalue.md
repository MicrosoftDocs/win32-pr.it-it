---
description: Il metodo GetIUnknownValue recupera un valore dell'interfaccia IUnknown (tipo VT \_ UNKNOWN) specificato da una chiave.
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: Metodo IPortableDeviceValues::GetIUnknownValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: daf1164fefdc414a84508e4b295620af3cb671e9da624dd60cc08541c5c4fd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963650"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a>Metodo IPortableDeviceValues::GetIUnknownValue

Il **metodo GetIUnknownValue** recupera un **valore dell'interfaccia IUnknown** (tipo VT \_ UNKNOWN) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ Pollici\]
</dt> <dd>

Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.

</dd> <dt>

*ppValue* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore **all'interfaccia IUnknown** recuperata. Il chiamante è responsabile della chiamata **di Release** sull'interfaccia recuperata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                             |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *key* non è **un'interfaccia IUnknown.**<br/> |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(ERRORE \_ NON \_ TROVATO)**</dt> </dl> | La proprietà specificata da *key* non è presente nell'insieme.<br/>         |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIUnknownValue**](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




