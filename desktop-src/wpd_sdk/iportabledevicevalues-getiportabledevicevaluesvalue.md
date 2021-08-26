---
description: Il metodo GetIPortableDeviceValuesValues Recupera un valore IPortableDeviceValues (tipo VT \_ UNKNOWN) specificato da una chiave.
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
title: Metodo IPortableDeviceValues::GetIPortableDeviceValuesValuesValue (PortableDeviceTypes.h)
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
ms.openlocfilehash: aeec29bf3d9cf18bcf54c885d46d159c21c661a1e886903110952cd3a23c540e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055161"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluesvalue-method"></a>Metodo IPortableDeviceValues::GetIPortableDeviceValuesValuesValue

Il **metodo GetIPortableDeviceValuesValues Recupera** un valore **IPortableDeviceValues** (tipo VT \_ UNKNOWN) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIPortableDeviceValuesValue(
  [in]  REFPROPERTYKEY        key,
  [out] IPortableDeviceValues **ppValue
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

Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IPortableDeviceValues recuperata.**](iportabledevicevalues.md) Il chiamante è responsabile della chiamata **di Release** sull'interfaccia recuperata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                                          |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *key* non è **un'interfaccia IPortableDeviceValues.**<br/> |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(ERRORE \_ NON \_ TROVATO)**</dt> </dl> | La proprietà specificata da *key* non è presente nell'insieme.<br/>                      |



 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [Recupero di eventi del servizio supportati.](retrieving-supported-events.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDeviceValuesValuesValue**](iportabledevicevalues-setiportabledevicevaluesvalue.md)
</dt> <dt>

[Recupero di eventi del servizio supportati](retrieving-supported-events.md)
</dt> <dt>

[Recupero delle funzionalità di rendering supportate da un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




