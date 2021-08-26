---
description: Il metodo Cancel annulla una richiesta CDeferredCommand::Invoke precedentemente accodata.
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: Metodo CDeferredCommand.Cancel (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa7e957fe97e06c6fb14fe3a9048048e351ac1baf4ff8f4dae25b3cf5863776e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043711"
---
# <a name="cdeferredcommandcancel-method"></a>Metodo CDeferredCommand.Cancel

Il `Cancel` metodo annulla una richiesta [**CDeferredCommand::Invoke precedentemente accodata.**](cdeferredcommand-invoke.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce VFW \_ E \_ ALREADY \_ CANCELLED se m **\_ pQueue** è **NULL.** Restituisce un **valore HRESULT** [**da CCmdQueue::Remove**](ccmdqueue-remove.md) se la chiamata genera un errore. Restituisce S \_ OK in caso di esito positivo.

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IDeferredCommand::Cancel.**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




