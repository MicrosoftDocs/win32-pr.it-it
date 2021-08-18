---
description: Il metodo GetBufferValue recupera un valore di matrice di byte (tipo VT \_ VECTOR \| VT \_ UI1) specificato da una chiave.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: Metodo IPortableDeviceValues::GetBufferValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c5d209d7ee13f55ab2236166851e2e24143b9cdeb01e947f0463491eb7446eb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963700"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a>Metodo IPortableDeviceValues::GetBufferValue

Il **metodo GetBufferValue** recupera un valore di **matrice di byte** (tipo VT VECTOR \_ \| VT \_ UI1) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBufferValue(
  [in]  REFPROPERTYKEY key,
  [out] BYTE           **ppValue,
  [out] DWORD          *pcbValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ Pollici\]
</dt> <dd>

Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.

</dd> <dt>

*ppValue* \[ Cambio\]
</dt> <dd>

Puntatore al valore **BYTE \* *_ recuperato. Il chiamante è responsabile della liberazione della memoria chiamando _* CoTaskMemFree**.

</dd> <dt>

*pcbValue* \[ Cambio\]
</dt> <dd>

Puntatore alla dimensione di *ppValue,* in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *key* non è di **tipo BYTE.** \*<br/> |
| <dl> <dt>**HRESULT \_ DA \_ WIN32(ERRORE \_ NON \_ TROVATO)**</dt> </dl> | La proprietà specificata da *key* non è presente nella raccolta.<br/> |



 

## <a name="remarks"></a>Commenti

Il recupero di un buffer **NULL** o di dimensioni zero non è supportato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetBufferValue**](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




