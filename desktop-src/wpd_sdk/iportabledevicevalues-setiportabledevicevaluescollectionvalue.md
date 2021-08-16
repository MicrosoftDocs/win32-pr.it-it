---
description: Il metodo SetIPortableDeviceValuesCollectionValue aggiunge un nuovo valore IPortableDeviceValuesCollection (tipo VT UNKNOWN) o ne \_ sovrascrive uno esistente.
ms.assetid: 29bdecaa-4820-4b1d-be59-ae82f7715a53
title: Metodo IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7f015333a8d384743d0e8ea16000252a4e60fd24ab0637b92ee3d85ddb42a1c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697089"
---
# <a name="iportabledevicevaluessetiportabledevicevaluescollectionvalue-method"></a>Metodo IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue

Il **metodo SetIPortableDeviceValuesCollectionValue** aggiunge un nuovo valore **IPortableDeviceValuesCollection** (tipo VT UNKNOWN) o ne \_ sovrascrive uno esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetIPortableDeviceValuesCollectionValue(
  [in] REFPROPERTYKEY                  key,
  [in] IPortableDeviceValuesCollection *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ Pollici\]
</dt> <dd>

**RefPROPERTYKEY che** specifica l'elemento da creare o sovrascrivere.

</dd> <dt>

*pValue* \[ Pollici\]
</dt> <dd>

Puntatore a **un'interfaccia IPortableDeviceValuesCollection** che specifica il nuovo valore. L'SDK copia un riferimento all'interfaccia inviata e chiama **AddRef** su di essa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Se un valore esistente ha la stessa chiave specificata dal parametro *key,* sovrascrive il valore esistente senza alcun avviso. La memoria della chiave esistente viene rilasciata in modo appropriato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




