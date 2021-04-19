---
description: Il metodo CreateInstance chiama la funzione di creazione di oggetti per la classe.
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: Metodo CFactoryTemplate. CreateInstance (ComBase. h)
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
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329831"
---
# <a name="cfactorytemplatecreateinstance-method"></a>Metodo CFactoryTemplate. CreateInstance

Il `CreateInstance` metodo chiama la funzione di creazione di oggetti per la classe.

## <a name="syntax"></a>Sintassi


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pUnk* 
</dt> <dd>

Puntatore all'interfaccia **IUnknown** di aggregazione.

</dd> <dt>

*PHR* 
</dt> <dd>

Puntatore a una variabile che riceve un valore **HRESULT** che indica l'esito positivo o negativo del metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un'istanza dell'oggetto classe.

## <a name="remarks"></a>Commenti

Il metodo **IClassFactory:: CreateInstance** chiama questo metodo della classe. Questo metodo chiama la funzione a cui fa riferimento la variabile membro [**CFactoryTemplate:: m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>ComBase. h (Includi Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CFactoryTemplate**](cfactorytemplate.md)
</dt> </dl>

 

 




