---
description: Il metodo PassNotify passa un messaggio di controllo di qualità all'oggetto appropriato.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: Metodo CBaseInputPin. PassNotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36316815ae1d9fde1a18fb36029da92ae6263f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326665"
---
# <a name="cbaseinputpinpassnotify-method"></a>CBaseInputPin. PassNotify, metodo

Il `PassNotify` metodo passa un messaggio di controllo di qualità all'oggetto appropriato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*d* 
</dt> <dd>

Struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo della qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Esito positivo.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ non \_ trovato**</dt> </dl> | Impossibile trovare un oggetto per accettare il messaggio.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo se il filtro non gestisce i messaggi di controllo di qualità. Questo metodo passa il messaggio a uno degli oggetti seguenti, in ordine di preferenza:

-   Gestore di controllo della qualità esterno, se è stato chiamato il metodo [**IQualityControl::**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) SetValue.
-   Pin di output upstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> <dt>

[Gestione controllo qualità](quality-control-management.md)
</dt> </dl>

 

 




