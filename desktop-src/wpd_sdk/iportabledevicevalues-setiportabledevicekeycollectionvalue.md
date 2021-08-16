---
description: Il metodo SetIPortableDeviceKeyCollectionValue aggiunge un nuovo valore SetIPortableDeviceKeyCollectionValue (tipo VT UNKNOWN) o ne \_ sovrascrive uno esistente.
ms.assetid: f470cb89-e7a0-470d-83d1-eb643b062e45
title: Metodo IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 100dd614978260824fa14cefc22e1bf7fdd5d11e474e4f58124685fc8d8f2eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963570"
---
# <a name="iportabledevicevaluessetiportabledevicekeycollectionvalue-method"></a>Metodo IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue

Il **metodo SetIPortableDeviceKeyCollectionValue** aggiunge un nuovo valore **SetIPortableDeviceKeyCollectionValue** (tipo VT UNKNOWN) o ne \_ sovrascrive uno esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetIPortableDeviceKeyCollectionValue(
  [in] REFPROPERTYKEY               key,
  [in] IPortableDeviceKeyCollection *pValue
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

Puntatore a **un'interfaccia IPortableDeviceKeyCollection** che specifica il nuovo valore. L'SDK copia un riferimento all'interfaccia inviata e chiama **AddRef** su di essa.

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

[**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)
</dt> </dl>

 

 




