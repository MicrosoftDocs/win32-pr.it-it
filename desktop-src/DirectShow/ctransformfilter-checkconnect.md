---
description: Il metodo CheckConnect determina se una connessione pin è adatta.
ms.assetid: 4bec4b19-3f7c-43d8-9a45-2eb2cc15a0d4
title: Metodo CTransformFilter. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0d41c50323bae7cb4eaca52a87d8c1b936237ccd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325732"
---
# <a name="ctransformfiltercheckconnect-method"></a>CTransformFilter. CheckConnect, metodo

Il `CheckConnect` metodo determina se una connessione pin è adatta.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CheckConnect(
   PIN_DIRECTION dir,
   IPin          *pPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dir* 
</dt> <dd>

Membro del tipo enumerato di [**\_ direzione del pin**](/windows/win32/api/strmif/ne-strmif-pin_direction) , che specifica quale pin del filtro sta effettuando la connessione.

</dd> <dt>

*pPin* 
</dt> <dd>

Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin in questo tentativo di connessione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

I metodi [**CTransformInputPin:: CheckConnect**](ctransforminputpin-checkconnect.md) e [**CTransformOutputPin:: CheckConnect**](ctransformoutputpin-checkconnect.md) chiamano questo metodo durante il processo di connessione del PIN. Questo metodo non esegue alcuna operazione nella classe di base. La classe derivata può eseguire l'override. La classe derivata può ad esempio eseguire una query sull'altro pin per una particolare interfaccia.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transfrm. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




