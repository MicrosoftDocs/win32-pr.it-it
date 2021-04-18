---
description: Il metodo CopyValuesFromPropertyStore copia il contenuto di un oggetto IPropertyStore nella raccolta.
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'Metodo IPortableDeviceValues:: CopyValuesFromPropertyStore (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330710"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a>Metodo IPortableDeviceValues:: CopyValuesFromPropertyStore

Il metodo **CopyValuesFromPropertyStore** copia il contenuto di un oggetto **IPropertyStore** nella raccolta.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStore* \[ in\]
</dt> <dd>

Puntatore a un oggetto **IPropertyStore** da copiare nella raccolta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo converte automaticamente tutti i valori **\_ BSTR di VT** in valori **\_ LPWSTR VT** .

Molte applicazioni o componenti esterni che comunicano con l'applicazione, ad esempio alcune applicazioni shell, usano l'interfaccia **IPropertyStore** . Questo metodo consente di scambiare dati in modo semplice e rapido con questi programmi.

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

[**IPortableDeviceValues::CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




