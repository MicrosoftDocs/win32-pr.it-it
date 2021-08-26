---
description: 'Metodo IPortableDevicePropVariantCollection::Add: il metodo Add aggiunge un elemento alla raccolta.'
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: Metodo IPortableDevicePropVariantCollection::Add (PortableDeviceTypes.h)
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
ms.openlocfilehash: fd90e4702045200e4f2766f6dcdd661ff83b6cd3370970a22e3211eebfa13c90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055261"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a>Metodo IPortableDevicePropVariantCollection::Add

Il **metodo Add** aggiunge un elemento alla raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pValue* \[ Pollici\]
</dt> <dd>

Puntatore a un **nuovo oggetto PROPVARIANT** da aggiungere alla raccolta. Questo metodo copia **PROPVARIANT** nella raccolta, quindi è necessario rilasciare la copia locale della variabile chiamando **PropVariantClear** dopo aver chiamato questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Quando VARTYPE per *pValue* è VT VECTOR o \_ VT UI1, l'impostazione e il recupero di un buffer NULL o di dimensioni \_ zero non sono supportati.  Ad esempio, non sono consentiti pValue.caub.pElems = **NULL** o pValue.caub.cElems = 0.

Se un chiamante tenta di aggiungere un elemento di un VARTYPE diverso contenuto nella raccolta e il valore PROPVARIANT non può essere modificato automaticamente da questa interfaccia, questo metodo avrà esito negativo. Per modificare manualmente il tipo di raccolta, chiamare [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere Recupero di un identificatore di [oggetto da un identificatore univoco permanente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Spostamento di contenuto nel dispositivo](moving-content-on-the-device.md)
</dt> <dt>

[Recupero di un identificatore di oggetto da un identificatore univoco permanente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




