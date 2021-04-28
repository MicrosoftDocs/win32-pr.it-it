---
description: 'Metodo CTransformOutputPin.CompleteConnect: il metodo CompleteConnect completa una connessione a un altro pin.'
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: Metodo CTransformOutputPin.CompleteConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ab3d7e56473094b31c0d97d0e15c083ff61a21d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094919"
---
# <a name="ctransformoutputpincompleteconnect-method"></a>Metodo CTransformOutputPin.CompleteConnect

Il `CompleteConnect` metodo completa una connessione a un altro pin.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore all'interfaccia [**IPin dell'altro**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT.**

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseOutputPin::CompleteConnect.**](cbaseoutputpin-completeconnect.md) Chiama il metodo [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) del filtro, che restituisce S \_ OK nella classe di base. La classe derivata può eseguire l'override del **metodo CTransformFilter::CompleteConnect** per eseguire controlli aggiuntivi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




