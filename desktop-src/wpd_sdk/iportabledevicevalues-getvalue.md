---
description: Il metodo GetValue recupera un valore PROPVARIANT specificato da una chiave.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: Metodo IPortableDeviceValues::GetValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cce387bfc08c48547603d8b30a3952952f1e2decf70e06986ea4fb477fe4fdc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843033"
---
# <a name="iportabledevicevaluesgetvalue-method"></a>Metodo IPortableDeviceValues::GetValue

Il **metodo GetValue** recupera un **valore PROPVARIANT** specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
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

Puntatore al valore **PROPVARIANT** recuperato. Al termine, il chiamante deve rilasciare la memoria chiamando **PropVariantClear.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(ERRORE \_ NON \_ TROVATO)**</dt> </dl> | La proprietà specificata da *key* non è presente nella raccolta.<br/> |



 

## <a name="remarks"></a>Commenti

Quando VARTYPE per *pValue* è VT VECTOR o \_ VT UI1, il recupero di un buffer NULL o di dimensioni \_ zero non è supportato.  Ad esempio, non sono consentiti pValue.caub.pElems = **NULL** o pValue.caub.cElems = 0.

Questo metodo può essere usato per recuperare un valore di qualsiasi tipo dalla raccolta. Tuttavia, se si conosce il tipo di valore in anticipo, usare uno dei metodi di recupero specializzati di questa interfaccia per evitare l'overhead di utilizzo diretto dei valori PROPVARIANT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> <dt>

[**IPortableDeviceValues::SetValue**](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




