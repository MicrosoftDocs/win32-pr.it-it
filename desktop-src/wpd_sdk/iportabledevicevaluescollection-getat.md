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
ms.openlocfilehash: 2ad10a7b9cc3c252a0cee4cb71df05cb108e0a18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083259"
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

*valori ppValues* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore a [**un'interfaccia IPortableDeviceValues**](iportabledevicevalues.md) dalla raccolta. Il chiamante è responsabile della chiamata **di Release** su questa interfaccia al termine dell'operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è riuscito.<br/>                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L'indice in base zero passato non è compreso nell'intervallo.<br/>             |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>    | Un argomento del puntatore obbligatorio era **NULL.**<br/>                             |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | La raccolta contiene un **puntatore** **NULL IPortableDeviceValues.**<br/> |



 

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

 

 




