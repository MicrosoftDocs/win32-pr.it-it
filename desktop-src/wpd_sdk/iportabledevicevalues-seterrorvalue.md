---
description: Il metodo SetErrorValue aggiunge un nuovo valore HRESULT (tipo \_ errore VT) o sovrascrive uno esistente.
ms.assetid: 87369791-42bd-4523-b15a-acf0ea1e5af8
title: 'Metodo IPortableDeviceValues:: SetErrorValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetErrorValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 19c7ca57d325e31fd9cd8e0bf5130dc594b0b8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330434"
---
# <a name="iportabledevicevaluesseterrorvalue-method"></a>Metodo IPortableDeviceValues:: SetErrorValue

Il metodo **SetErrorValue** aggiunge un nuovo valore **HRESULT** (tipo \_ errore VT) o sovrascrive uno esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetErrorValue(
  [in]       REFPROPERTYKEY key,
  [in] const HRESULT        Value
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

**HRESULT** che contiene il nuovo valore.

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

[**IPortableDeviceValues::GetErrorValue**](iportabledevicevalues-geterrorvalue.md)
</dt> </dl>

 

 




