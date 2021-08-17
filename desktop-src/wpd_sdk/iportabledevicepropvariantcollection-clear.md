---
description: Il metodo Clear libera e quindi rimuove tutti gli elementi dalla raccolta. La raccolta viene considerata vuota dopo la chiamata a questo metodo.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: Metodo IPortableDevicePropVariantCollection::Clear (PortableDeviceTypes.h)
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
ms.openlocfilehash: 0cec3f12757fe43c408488204de8b0dd95d5e95c75d8315ea758e4311ff5e9bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194139"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a>Metodo IPortableDevicePropVariantCollection::Clear

Il **metodo Clear** libera e quindi rimuove tutti gli elementi dalla raccolta. La raccolta viene considerata vuota dopo la chiamata a questo metodo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Clear();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Dopo la **chiamata a Clear,** la raccolta viene considerata senza tipi, vale a dire che VARTYPE su cui è stata impostata in precedenza non limita più **le operazioni Add.** Una chiamata ad **Add** dopo **aver chiamato Clear** viene considerata la "prima" **Add** per questa raccolta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




