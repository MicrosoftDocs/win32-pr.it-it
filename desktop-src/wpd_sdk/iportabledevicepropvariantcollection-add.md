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
ms.openlocfilehash: 7aed732cb92ea7e0f2fb3c2ebdd615f643bc3107
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112459"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a>Metodo IPortableDevicePropVariantCollection::Add

Il **metodo Add** aggiunge un elemento alla raccolta .

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

Puntatore a un **nuovo oggetto PROPVARIANT** da aggiungere alla raccolta. Questo metodo copia **PROPVARIANT** nella raccolta, pertanto è necessario rilasciare la copia locale della variabile chiamando **PropVariantClear** dopo aver chiamato questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Quando VARTYPE per *pValue* è VT VECTOR o \_ VT UI1, l'impostazione e il recupero di un buffer NULL o di dimensioni \_ zero non sono supportati.  Ad esempio, né pValue.caub.pElems = **NULL** né pValue.caub.cElems = 0 sono consentiti.

Se un chiamante tenta di aggiungere un elemento di un tipo VARTYPE diverso contenuto nella raccolta e il valore PROPVARIANT non può essere modificato automaticamente da questa interfaccia, questo metodo avrà esito negativo. Per modificare manualmente il tipo di raccolta, chiamare [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere Recupero di un identificatore di [oggetto da un identificatore univoco persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Spostamento del contenuto nel dispositivo](moving-content-on-the-device.md)
</dt> <dt>

[Recupero di un identificatore di oggetto da un identificatore univoco permanente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




