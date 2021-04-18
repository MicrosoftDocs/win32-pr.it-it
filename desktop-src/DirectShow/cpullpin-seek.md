---
description: Il metodo Seek imposta le posizioni di inizio e di fine del flusso.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: Metodo CPullPin. Seek (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f1a82ec549b5ceb888acc194a7abc2cd3eace47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331157"
---
# <a name="cpullpinseek-method"></a>Metodo CPullPin. Seek

Il `Seek` metodo imposta le posizioni di inizio e di fine del flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tStart* 
</dt> <dd>

Specifica la posizione iniziale, in byte, moltiplicata per 10 milioni.

</dd> <dt>

*tStop* 
</dt> <dd>

Specifica la posizione di arresto, in byte moltiplicata per 10 milioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se il metodo ha esito positivo o un codice di errore.

## <a name="remarks"></a>Commenti

Se il thread di lavoro è in esecuzione, il metodo sospende il thread, svuota il grafo del filtro e riprende il thread. Il thread inizia a estrarre i dati dalla nuova posizione iniziale. In caso contrario, i nuovi valori di posizione diventano effettivi ogni volta che il thread viene avviato.

Le posizioni sono relative all'inizio dell'origine originale. Moltiplicare gli offset di byte desiderati in base alle unità costanti, definite nella libreria di classi di base come 10 milioni.

Quando il pin si connette per la prima volta, le posizioni di arresto e avvio vengono assegnate per impostazione predefinita all'inizio e alla fine del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




