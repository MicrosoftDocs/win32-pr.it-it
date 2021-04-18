---
description: Il metodo Clear libera, quindi rimuove tutti gli elementi dalla raccolta. La raccolta viene considerata vuota dopo la chiamata a questo metodo.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: 'Metodo IPortableDevicePropVariantCollection:: Clear (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fa7c2a8dddeb74b5ac666da2561bd6ee6536821a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330584"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a>Metodo IPortableDevicePropVariantCollection:: Clear

Il metodo **Clear** libera, quindi rimuove tutti gli elementi dalla raccolta. La raccolta viene considerata vuota dopo la chiamata a questo metodo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clear();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Dopo aver chiamato **Clear**, la raccolta viene considerata senza tipo, ovvero il VarType in precedenza impostato su non limita più le operazioni di **aggiunta** . Una chiamata a **Add** dopo aver chiamato **Clear** viene considerata l' **aggiunta** "First" per questa raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




