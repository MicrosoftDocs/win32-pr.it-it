---
description: Il metodo SetUnsignedIntegerValue aggiunge un nuovo valore ULONG (Type VT \_ UI4) o ne sovrascrive uno esistente.
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: 'Metodo IPortableDeviceValues:: SetUnsignedIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7dc237e5cdba120a08899035dc20f6fb6b2b63f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326850"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a>Metodo IPortableDeviceValues:: SetUnsignedIntegerValue

Il metodo **SetUnsignedIntegerValue** aggiunge un nuovo valore **ULONG** (Type VT \_ UI4) o ne sovrascrive uno esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
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

**ULONG** che specifica il nuovo valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.

## <a name="examples"></a>Esempio

Per un esempio di come usare questo metodo, vedere [**specifica delle informazioni client**](specifying-client-information.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[**Specifica delle informazioni client**](specifying-client-information.md)
</dt> </dl>

 

 




