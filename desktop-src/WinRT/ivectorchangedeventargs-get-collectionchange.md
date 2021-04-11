---
description: Ottiene il tipo di modifica che si è verificata nel vettore.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'Metodo IVectorChangedEventArgs:: get_CollectionChange (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226098"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a>Metodo IVectorChangedEventArgs:: Get \_ CollectionChange

Ottiene il tipo di modifica che si è verificata nel vettore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out, retval\]
</dt> <dd>

Tipo: **CollectionChange \** _

Valore dell'enumerazione [_ *CollectionChange* *](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) che descrive la modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                 |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                       |
| Intestazione<br/>                   | <dl> <dt>IVectorChangedEventArgs. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVectorChangedEventArgs**](ivectorchangedeventargs.md)
</dt> </dl>

 

 
