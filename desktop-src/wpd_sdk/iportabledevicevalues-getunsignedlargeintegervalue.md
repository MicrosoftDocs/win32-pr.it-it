---
description: Il metodo GetUnsignedLargeIntegerValue recupera un valore ULONGLONG (tipo VT \_ UI8) specificato da una chiave.
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: Metodo IPortableDeviceValues::GetUnsignedLargeIntegerValue (PortableDeviceTypes.h)
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
ms.openlocfilehash: df10faa20094623940e9694a5612c4f49b45f3c979d7e05df3239512cb021ab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194030"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a>Metodo IPortableDeviceValues::GetUnsignedLargeIntegerValue

Il **metodo GetUnsignedLargeIntegerValue** recupera un **valore ULONGLONG** (tipo VT \_ UI8) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ Pollici\]
</dt> <dd>

Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.

</dd> <dt>

*pValue* \[ Cambio\]
</dt> <dd>

Puntatore al valore **ULONGLONG** recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                        |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *key* non è di **tipo ULONGLONG.**<br/> |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(ERRORE \_ NON \_ TROVATO)**</dt> </dl> | La proprietà specificata da *key* non è presente nella raccolta.<br/>    |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetUnsignedLargeIntegerValue**](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




