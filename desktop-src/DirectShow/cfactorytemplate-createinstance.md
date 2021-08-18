---
description: Il metodo CreateInstance chiama la funzione di creazione dell'oggetto per la classe .
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: Metodo CFactoryTemplate.CreateInstance (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 816d690a7e57df83b3f521f4591c3334269d0fccebbaeac480e7aacb46253273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074205"
---
# <a name="cfactorytemplatecreateinstance-method"></a>Metodo CFactoryTemplate.CreateInstance

Il `CreateInstance` metodo chiama la funzione di creazione dell'oggetto per la classe .

## <a name="syntax"></a>Sintassi


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Punk* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown aggregata.**

</dd> <dt>

*Phr* 
</dt> <dd>

Puntatore a una variabile che riceve un **valore HRESULT** che indica l'esito positivo o negativo del metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un'istanza dell'oggetto classe .

## <a name="remarks"></a>Commenti

Il **metodo IClassFactory::CreateInstance** chiama questo metodo della classe. Questo metodo chiama la funzione a cui punta [**la variabile membro CFactoryTemplate::m \_ lpfnNew.**](cfactorytemplate-m-lpfnnew.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




