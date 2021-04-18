---
description: Il metodo GetIPortableDeviceValuesFromBuffer deserializza una matrice di byte in un'interfaccia IPortableDeviceValues.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'Metodo IWpdSerializer:: GetIPortableDeviceValuesFromBuffer (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324497"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a>Metodo IWpdSerializer:: GetIPortableDeviceValuesFromBuffer

Il metodo **GetIPortableDeviceValuesFromBuffer** deserializza una matrice di byte in un'interfaccia **IPortableDeviceValues** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pbuffer* \[ in\]
</dt> <dd>

Puntatore al buffer da deserializzare.

</dd> <dt>

*dwInputBufferLength* \[ in\]
</dt> <dd>

**DWORD** che specifica la dimensione, in byte, del buffer.

</dd> <dt>

*ppParams* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore a un'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) creata dal buffer. L'applicazione è responsabile della chiamata del **rilascio** sull'interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è riuscito.<br/>                     |
| <dl> <dt>**\_puntatore E**</dt> </dl>    | Un argomento obbligatorio del puntatore è **null**.<br/> |
| <dl> <dt>**E \_ imprevisto**</dt> </dl> | Si è verificato un errore di conversione non specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




