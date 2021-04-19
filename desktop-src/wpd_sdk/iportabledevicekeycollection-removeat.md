---
description: Il metodo RemoveAt rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: 'Metodo IPortableDeviceKeyCollection:: RemoveAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f4e126ef5fcad74b7cee5f748322f15e75481e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332108"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a>Metodo IPortableDeviceKeyCollection:: RemoveAt

Il metodo **RemoveAt** rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Specifica l'indice dell'elemento da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è riuscito.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L'indice specificato non è compreso nell'intervallo.<br/> |



 

## <a name="remarks"></a>Commenti

È necessario specificare un indice in base zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> </dl>

 

 




