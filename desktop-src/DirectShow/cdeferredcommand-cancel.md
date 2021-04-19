---
description: 'Il metodo Cancel Annulla una richiesta CDeferredCommand:: Invoke precedentemente accodata.'
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: Metodo CDeferredCommand. Cancel (Ctlutil. h)
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
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333208"
---
# <a name="cdeferredcommandcancel-method"></a>CDeferredCommand. Cancel, metodo

Il `Cancel` metodo annulla una richiesta [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) precedentemente accodata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce VFW \_ E \_ già \_ annullato se **m \_ pQueue** è **null**. Restituisce un valore **HRESULT** da [**CCmdQueue:: Remove**](ccmdqueue-remove.md) se la chiamata genera un errore. Restituisce \_ OK se ha esito positivo.

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IDeferredCommand:: Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




