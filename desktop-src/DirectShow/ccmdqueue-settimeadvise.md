---
description: Il metodo SetTimeAdvise imposta un evento timer con l'orologio di riferimento.
ms.assetid: d0ab5c21-3585-413b-ba75-8591ed4527e4
title: Metodo CCmdQueue. SetTimeAdvise (Winutil. h)
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
ms.openlocfilehash: 24313b908f1271f270e28b08058c415ed82396fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324025"
---
# <a name="ccmdqueuesettimeadvise-method"></a>CCmdQueue. SetTimeAdvise, metodo

Il `SetTimeAdvise` metodo configura un evento timer con l'orologio di riferimento.

## <a name="syntax"></a>Sintassi


```C++
void SetTimeAdvise();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione membro chiama il metodo [**IReferenceClock:: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) per impostare una notifica per la prima ora necessaria nella coda. I comandi per la fase di presentazione posticipati vengono sempre controllati. Se il grafico del filtro è in modalità di esecuzione, vengono controllati anche i comandi posticipati che usano il tempo di flusso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CCmdQueue**](ccmdqueue.md)
</dt> </dl>

 

 




