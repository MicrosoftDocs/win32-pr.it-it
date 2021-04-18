---
description: Il metodo posticipate specifica una nuova ora di presentazione per un comando accodato in precedenza.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: Metodo CDeferredCommand. posticipate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9ce19c5391541336f52dd872b44bb9f3a447c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333725"
---
# <a name="cdeferredcommandpostpone-method"></a>Metodo CDeferredCommand. posporre

Il `Postpone` metodo specifica una nuova ora di presentazione per un comando accodato in precedenza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newTime* 
</dt> <dd>

Ora della nuova presentazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l' \_ ora di VFW E \_ \_ è già stata \_ passata se *newTime* è già stato superato. In caso contrario, restituisce un **HRESULT** risultante da una chiamata a [**CCmdQueue:: Remove**](ccmdqueue-remove.md) (quando si estrae dall'elenco) o [**CCmdQueue:: Insert**](ccmdqueue-insert.md) (durante il reinserimento con l'ora di modifica).

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IDeferredCommand::P ostpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




