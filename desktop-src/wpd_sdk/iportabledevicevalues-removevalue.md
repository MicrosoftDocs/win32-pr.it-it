---
description: Il Metodo RemoveValue rimuove un elemento dalla raccolta.
ms.assetid: 864c23ee-5a4e-4e06-add0-f6aef5562430
title: 'Metodo IPortableDeviceValues:: RemoveValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.RemoveValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f65160cc2798524d88471382c855f65dea2e6033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325810"
---
# <a name="iportabledevicevaluesremovevalue-method"></a>Metodo IPortableDeviceValues:: RemoveValue

Il metodo **RemoveValue** rimuove un elemento dalla raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RemoveValue(
  [in] REFPROPERTYKEY key
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ di in\]
</dt> <dd>

Oggetto **REFPROPERTYKEY** che specifica l'elemento da rimuovere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: GetValue**](iportabledevicevalues-getvalue.md)
</dt> <dt>

[**IPortableDeviceValues:: SetValue**](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




