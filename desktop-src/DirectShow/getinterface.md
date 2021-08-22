---
description: La funzione GetInterface recupera un puntatore a interfaccia.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: Funzione GetInterface (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 289c6e56d4b5387fe9224e476c69865107102141b687825cdfd9a717f482632c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537031"
---
# <a name="getinterface-function"></a>Funzione GetInterface

La `GetInterface` funzione recupera un puntatore a interfaccia.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Punk* 
</dt> <dd>

Puntatore **all'interfaccia IUnknown.**

</dd> <dt>

*Ppv* 
</dt> <dd>

Indirizzo di un puntatore all'interfaccia recuperata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro esegue un incremento thread-safe del conteggio dei riferimenti. Per recuperare l'interfaccia e aggiungere un riferimento, chiamare questa funzione dall'implementazione di override del metodo **INonDelegatingUnknown::NonDelegatingQueryInterface.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Combase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni helper COM**](com-helper-functions.md)
</dt> <dt>

[**INonDelegatingUnknown**](inondelegatingunknown.md)
</dt> </dl>

 

 




