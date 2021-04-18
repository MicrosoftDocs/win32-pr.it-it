---
description: Il metodo GetBufferFromIPortableDeviceValues serializza un'interfaccia IPortableDeviceValues inviata in una matrice di byte allocata. La matrice di byte restituita è allocata per il chiamante e deve essere liberata dal chiamante utilizzando CoTaskMemFree.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'Metodo IWpdSerializer:: GetBufferFromIPortableDeviceValues (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44f4e9e7011e6a4766183307e81ef7e783da899f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324501"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a>Metodo IWpdSerializer:: GetBufferFromIPortableDeviceValues

Il metodo **GetBufferFromIPortableDeviceValues** serializza un'interfaccia **IPortableDeviceValues** inviata in una matrice di byte allocata. La matrice di byte restituita è allocata per il chiamante e deve essere liberata dal chiamante utilizzando **CoTaskMemFree**.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSource* \[ in\]
</dt> <dd>

Puntatore a un'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) da serializzare.

</dd> <dt>

*ppBuffer* \[ out\]
</dt> <dd>

Puntatore a un **byte \* *_ che contiene i dati serializzati. I dispositivi portatili Windows allocano questa memoria; il chiamante deve liberarlo chiamando _* CoTaskMemFree**.

</dd> <dt>

*pdwBufferSize* \[ out\]
</dt> <dd>

Puntatore a un **valore DWORD** che specifica la dimensione del buffer allocato, in byte.

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

 

 




