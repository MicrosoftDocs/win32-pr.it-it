---
description: Il metodo SetStringValue aggiunge un nuovo valore stringa (tipo VT \_ LPWSTR) o ne sovrascrive uno esistente.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: Metodo IPortableDeviceValues::SetStringValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c00195823d71a59e706af1c0a627670f583776140772c3b8634ac10d7d95919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806861"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a>Metodo IPortableDeviceValues::SetStringValue

Il **metodo SetStringValue** aggiunge un nuovo valore stringa (tipo VT \_ LPWSTR) o ne sovrascrive uno esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ Pollici\]
</dt> <dd>

**RefPROPERTYKEY che** specifica l'elemento da creare o sovrascrivere.

</dd> <dt>

*Valore* \[ Pollici\]
</dt> <dd>

Oggetto **LPCWSTR** che specifica il nuovo valore. La stringa viene copiata, in modo che il chiamante possa rilasciare la memoria allocata per questo valore dopo la chiamata a questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Qualsiasi memoria della chiave esistente verrà rilasciata in modo appropriato.

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [Specifica delle informazioni client](specifying-client-information.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Aggiunta di una risorsa a un oggetto](adding-a-resource-to-an-object.md)
</dt> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[Impostazione delle proprietà per un singolo oggetto](setting-properties-for-a-single-object.md)
</dt> <dt>

[Impostazione delle proprietà per più oggetti](setting-properties-for-multiple-objects.md)
</dt> <dt>

[Specifica delle informazioni sul client](specifying-client-information.md)
</dt> <dt>

[Scrittura di proprietà content-object](writing-content-object-properties.md)
</dt> </dl>

 

 




