---
description: Il metodo GetStringValue recupera un valore stringa (tipo VT \_ LPWSTR) specificato da una chiave.
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
title: Metodo IPortableDeviceValues::GetStringValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7d8a9703a359a2de13ec96ff3faf46ea9e49fb1fc467cdade56d799503f1b8cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806961"
---
# <a name="iportabledevicevaluesgetstringvalue-method"></a>Metodo IPortableDeviceValues::GetStringValue

Il **metodo GetStringValue** recupera un valore stringa (tipo VT \_ LPWSTR) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStringValue(
  [in]  REFPROPERTYKEY key,
  [out] LPWSTR         *pValue
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

Puntatore al valore **LPWSTR** recuperato. Il chiamante è responsabile della chiamata **a CoTaskMemFree** per rilasciare la memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                           |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                      |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *key* non è un **tipo LPWSTR.**<br/> |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(ERRORE \_ NON \_ TROVATO)**</dt> </dl> | La proprietà specificata da *key* non è presente nell'insieme.<br/>  |



 

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

[**IPortableDeviceValues::GetAt**](iportabledevicevalues-getat.md)
</dt> <dt>

[**IPortableDeviceValues::SetStringValue**](iportabledevicevalues-setstringvalue.md)
</dt> <dt>

[Recupero di eventi del servizio supportati](retrieving-supported-events.md)
</dt> <dt>

[Recupero di formati di servizio supportati](retrieving-supported-formats.md)
</dt> <dt>

[Recupero di metodi di servizio supportati](retrieving-supported-methods.md)
</dt> </dl>

 

 




