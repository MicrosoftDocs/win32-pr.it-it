---
description: Il metodo GetType recupera il tipo di dati degli elementi nella raccolta.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: Metodo IPortableDevicePropVariantCollection::GetType (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c29e47cd08b5c31012df92ca04e018d38f7adb7f8802ec534682289852f518b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963740"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a>Metodo IPortableDevicePropVariantCollection::GetType

Il **metodo GetType** recupera il tipo di dati degli elementi nella raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pvt* \[ Cambio\]
</dt> <dd>

Valore di enumerazione **VARTYPE** di Platform SDK che indica il tipo di dati di tutti gli elementi nella raccolta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Il metodo è riuscito.<br/>                     |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl> | Un argomento del puntatore obbligatorio era **NULL.**<br/> |



 

## <a name="remarks"></a>Commenti

Tutti gli elementi archiviati in **un oggetto IPortableDevicePropVariantCollection** sono dello stesso tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




