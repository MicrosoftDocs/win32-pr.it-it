---
description: Il metodo GetSignedIntegerValue recupera un valore LONG (tipo VT \_ I4) specificato da una chiave.
ms.assetid: d2291a64-d0b3-4a30-a37c-2b6cd9880a11
title: Metodo IPortableDeviceValues::GetSignedIntegerValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5b2bab46a7509ce858af9db3c7c4785de5161b64e86c0f3c280fdad00ebe5f64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843004"
---
# <a name="iportabledevicevaluesgetsignedintegervalue-method"></a>Metodo IPortableDeviceValues::GetSignedIntegerValue

Il **metodo GetSignedIntegerValue** recupera un **valore LONG** (tipo VT \_ I4) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONG           *pValue
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

Puntatore al valore **LONG** recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *key* non è di **tipo LONG.**<br/>   |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(ERRORE \_ NON \_ TROVATO)**</dt> </dl> | La proprietà specificata da *key* non è presente nell'insieme.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetSignedIntegerValue**](iportabledevicevalues-setsignedintegervalue.md)
</dt> </dl>

 

 




