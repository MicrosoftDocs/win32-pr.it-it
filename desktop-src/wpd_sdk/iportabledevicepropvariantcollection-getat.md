---
description: 'Metodo IPortableDevicePropVariantCollection::GetAt: il metodo GetAt recupera un elemento dalla raccolta in base a un indice in base zero.'
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: Metodo IPortableDevicePropVariantCollection::GetAt (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 02fa273b3bedea78884e15d2dedb5b7d2f675c78330c735e3bfb1896bc9d5199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963730"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a>Metodo IPortableDevicePropVariantCollection::GetAt

Il **metodo GetAt** recupera un elemento dalla raccolta in base a un indice in base zero.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwIndex* \[ Pollici\]
</dt> <dd>

**Valore DWORD** che contiene l'indice in base zero dell'elemento da recuperare.

</dd> <dt>

*pValue* \[ Cambio\]
</dt> <dd>

Puntatore a **una struttura PROPVARIANT.** Il chiamante è responsabile del liberare la memoria chiamando **PropVariantClear.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è riuscito.<br/>                          |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>    | Un argomento del puntatore obbligatorio era **NULL.**<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L'indice passato non è compreso nell'intervallo.<br/> |



 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [Recupero delle categorie funzionali supportate da un dispositivo.](retrieving-the-functional-categories-supported-by-a-device.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Recupero di un identificatore di oggetto da un identificatore univoco permanente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[Recupero di eventi del servizio supportati](retrieving-supported-events.md)
</dt> <dt>

[Recupero di formati di servizio supportati](retrieving-supported-formats.md)
</dt> <dt>

[Recupero di metodi di servizio supportati](retrieving-supported-methods.md)
</dt> <dt>

[Recupero dei tipi di contenuto supportati da un dispositivo](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[Recupero delle categorie funzionali supportate da un dispositivo](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Recupero degli identificatori di oggetto funzionale per un dispositivo](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[Recupero delle funzionalità di rendering supportate da un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[Impostazione delle proprietà per più oggetti](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




