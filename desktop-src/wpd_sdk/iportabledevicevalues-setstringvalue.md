---
description: Il metodo SetStringValue aggiunge un nuovo valore stringa (digitare VT \_ LPWSTR) o sovrascrive uno esistente.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'Metodo IPortableDeviceValues:: SetStringValue (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 163b5cd81ce8da64fc6d9f4304de5783b248522f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326855"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a>Metodo IPortableDeviceValues:: SetStringValue

Il metodo **SetStringValue** aggiunge un nuovo valore stringa (digitare VT \_ LPWSTR) o sovrascrive uno esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ di in\]
</dt> <dd>

Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.

</dd> <dt>

*Valore* \[ di in\]
</dt> <dd>

Oggetto **LPCWSTR** che specifica il nuovo valore. La stringa viene copiata, quindi il chiamante può rilasciare la memoria allocata per questo valore dopo la chiamata a questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Eventuali memorie chiave esistenti verranno rilasciate in modo appropriato.

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [specifica delle informazioni client](specifying-client-information.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Aggiunta di una risorsa a un oggetto](adding-a-resource-to-an-object.md)
</dt> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[Impostazione delle proprietà per un singolo oggetto](setting-properties-for-a-single-object.md)
</dt> <dt>

[Impostazione delle proprietà per più oggetti](setting-properties-for-multiple-objects.md)
</dt> <dt>

[Specifica delle informazioni client](specifying-client-information.md)
</dt> <dt>

[Scrittura di proprietà di contenuto-oggetto](writing-content-object-properties.md)
</dt> </dl>

 

 




