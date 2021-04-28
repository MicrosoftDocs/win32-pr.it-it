---
description: 'Metodo IPortableDeviceValuesCollection::Add: il metodo Add aggiunge un elemento alla raccolta.'
ms.assetid: 3b06abc4-f0ab-4b02-b3a7-360615f86a2a
title: Metodo IPortableDeviceValuesCollection::Add (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 765100e1272fc6766e9f305f37f3b699bd96beb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083242"
---
# <a name="iportabledevicevaluescollectionadd-method"></a>Metodo IPortableDeviceValuesCollection::Add

Il **metodo Add** aggiunge un elemento alla raccolta .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Add(
  [in] IPortableDeviceValues *pValues
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pValues* \[ Pollici\]
</dt> <dd>

Puntatore a **un'interfaccia IPortableDeviceValues** da aggiungere alla raccolta. L'interfaccia non viene effettivamente copiata, **ma su di** essa viene chiamato AddRef.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | La memoria disponibile non è sufficiente per aggiungere il valore alla raccolta.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




