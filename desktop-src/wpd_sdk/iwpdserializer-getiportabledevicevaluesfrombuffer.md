---
description: Il metodo GetIPortableDeviceValuesFromBuffer deserializza una matrice di byte in un'interfaccia IPortableDeviceValues.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: Metodo IWpdSerializer::GetIPortableDeviceValuesFromBuffer (PortableDeviceTypes.h)
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
ms.openlocfilehash: ac33bf0cfb04363d40e4efeff13db1cb2504ce2dcb7ece4d9b10ac3d08dff83f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054961"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a>Metodo IWpdSerializer::GetIPortableDeviceValuesFromBuffer

Il **metodo GetIPortableDeviceValuesFromBuffer** deserializza una matrice di byte in **un'interfaccia IPortableDeviceValues.**

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

*pBuffer* \[ Pollici\]
</dt> <dd>

Puntatore al buffer da deserializzare.

</dd> <dt>

*dwInputBufferLength* \[ Pollici\]
</dt> <dd>

**Valore DWORD** che specifica le dimensioni del buffer, in byte.

</dd> <dt>

*ppParams* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore a [**un'interfaccia IPortableDeviceValues**](iportabledevicevalues.md) creata dal buffer. L'applicazione è responsabile della chiamata **di Release** sull'interfaccia .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è riuscito.<br/>                     |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>    | Un argomento del puntatore obbligatorio era **NULL.**<br/> |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl> | Si è verificato un errore di conversione non specificato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




