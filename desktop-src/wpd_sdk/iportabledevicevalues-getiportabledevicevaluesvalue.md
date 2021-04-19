---
description: Il metodo GetIPortableDeviceValuesValue recupera un valore IPortableDeviceValues (Type VT \_ Unknown) specificato da una chiave.
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
title: 'Metodo IPortableDeviceValues:: GetIPortableDeviceValuesValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9583ea157c1e3395fd9814b1a2e78af3f1985b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332279"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluesvalue-method"></a>Metodo IPortableDeviceValues:: GetIPortableDeviceValuesValue

Il metodo **GetIPortableDeviceValuesValue** recupera un valore **IPORTABLEDEVICEVALUES** (Type VT \_ Unknown) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIPortableDeviceValuesValue(
  [in]  REFPROPERTYKEY        key,
  [out] IPortableDeviceValues **ppValue
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

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) recuperata. Il chiamante è responsabile della chiamata della **versione** sull'interfaccia recuperata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                                          |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *Key* non è un'interfaccia **IPortableDeviceValues** .<br/> |
| <dl> <dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt> </dl> | La proprietà specificata dalla *chiave* non è presente nella raccolta.<br/>                      |



 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [recupero di eventi del servizio supportati](retrieving-supported-events.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDeviceValuesValue**](iportabledevicevalues-setiportabledevicevaluesvalue.md)
</dt> <dt>

[Recupero degli eventi del servizio supportati](retrieving-supported-events.md)
</dt> <dt>

[Recupero delle funzionalità di rendering supportate da un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




