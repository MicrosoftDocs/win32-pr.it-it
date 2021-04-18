---
description: Il metodo SetSignedLargeIntegerValue aggiunge un nuovo valore LONGLONG (Type VT \_ I8) o ne sovrascrive uno esistente.
ms.assetid: 604b48ed-3e3f-4a06-91dd-7ece9f146824
title: 'Metodo IPortableDeviceValues:: SetSignedLargeIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f8c207a88e17c9a1ddf45d77e9da8b62a8396e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326856"
---
# <a name="iportabledevicevaluessetsignedlargeintegervalue-method"></a>Metodo IPortableDeviceValues:: SetSignedLargeIntegerValue

Il metodo **SetSignedLargeIntegerValue** aggiunge un nuovo valore **LONGLONG** (Type VT \_ I8) o ne sovrascrive uno esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONGLONG       Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ di in\]
</dt> <dd>

Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.

</dd> <dt>

*Valore* \[ di in\]
</dt> <dd>

Oggetto **LONGLONG** che specifica il nuovo valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetSignedLargeIntegerValue**](iportabledevicevalues-getsignedlargeintegervalue.md)
</dt> </dl>

 

 




