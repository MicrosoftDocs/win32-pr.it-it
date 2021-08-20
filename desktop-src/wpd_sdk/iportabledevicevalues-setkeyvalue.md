---
description: Il metodo SetKeyValue aggiunge un nuovo valore REFPROPERTYKEY (tipo VT \_ UNKNOWN) o ne sovrascrive uno esistente.
ms.assetid: 344c52ec-91b1-43f9-b16a-28c24971d805
title: Metodo IPortableDeviceValues::SetKeyValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 850c9752d83e95aa6d602aec5a8d44fa43deb83728d0bc0c3130c30e04151a04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584301"
---
# <a name="iportabledevicevaluessetkeyvalue-method"></a>Metodo IPortableDeviceValues::SetKeyValue

Il **metodo SetKeyValue** aggiunge un nuovo **valore REFPROPERTYKEY** (tipo VT \_ UNKNOWN) o ne sovrascrive uno esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetKeyValue(
  [in] REFPROPERTYKEY key,
  [in] REFPROPERTYKEY Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ Pollici\]
</dt> <dd>

**RefPROPERTYKEY che** specifica l'elemento da creare o sovrascrivere.

</dd> <dt>

*Valore* \[ Pollici\]
</dt> <dd>

**RefPROPERTYKEY** che specifica il nuovo valore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Se un valore esistente ha la stessa chiave specificata dal parametro *key,* sovrascrive il valore esistente senza alcun avviso. La memoria della chiave esistente viene rilasciata in modo appropriato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Aggiunta di una risorsa a un oggetto](adding-a-resource-to-an-object.md)
</dt> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetKeyValue**](iportabledevicevalues-getkeyvalue.md)
</dt> </dl>

 

 




