---
description: Il metodo CopyValuesToPropertyStore copia tutti i valori da una raccolta in un'interfaccia IPropertyStore.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'Metodo IPortableDeviceValues:: CopyValuesToPropertyStore (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d6ab6b4614c336d3e0da50c0291b2e69a260ae1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330707"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a>Metodo IPortableDeviceValues:: CopyValuesToPropertyStore

Il metodo **CopyValuesToPropertyStore** copia tutti i valori da una raccolta in un'interfaccia **IPropertyStore** .

## <a name="syntax"></a>Sintassi


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStore* \[ in\]
</dt> <dd>

Puntatore a un oggetto Store.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo non converte i valori dei \_ LPWSTR VT in VT \_ BSTR. Molte applicazioni o componenti esterni che comunicano con l'applicazione, ad esempio alcune applicazioni shell, usano l'interfaccia **IPropertyStore** . Questo metodo consente di scambiare dati in modo semplice e rapido con questi programmi.

Questo metodo è supportato in Windows Vista e nelle versioni successive di Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




