---
description: 'Metodo IPortableDeviceValuesCollection::GetAt: il metodo GetAt recupera un elemento dalla raccolta in base a un indice in base zero.'
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: Metodo IPortableDeviceValuesCollection::GetAt (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 089c6c5c523b6f05f91efb5524904c942a539a7ebbb3cd863c1c07d413cdf1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704631"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a>Metodo IPortableDeviceValuesCollection::GetAt

Il **metodo GetAt** recupera un elemento dalla raccolta in base a un indice in base zero.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwIndex* \[ Pollici\]
</dt> <dd>

**Valore DWORD** che specifica un indice in base zero nella raccolta.

</dd> <dt>

*ppValues* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore a [**un'interfaccia IPortableDeviceValues**](iportabledevicevalues.md) dalla raccolta. Il chiamante è responsabile della chiamata **a Release** su questa interfaccia al termine dell'operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è riuscito.<br/>                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L'indice in base zero passato non è compreso nell'intervallo.<br/>             |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>    | Un argomento del puntatore obbligatorio era **NULL.**<br/>                             |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl> | La raccolta contiene un **puntatore** **NULL IPortableDeviceValues.**<br/> |



 

## <a name="remarks"></a>Commenti

Tutte le modifiche apportate ai valori nell'interfaccia recuperata verranno apportate alla versione archiviata nella raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




