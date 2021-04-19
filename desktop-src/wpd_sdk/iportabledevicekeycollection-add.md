---
description: Il metodo Add aggiunge una chiave di proprietà alla raccolta.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'Metodo IPortableDeviceKeyCollection:: Add (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e43fea25a08969b2ae8169884d51ddc46f8c7136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332119"
---
# <a name="iportabledevicekeycollectionadd-method"></a>Metodo IPortableDeviceKeyCollection:: Add

Il metodo **Add** aggiunge una chiave di proprietà alla raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ di in\]
</dt> <dd>

Oggetto **REFPROPERTYKEY** da aggiungere alla raccolta. Questo metodo copia la chiave nella raccolta, in modo che sia possibile rilasciare la variabile locale dopo la chiamata a questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                                  |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per aggiungere la chiave alla raccolta.<br/> |



 

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [recupero delle proprietà per un singolo oggetto](retrieving-properties-for-a-single-object.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[Recupero proprietà contenuto-oggetto](retrieving-content-object-properties.md)
</dt> <dt>

[Recupero di proprietà per un singolo oggetto](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[Recupero delle funzionalità di rendering supportate da un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




