---
description: Il metodo GetA recupera un PROPERTYKEY dalla raccolta in base all'indice.
ms.assetid: 9a3c5c28-39b4-4d53-a8d7-0f5a0d4d89ad
title: 'Metodo IPortableDeviceKeyCollection:: GetA (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: b75285f6dcdb0961312fa1db8f5c912b771bd786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329895"
---
# <a name="iportabledevicekeycollectiongetat-method"></a>IPortableDeviceKeyCollection:: GetA (metodo)

Il metodo **Geta** recupera un **PropertyKey** dalla raccolta in base all'indice.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPERTYKEY *pKey
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

**DWORD** che contiene l'indice della chiave da recuperare.

</dd> <dt>

*pKey* \[ out\]
</dt> <dd>

Puntatore a un oggetto **PropertyKey** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è riuscito.<br/>                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L'indice passato non è compreso nell'intervallo.<br/>     |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Un argomento obbligatorio del puntatore è **null**.<br/> |



 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [recupero di eventi del servizio supportati](retrieving-supported-events.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[Recupero degli eventi del servizio supportati](retrieving-supported-events.md)
</dt> <dt>

[Recupero di metodi di servizio supportati](retrieving-supported-methods.md)
</dt> </dl>

 

 




