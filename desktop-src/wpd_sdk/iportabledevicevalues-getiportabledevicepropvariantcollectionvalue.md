---
description: Il metodo GetIPortableDevicePropVariantCollectionValue recupera un valore IPortableDevicePropVariantCollection (Type VT \_ Unknown) specificato da una chiave.
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: 'Metodo IPortableDeviceValues:: GetIPortableDevicePropVariantCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7deb73d10f2e2daa5d06d6cb4394c43778af2ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332659"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a>Metodo IPortableDeviceValues:: GetIPortableDevicePropVariantCollectionValue

Il metodo **GetIPortableDevicePropVariantCollectionValue** recupera un valore **IPORTABLEDEVICEPROPVARIANTCOLLECTION** (Type VT \_ Unknown) specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ di in\]
</dt> <dd>

Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.

</dd> <dt>

*ppValue* \[ out\]
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) recuperata. Il chiamante è responsabile della chiamata della **versione** sull'interfaccia recuperata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                                                         |
| <dl> <dt>**DISP \_ E \_ TYPEMISMATCH**</dt> </dl>                   | La proprietà specificata da *Key* non è un'interfaccia **IPortableDevicePropVariantCollection** .<br/> |
| <dl> <dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt> </dl> | La proprietà specificata dalla *chiave* non è presente nella raccolta.<br/>                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




