---
description: 'Metodo IPortableDeviceValues::GetCount: il metodo GetCount recupera il numero di elementi nella raccolta.'
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: Metodo IPortableDeviceValues::GetCount (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f53bd254699360de760a9ff60d385020b9c48213d19ce40d53b5b3ebc5ce56e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194112"
---
# <a name="iportabledevicevaluesgetcount-method"></a>Metodo IPortableDeviceValues::GetCount

Il **metodo GetCount** recupera il numero di elementi nella raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pcelt* \[ Pollici\]
</dt> <dd>

Puntatore a **un valore DWORD** che contiene il numero di elementi nella raccolta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> </dl>

 

 




