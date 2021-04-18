---
description: Il metodo GetIPortableDeviceValuesCollectionValue recupera un valore IPortableDeviceValuesCollection (Type VT \_ Unknown) specificato da una chiave.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: 'Metodo IPortableDeviceValues:: GetIPortableDeviceValuesCollectionValue (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 3db3b8410ca82a97a41fdf45ee3f866cb8d2e4b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326958"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a>Metodo IPortableDeviceValues:: GetIPortableDeviceValuesCollectionValue

Il metodo **GetIPortableDeviceValuesCollectionValue** recupera un valore **IPORTABLEDEVICEVALUESCOLLECTION** (Type VT \_ Unknown) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ di in\]
</dt> <dd>

Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.

</dd> <dt>

*ppValue* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) recuperata. Il chiamante è responsabile della chiamata della **versione** sull'interfaccia recuperata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                                                    |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *Key* non è un'interfaccia **IPortableDeviceValuesCollection** .<br/> |
| <dl> <dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt> </dl> | La proprietà specificata dalla *chiave* non è presente nella raccolta.<br/>                                |



 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [recupero delle funzionalità di rendering supportate da un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[Recupero delle funzionalità di rendering supportate da un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




