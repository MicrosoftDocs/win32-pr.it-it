---
description: Il metodo GetBufferFromIPortableDeviceValues serializza un'interfaccia IPortableDeviceValues inviata in una matrice di byte allocata. La matrice di byte restituita viene allocata per il chiamante e deve essere liberata dal chiamante usando CoTaskMemFree.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: Metodo IWpdSerializer::GetBufferFromIPortableDeviceValues (PortableDeviceTypes.h)
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
ms.openlocfilehash: 10a483331d15c09de8398d11e940453d8f239e2207fdefb82d86fd4bb1460daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843014"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a>Metodo IWpdSerializer::GetBufferFromIPortableDeviceValues

Il **metodo GetBufferFromIPortableDeviceValues** serializza un'interfaccia **IPortableDeviceValues** inviata in una matrice di byte allocata. La matrice di byte restituita viene allocata per il chiamante e deve essere liberata dal chiamante usando **CoTaskMemFree**.

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

*pSource* \[ Pollici\]
</dt> <dd>

Puntatore a [**un'interfaccia IPortableDeviceValues**](iportabledevicevalues.md) da serializzare.

</dd> <dt>

*ppBuffer* \[ Cambio\]
</dt> <dd>

Puntatore a **un oggetto BYTE _ che contiene i dati \* *serializzati. Windows I dispositivi portatili allocano questa memoria; Il chiamante deve liberarlo chiamando _* CoTaskMemFree**.

</dd> <dt>

*pdwBufferSize* \[ Cambio\]
</dt> <dd>

Puntatore a **un valore DWORD** che specifica le dimensioni del buffer allocato, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                       |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Un argomento del puntatore obbligatorio era **NULL.**<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per creare il buffer.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




