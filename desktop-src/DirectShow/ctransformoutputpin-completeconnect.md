---
description: Il metodo CompleteConnect completa una connessione a un altro pin.
ms.assetid: 14bc48bc-ddfb-4491-8d5b-9e5ac601ba04
title: Metodo CTransformOutputPin. CompleteConnect (Transfrm. h)
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
ms.openlocfilehash: 8d0c9c9fc7096191d7cdedffa21e2639fa0750ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333304"
---
# <a name="ctransformoutputpincompleteconnect-method"></a>CTransformOutputPin. CompleteConnect, metodo

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

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o un altro valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBaseOutputPin:: CompleteConnect**](cbaseoutputpin-completeconnect.md) . Chiama il metodo [**CTransformFilter:: CompleteConnect**](ctransformfilter-completeconnect.md) del filtro, che restituisce \_ OK nella classe di base. La classe derivata può eseguire l'override del metodo **CTransformFilter:: CompleteConnect** per eseguire ulteriori controlli.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




