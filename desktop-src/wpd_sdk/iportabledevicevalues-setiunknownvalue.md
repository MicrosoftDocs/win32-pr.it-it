---
description: Il metodo SetIUnknownValue aggiunge un nuovo valore IUnknown (Type VT \_ Unknown) o ne sovrascrive uno esistente.
ms.assetid: 292adf45-439c-4aae-9b17-e4d9ed701eda
title: 'Metodo IPortableDeviceValues:: SetIUnknownValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2c3a27fe5ea89359884d70162000b5164b7c1aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326861"
---
# <a name="iportabledevicevaluessetiunknownvalue-method"></a>Metodo IPortableDeviceValues:: SetIUnknownValue

Il metodo **SetIUnknownValue** aggiunge un nuovo valore **IUnknown** (Type VT \_ Unknown) o ne sovrascrive uno esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetIUnknownValue(
  [in] REFPROPERTYKEY key,
  [in] IUnknown       *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ di in\]
</dt> <dd>

Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.

</dd> <dt>

*pValue* \[ in\]
</dt> <dd>

Puntatore a un'interfaccia **IUnknown** che specifica il nuovo valore. L'SDK copia un riferimento all'interfaccia inviata e chiama **AddRef** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso. La memoria della chiave esistente viene rilasciata in modo appropriato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetIUnknownValue**](iportabledevicevalues-getiunknownvalue.md)
</dt> </dl>

 

 




