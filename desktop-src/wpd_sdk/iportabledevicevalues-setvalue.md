---
description: Il metodo SetValue aggiunge un nuovo valore PROPVARIANT o ne sovrascrive uno esistente.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: Metodo IPortableDeviceValues::SetValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f6af975b2876a177207df4f57bfe1f76d78a4b7239ce6d9c4cfcab52f0cf9042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055041"
---
# <a name="iportabledevicevaluessetvalue-method"></a>Metodo IPortableDeviceValues::SetValue

Il **metodo SetValue** aggiunge un nuovo **valore PROPVARIANT** o ne sovrascrive uno esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
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

Oggetto **PROPVARIANT** che specifica il nuovo valore. L'SDK copia il valore, in modo che il chiamante possa rilasciare la variabile locale chiamando **PropVariantClear** dopo aver chiamato questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Quando VARTYPE per *pValue* è VT VECTOR o \_ VT UI1, l'impostazione di un buffer NULL o \_ di dimensioni zero non è supportata.  Ad esempio, né pValue.caub.pElems = **NULL** né pValue.caub.cElems = 0 sono consentiti.

Questo metodo può essere utilizzato per recuperare un valore di qualsiasi tipo dalla raccolta. Tuttavia, se si conosce in anticipo il tipo di valore, usare uno dei metodi **Set...** specializzati di questa interfaccia per evitare l'overhead di utilizzo diretto dei valori PROPVARIANT.

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

[**IPortableDeviceValues::GetValue**](iportabledevicevalues-getvalue.md)
</dt> <dt>

[**IPortableDeviceValues::RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




