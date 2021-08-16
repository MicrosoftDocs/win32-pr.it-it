---
description: Il metodo Seek imposta le posizioni iniziale e di arresto del flusso.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: Metodo CPullPin.Seek (Pullpin.h)
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
ms.openlocfilehash: 65ea4deddd000d1064adf8b8caf5a636eed87105856d506191d677e70978d096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953990"
---
# <a name="cpullpinseek-method"></a>Metodo CPullPin.Seek

Il `Seek` metodo imposta le posizioni iniziale e di arresto del flusso.

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

Specifica la posizione iniziale, in byte moltiplicata per 10.000.000.

</dd> <dt>

*tStop* 
</dt> <dd>

Specifica la posizione di arresto, in byte moltiplicata per 10.000.000.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il metodo ha esito positivo oppure un codice di errore in caso contrario.

## <a name="remarks"></a>Commenti

Se il thread di lavoro è in esecuzione, il metodo sospende il thread, scarica il grafico dei filtri e riprende il thread. Il thread inizia a eseguire il pull dei dati dalla nuova posizione iniziale. In caso contrario, i nuovi valori di posizione diventano effettivi ogni volta che viene avviato il thread.

Le posizioni sono relative all'inizio dell'origine originale. Moltiplicare gli offset di byte desiderati per la costante UNITS, definita nella libreria di classi di base come 10.000.000.

Quando il pin si connette per la prima volta, le posizioni di arresto e di avvio vengono posizionate per impostazione predefinita all'inizio e alla fine del flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




