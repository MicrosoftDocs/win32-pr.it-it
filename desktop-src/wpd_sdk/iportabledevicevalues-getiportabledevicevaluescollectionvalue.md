---
description: Il metodo GetIPortableDeviceValuesCollectionValue recupera un valore IPortableDeviceValuesCollection (tipo VT \_ UNKNOWN) specificato da una chiave.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: Metodo IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cbbea545f0f3c75281c5abb7e68795750521251392529d037bf18682e84dc436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697079"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a>Metodo IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue

Il **metodo GetIPortableDeviceValuesCollectionValue** recupera un valore **IPortableDeviceValuesCollection** (tipo VT \_ UNKNOWN) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
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

Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) recuperata. Il chiamante è responsabile della chiamata **di Release** sull'interfaccia recuperata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                                                    |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *key* non è **un'interfaccia IPortableDeviceValuesCollection.**<br/> |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(ERRORE \_ NON \_ TROVATO)**</dt> </dl> | La proprietà specificata da *key* non è presente nell'insieme.<br/>                                |



 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere Recupero delle [funzionalità di rendering supportate da un dispositivo.](retrieving-the-rendering-capabilities-supported-by-a-device.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[Recupero delle funzionalità di rendering supportate da un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




