---
description: "Metodo IPortableDeviceValuesCollection::RemoveAt: il metodo RemoveAt rimuove l'elemento archiviato nella posizione specificata dall'indice specificato."
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: Metodo IPortableDeviceValuesCollection::RemoveAt (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7db15480906bee8181bb0fc589c4f3e30ce4753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083169"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a>Metodo IPortableDeviceValuesCollection::RemoveAt

Il **metodo RemoveAt** rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwIndex* \[ Pollici\]
</dt> <dd>

Specifica l'indice dell'elemento da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è riuscito.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | L'indice specificato non è compreso nell'intervallo.<br/> |



 

## <a name="remarks"></a>Commenti

È necessario specificare un indice in base zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




