---
description: 'Metodo CTransformInputPin.CompleteConnect: il metodo CompleteConnect completa una connessione a un altro pin.'
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: Metodo CTransformInputPin.CompleteConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8b92ae9830bc7083f5e7a091b1ffbed273d9b62068ca47c5ad85682347706653
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812821"
---
# <a name="ctransforminputpincompleteconnect-method"></a>Metodo CTransformInputPin.CompleteConnect

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

Questo metodo esegue l'override [**del metodo CBasePin::CompleteConnect.**](cbasepin-completeconnect.md) Chiama il metodo [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) del filtro, che restituisce S \_ OK nella classe di base. La classe derivata può eseguire l'override del **metodo CTransformFilter::CompleteConnect** per eseguire controlli aggiuntivi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




