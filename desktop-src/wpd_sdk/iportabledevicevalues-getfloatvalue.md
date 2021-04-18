---
description: Il metodo GetFloatValue recupera un valore FLOAT (tipo VT \_ R4) specificato da una chiave.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'Metodo IPortableDeviceValues:: GetFloatValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327685"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a>Metodo IPortableDeviceValues:: GetFloatValue

Il metodo **GetFloatValue** recupera un valore **float** (tipo VT \_ R4) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ di in\]
</dt> <dd>

Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Puntatore al valore **float** recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                             | Descrizione                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>    | La proprietà specificata da *Key* non è di tipo **float** .<br/>  |
| <dl> <dt>**\_ID Prop \_ non \_ supportato**</dt> </dl> | La proprietà specificata dalla *chiave* non è presente nella raccolta.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetFloatValue**](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




