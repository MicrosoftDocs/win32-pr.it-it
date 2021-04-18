---
description: Il metodo GetA recupera un elemento dalla raccolta in base a un indice in base zero.
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'Metodo IPortableDeviceValuesCollection:: GetA (PortableDeviceTypes. h)'
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
ms.openlocfilehash: ffbc65f39aab63189aa451005008f585c46bd8d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324511"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a>IPortableDeviceValuesCollection:: GetA (metodo)

Il metodo **Geta** recupera un elemento dalla raccolta in base a un indice in base zero.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

**DWORD** che specifica un indice in base zero nella raccolta.

</dd> <dt>

*ppValues* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore a un'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) dalla raccolta. Il chiamante è responsabile della richiamata della **versione** su questa interfaccia quando viene eseguita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è riuscito.<br/>                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L'indice in base zero passato non era compreso nell'intervallo.<br/>             |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Un argomento obbligatorio del puntatore è **null**.<br/>                             |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | La raccolta contiene un puntatore **IPortableDeviceValues** **null** .<br/> |



 

## <a name="remarks"></a>Commenti

Tutte le modifiche apportate ai valori nell'interfaccia recuperata verranno apportate alla versione archiviata nella raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




