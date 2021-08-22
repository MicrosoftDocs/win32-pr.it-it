---
description: Ottiene il tipo di modifica che si è verificata nel vettore.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: Metodo IVectorChangedEventArgs::get_CollectionChange (IVectorChangedEventArgs.h)
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
ms.openlocfilehash: 2476f9563b4e2a0cabf9babbcfc265ee4f3549416c2fdfda0dbb0f204b7ca9bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504811"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a>Metodo IVectorChangedEventArgs::get \_ CollectionChange

Ottiene il tipo di modifica che si è verificata nel vettore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Tipo: **CollectionChange \***

Valore [**dell'enumerazione CollectionChange**](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) che descrive la modifica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                 |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                       |
| Intestazione<br/>                   | <dl> <dt>IVectorChangedEventArgs.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVectorChangedEventArgs**](ivectorchangedeventargs.md)
</dt> </dl>

 

 
