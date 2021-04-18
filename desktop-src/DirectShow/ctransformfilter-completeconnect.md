---
description: Il metodo CompleteConnect completa una connessione pin.
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Metodo CTransformFilter. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 630950cf9b05c08412394bf9270f2369b3f3b94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329150"
---
# <a name="ctransformfiltercompleteconnect-method"></a>CTransformFilter. CompleteConnect, metodo

Il `CompleteConnect` metodo completa una connessione pin.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*direction* 
</dt> <dd>

Membro del tipo enumerato di [**\_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) , che specifica quale pin del filtro sta effettuando la connessione.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin in questo tentativo di connessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

I metodi [**CTransformInputPin:: CompleteConnect**](ctransforminputpin-completeconnect.md) e [**CTransformOutputPin:: CompleteConnect**](ctransformoutputpin-completeconnect.md) chiamano questo metodo durante il processo di connessione del PIN. Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




