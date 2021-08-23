---
description: Il metodo GetBoolValue recupera un valore booleano (tipo VT \_ BOOL) specificato da una chiave.
ms.assetid: cb5fed7a-50b5-4af1-806a-c6582409d265
title: Metodo IPortableDeviceValues::GetBoolValue (PortableDeviceTypes.h)
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
ms.openlocfilehash: 26006d151cd3adfc9f1c3f892cca05724c4ba54dc273cbbf58bd96c5779ccefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807021"
---
# <a name="iportabledevicevaluesgetboolvalue-method"></a>Metodo IPortableDeviceValues::GetBoolValue

Il **metodo GetBoolValue** recupera un **valore booleano** (tipo VT \_ BOOL) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBoolValue(
  [in]  REFPROPERTYKEY key,
  [out] BOOL           *pValue
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

Puntatore al valore **BOOL** recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *key* non è di **tipo BOOL.**<br/>   |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(ERRORE \_ NON \_ TROVATO)**</dt> </dl> | La proprietà specificata da *key* non è presente nell'insieme.<br/> |



 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [Impostazione delle proprietà per un singolo oggetto](setting-properties-for-a-single-object.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetBoolValue**](iportabledevicevalues-setboolvalue.md)
</dt> <dt>

[Recupero di eventi del servizio supportati](retrieving-supported-events.md)
</dt> <dt>

[Impostazione delle proprietà per un singolo oggetto](setting-properties-for-a-single-object.md)
</dt> <dt>

[Scrittura di proprietà content-object](writing-content-object-properties.md)
</dt> </dl>

 

 




