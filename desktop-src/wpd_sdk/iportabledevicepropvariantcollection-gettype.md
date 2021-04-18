---
description: Il metodo GetType Recupera il tipo di dati degli elementi nella raccolta.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'Metodo IPortableDevicePropVariantCollection:: GetType (PortableDeviceTypes. h)'
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
ms.openlocfilehash: de5ea5b1eeaa9cf494c24e13b8b9b36f7490b84d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325943"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a>Metodo IPortableDevicePropVariantCollection:: GetType

Il metodo **GetType** Recupera il tipo di dati degli elementi nella raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pvt* \[ out\]
</dt> <dd>

Valore di enumerazione **VarType** di Platform SDK che indica il tipo di dati di tutti gli elementi nella raccolta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Il metodo è riuscito.<br/>                     |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Un argomento obbligatorio del puntatore è **null**.<br/> |



 

## <a name="remarks"></a>Commenti

Tutti gli elementi archiviati in un **IPortableDevicePropVariantCollection** sono dello stesso tipo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




