---
description: Il metodo Add aggiunge un elemento alla raccolta.
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'Metodo IPortableDevicePropVariantCollection:: Add (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d9d5b4ee664d2fbbcc78550b1af5a48874d153d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329893"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a>Metodo IPortableDevicePropVariantCollection:: Add

Il metodo **Add** aggiunge un elemento alla raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pValue* \[ in\]
</dt> <dd>

Puntatore a un nuovo oggetto **PROPVARIANT** da aggiungere alla raccolta. Questo metodo copia **PROPVARIANT** nella raccolta, quindi è necessario rilasciare la copia locale della variabile chiamando **PropVariantClear** dopo la chiamata a questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Quando VARTYPE for *pValue* è VT \_ vector o VT \_ Ui1, non è supportata l'impostazione e il recupero di un buffer di dimensioni **null** o zero. Ad esempio, non sono consentiti né pValue. Campo CAUB. pElems = **null** né pValue. Campo CAUB. cElems = 0.

Se un chiamante tenta di aggiungere un elemento di un VARTYPE diverso contenuto nella raccolta e il valore PROPVARIANT non può essere modificato automaticamente da questa interfaccia, questo metodo avrà esito negativo. Per modificare il tipo di raccolta manualmente, chiamare [**IPortableDevicePropVariantCollection:: ChangeType**](iportabledevicepropvariantcollection-changetype.md).

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [recupero di un identificatore di oggetto da un identificatore univoco permanente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Trasferimento del contenuto nel dispositivo](moving-content-on-the-device.md)
</dt> <dt>

[Recupero di un identificatore di oggetto da un identificatore univoco permanente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




