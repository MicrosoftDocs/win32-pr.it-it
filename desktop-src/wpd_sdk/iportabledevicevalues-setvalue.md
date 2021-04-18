---
description: Il metodo SetValue aggiunge un nuovo valore PROPVARIANT o ne sovrascrive uno esistente.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'Metodo IPortableDeviceValues:: SetValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4c2ba6c5b6f015e5961356ff8e246605bfeddd31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326846"
---
# <a name="iportabledevicevaluessetvalue-method"></a>Metodo IPortableDeviceValues:: SetValue

Il **Metodo SetValue aggiunge** un nuovo valore **PROPVARIANT** o ne sovrascrive uno esistente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*chiave* \[ di in\]
</dt> <dd>

Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.

</dd> <dt>

*pValue* \[ in\]
</dt> <dd>

Oggetto **PROPVARIANT** che specifica il nuovo valore. L'SDK copia il valore, in modo che il chiamante possa rilasciare la variabile locale chiamando **PropVariantClear** dopo la chiamata a questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Quando VARTYPE per *pValue* è VT \_ vector o VT \_ Ui1, non è supportata l'impostazione di un buffer di dimensioni **null** o zero. Ad esempio, non sono consentiti né pValue. Campo CAUB. pElems = **null** né pValue. Campo CAUB. cElems = 0.

Questo metodo può essere utilizzato per recuperare un valore di qualsiasi tipo dalla raccolta. Tuttavia, se si conosce il tipo di valore in anticipo, utilizzare uno dei metodi **set** specializzati di questa interfaccia per evitare il sovraccarico dell'utilizzo diretto dei valori PROPVARIANT.

Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso. La memoria della chiave esistente viene rilasciata in modo appropriato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: GetValue**](iportabledevicevalues-getvalue.md)
</dt> <dt>

[**IPortableDeviceValues:: RemoveValue**](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




