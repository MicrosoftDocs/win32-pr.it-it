---
description: Il metodo CopyValuesToPropertyStore copia tutti i valori da una raccolta in un'interfaccia IPropertyStore.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: Metodo IPortableDeviceValues::CopyValuesToPropertyStore (PortableDeviceTypes.h)
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
ms.openlocfilehash: 2d134cb61831426451b1c6068bde5ca787b027fbe5b153587b45d9693ef739c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697248"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a>Metodo IPortableDeviceValues::CopyValuesToPropertyStore

Il **metodo CopyValuesToPropertyStore** copia tutti i valori da una raccolta in **un'interfaccia IPropertyStore.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStore* \[ Pollici\]
</dt> <dd>

Puntatore a un oggetto archivio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo non converte i valori di \_ VT LPWSTR in VT \_ BSTR. Molte applicazioni o componenti esterni che comunicano con l'applicazione, ad esempio alcune applicazioni shell, usano **l'interfaccia IPropertyStore.** Questo metodo offre un modo semplice e rapido per scambiare dati con questi programmi.

Questo metodo è supportato in Windows Vista e versioni successive di Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




