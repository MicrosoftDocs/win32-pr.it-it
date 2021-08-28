---
description: Il metodo GetResult recupera l'elenco di argomenti risultante, se presente.
ms.assetid: a2a8b17c-3dcf-4f59-89c3-f42070d2a8eb
title: Metodo CDeferredCommand.GetResult (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2176d6787bd520517cccbf484bdf6642921d499aaeb97c2917d64fa148323b66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076421"
---
# <a name="cdeferredcommandgetresult-method"></a>Metodo CDeferredCommand.GetResult

Il `GetResult` metodo recupera l'elenco di argomenti risultante, se presente.

## <a name="syntax"></a>Sintassi


```C++
VARIANT* GetResult();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore a **un variant** contenente l'elenco di argomenti del metodo, se esistente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




