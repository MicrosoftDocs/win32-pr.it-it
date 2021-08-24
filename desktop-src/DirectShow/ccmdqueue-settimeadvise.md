---
description: Il metodo SetTimeAdvise imposta un evento timer con l'orologio di riferimento.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Metodo CCmdQueue.SetTimeAdvise (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.SetTimeAdvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecfa02354ad3662a6fd9060fff80b74635c63ade57539fbbd1307fa1d65e8872
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757131"
---
# <a name="ccmdqueuesettimeadvise-method"></a>Metodo CCmdQueue.SetTimeAdvise

Il `SetTimeAdvise` metodo imposta un evento timer con l'orologio di riferimento.

## <a name="syntax"></a>Sintassi


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro chiama il [**metodo IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) per configurare una notifica per la prima volta necessaria nella coda. I comandi in fase di presentazione posticimanti vengono sempre controllati. Se il grafico dei filtri è in modalità di esecuzione, vengono controllati anche i comandi posticimanti che usano il tempo di flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




