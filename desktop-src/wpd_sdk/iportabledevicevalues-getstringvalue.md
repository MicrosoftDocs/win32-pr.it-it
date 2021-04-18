---
description: Il metodo GetStringValue recupera un valore stringa (di tipo VT \_ LPWSTR) specificato da una chiave.
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
title: 'Metodo IPortableDeviceValues:: GetStringValue (PortableDeviceTypes. h)'
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
ms.openlocfilehash: fdb4741c36445af686b7721e1f5f04dd3e45f1e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331560"
---
# <a name="iportabledevicevaluesgetstringvalue-method"></a>Metodo IPortableDeviceValues:: GetStringValue

Il metodo **GetStringValue** recupera un valore stringa (di tipo VT \_ LPWSTR) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStringValue(
  [in]  REFPROPERTYKEY key,
  [out] LPWSTR         *pValue
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

Puntatore al valore **LPWSTR** recuperato. Il chiamante è responsabile della chiamata a **CoTaskMemFree** per rilasciare la memoria.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                           |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                      |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *Key* non è un tipo **LPWSTR** .<br/> |
| <dl> <dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt> </dl> | La proprietà specificata dalla *chiave* non è presente nella raccolta.<br/>  |



 

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

[**IPortableDeviceValues:: GetA**](iportabledevicevalues-getat.md)
</dt> <dt>

[**IPortableDeviceValues:: SetStringValue**](iportabledevicevalues-setstringvalue.md)
</dt> <dt>

[Recupero degli eventi del servizio supportati](retrieving-supported-events.md)
</dt> <dt>

[Recupero dei formati di servizio supportati](retrieving-supported-formats.md)
</dt> <dt>

[Recupero di metodi di servizio supportati](retrieving-supported-methods.md)
</dt> </dl>

 

 




