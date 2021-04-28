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
ms.openlocfilehash: b7a2f1f71f81296f56be779a4c6eea746ebd0963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086239"
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

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



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

 

 




