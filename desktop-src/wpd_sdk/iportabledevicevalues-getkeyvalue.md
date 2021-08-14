---
description: Il metodo GetKeyValue recupera un valore PROPERTYKEY specificato da una chiave.
ms.assetid: 2c92b1c0-3ea6-4a14-8b63-d57752b649b8
title: Metodo IPortableDeviceValues::GetKeyValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fb22fa8f93365cb7b0bc1f29b479683728b508a973a8702f5b86cc2605d0445d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194021"
---
# <a name="iportabledevicevaluesgetkeyvalue-method"></a>Metodo IPortableDeviceValues::GetKeyValue

Il **metodo GetKeyValue** recupera un **valore PROPERTYKEY** specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetKeyValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPERTYKEY    *pValue
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

Puntatore al valore **PROPERTYKEY** recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                               |
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                          |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *key* non è di **tipo PROPERTYKEY.**<br/> |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(ERRORE \_ NON \_ TROVATO)**</dt> </dl> | La proprietà specificata da *key* non è presente nell'insieme.<br/>      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetKeyValue**](iportabledevicevalues-setkeyvalue.md)
</dt> </dl>

 

 




