---
description: Il metodo GetSerializedSize calcola la dimensione del buffer necessaria per mantenere un'interfaccia IPortableDeviceValues serializzata.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'Metodo IWpdSerializer:: GetSerializedSize (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7b50f7f6158145cd71125b5e5f26649712bb065b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324499"
---
# <a name="iwpdserializergetserializedsize-method"></a>Metodo IWpdSerializer:: GetSerializedSize

Il metodo **GetSerializedSize** calcola la dimensione del buffer necessaria per mantenere un'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) serializzata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSource* \[ in\]
</dt> <dd>

Puntatore a un'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) la cui dimensione si desidera richiedere.

</dd> <dt>

*pdwSize* \[ out\]
</dt> <dd>

Puntatore a un **valore DWORD** che indica le dimensioni del buffer necessarie per serializzare *pSource* in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                       |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un argomento obbligatorio del puntatore è **null**.<br/>                   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria disponibile insufficiente per creare il buffer.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




