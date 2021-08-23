---
description: Il metodo Postpone specifica una nuova ora di presentazione per un comando accodato in precedenza.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: Metodo CDeferredCommand.Postpone (Ctlutil.h)
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
ms.openlocfilehash: 079b9f1a852ff0b9eb6e1c38cea6e24e3ee00107ac46ca15e738e1ef9e0eb8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074365"
---
# <a name="cdeferredcommandpostpone-method"></a>Metodo CDeferredCommand.Postpone

Il `Postpone` metodo specifica una nuova ora di presentazione per un comando precedentemente accodato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*newtime* 
</dt> <dd>

Nuova ora di presentazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce VFW \_ E TIME ALREADY PASSED se \_ \_ \_ *newtime* è già passato. In caso contrario, restituisce un **valore HRESULT** risultante da una chiamata a [**CCmdQueue::Remove**](ccmdqueue-remove.md) (durante l'estrazione dall'elenco) o [**CCmdQueue::Insert**](ccmdqueue-insert.md) (durante la reinserzione con l'ora modificata).

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IDeferredCommand::P ostpone.**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




