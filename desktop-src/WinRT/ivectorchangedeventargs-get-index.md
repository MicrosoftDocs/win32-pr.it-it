---
description: Ottiene la posizione nel vettore in cui si è verificata la modifica.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: Metodo IVectorChangedEventArgs::get_Index (IVectorChangedEventArgs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 72df7f0d46e1e3073262c43064daf58b1fefbf43af913bb7f1b912ed22e67a7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560647"
---
# <a name="ivectorchangedeventargsget_index-method"></a>Metodo IVectorChangedEventArgs::get \_ Index

Ottiene la posizione nel vettore in cui si è verificata la modifica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

Tipo: **senza \* segno**

Posizione in base zero nel vettore in cui si è verificata la modifica, se applicabile.

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

 

 




