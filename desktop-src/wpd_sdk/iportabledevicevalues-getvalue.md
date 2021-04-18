---
description: Il metodo GetValue recupera un valore PROPVARIANT specificato da una chiave.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: 'Metodo IPortableDeviceValues:: GetValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6ab5ec24e67d5259eec86c6a33d32766a5426b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325811"
---
# <a name="iportabledevicevaluesgetvalue-method"></a>Metodo IPortableDeviceValues:: GetValue

Il metodo **GetValue** recupera un valore **PROPVARIANT** specificato da una chiave.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ di in\]
</dt> <dd>

Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Puntatore al valore **PROPVARIANT** recuperato. Il chiamante deve rilasciare la memoria chiamando **PropVariantClear** al termine di tale operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                                            | Descrizione                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                                   | Il metodo è riuscito.<br/>                                     |
| <dl> <dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt> </dl> | La proprietà specificata dalla *chiave* non è presente nella raccolta.<br/> |



 

## <a name="remarks"></a>Commenti

Quando VARTYPE for *pValue* è VT \_ vector o VT \_ Ui1, il recupero di un buffer di dimensioni **null** o zero non è supportato. Ad esempio, non sono consentiti né pValue. Campo CAUB. pElems = **null** né pValue. Campo CAUB. cElems = 0.

Questo metodo può essere utilizzato per recuperare un valore di qualsiasi tipo dalla raccolta. Tuttavia, se si conosce il tipo di valore in anticipo, utilizzare uno dei metodi di recupero specializzati di questa interfaccia per evitare il sovraccarico dell'utilizzo diretto dei valori PROPVARIANT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> <dt>

[**IPortableDeviceValues:: SetValue**](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




