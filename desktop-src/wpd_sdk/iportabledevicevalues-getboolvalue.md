---
description: Il metodo GetBoolValue recupera un valore booleano (tipo VT \_ bool) specificato da una chiave.
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: 'Metodo IPortableDeviceValues:: GetBoolValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8554fc30a1b66226f6e4f8de4e5d8ac0e8abfabf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326959"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a>Metodo IPortableDeviceValues:: GetBoolValue

Il metodo **GetBoolValue** recupera un valore **booleano** (tipo VT \_ bool) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
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

Puntatore al valore **bool** recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *Key* non è di tipo **bool** .<br/>   |
| <dl> <dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt> </dl> | La proprietà specificata dalla *chiave* non è presente nella raccolta.<br/> |



 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [impostazione delle proprietà per un singolo oggetto](setting-properties-for-a-single-object.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: SetBoolValue**](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[Recupero degli eventi del servizio supportati](retrieving-supported-events.md)
</dt> <dt>

[Impostazione delle proprietà per un singolo oggetto](setting-properties-for-a-single-object.md)
</dt> <dt>

[Scrittura di proprietà di contenuto-oggetto](writing-content-object-properties.md)
</dt> </dl>

 

 




