---
description: 'Metodo CTransformFilter.CompleteConnect: il metodo CompleteConnect completa una connessione pin.'
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Metodo CTransformFilter.CompleteConnect (Transfrm.h)
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
ms.openlocfilehash: d2251ba45c7a39ec9bf205fdd6643e02392e40e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095169"
---
# <a name="ctransformfiltercompleteconnect-method"></a>Metodo CTransformFilter.CompleteConnect

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

Membro del [**tipo enumerato PIN \_ DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) che specifica quale pin nel filtro sta effettuando la connessione.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin in questo tentativo di connessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

I [**metodi CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) e [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) chiamano questo metodo durante il processo di connessione del pin. Questo metodo non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




