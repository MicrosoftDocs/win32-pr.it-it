---
description: 'Metodo IPortableDeviceValues::Clear: il metodo Clear elimina tutti gli elementi dalla raccolta.'
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
title: Metodo IPortableDeviceValues::Clear (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9303fe64ffafe383de8fc8a9bb9e160ab0401313d8c8e9972e609db41f01ba46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117652715"
---
# <a name="iportabledevicevaluesclear-method"></a>Metodo IPortableDeviceValues::Clear

Il **metodo Clear** elimina tutti gli elementi dalla raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clear();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo libera la memoria per tutti gli elementi allocati dinamicamente nella raccolta . Per le interfacce, chiama **Release.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> </dl>

 

 




