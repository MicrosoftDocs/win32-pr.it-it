---
description: Il metodo SetBufferValue aggiunge un nuovo valore BYTE \* (tipo VT \_ VECTOR \| VT \_ UI1) o ne sovrascrive uno esistente.
ms.assetid: 6c421240-2ff8-4862-bd90-1feee5d15a8d
title: Metodo IPortableDeviceValues::SetBufferValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 25a087c6f2d1e254e225f82ef794915898fbc20c7203fe20315d51f78e9770f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055101"
---
# <a name="iportabledevicevaluessetbuffervalue-method"></a>Metodo IPortableDeviceValues::SetBufferValue

Il **metodo SetBufferValue** aggiunge un nuovo valore **BYTE** \* (tipo VT \_ VECTOR \| VT \_ UI1) o ne sovrascrive uno esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetBufferValue(
  [in] REFPROPERTYKEY key,
  [in] BYTE           *pValue,
  [in] DWORD          cbValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ Pollici\]
</dt> <dd>

**REFPROPERTYKEY che** specifica l'elemento da creare o sovrascrivere.

</dd> <dt>

*pValue* \[ Pollici\]
</dt> <dd>

Byte **\* che** contiene i dati da scrivere nell'elemento. I dati del buffer inviati vengono copiati nell'interfaccia , in modo che il chiamante possa liberare questo buffer dopo aver fatto questa chiamata.

</dd> <dt>

*cbValue* \[ Pollici\]
</dt> <dd>

Dimensione del valore a cui punta *pValue*, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Se un valore esistente ha la stessa chiave specificata dal parametro *key,* sovrascrive il valore esistente senza alcun avviso. La memoria della chiave esistente viene rilasciata in modo appropriato.

**L'impostazione di un** buffer NULL o di dimensione zero non è supportata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetBufferValue**](iportabledevicevalues-getbuffervalue.md)
</dt> </dl>

 

 




