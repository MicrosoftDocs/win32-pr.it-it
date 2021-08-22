---
description: Il metodo PassNotify passa un messaggio di controllo qualità all'oggetto appropriato.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: Metodo CBaseInputPin.PassNotify (Amfilter.h)
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
ms.openlocfilehash: 760ec066a9d4876dd6ef754783c41ae12765db10c1595d08aef0a73258de087f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016999"
---
# <a name="cbaseinputpinpassnotify-method"></a>Metodo CBaseInputPin.PassNotify

Il `PassNotify` metodo passa un messaggio di controllo qualità all'oggetto appropriato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*D* 
</dt> <dd>

[**Struttura**](/windows/win32/api/strmif/ns-strmif-quality) Quality che contiene il messaggio di controllo qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** I valori possibili includono quelli elencati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Operazione completata.<br/>                                        |
| <dl> <dt>**VFW \_ E \_ NON \_ TROVATO**</dt> </dl> | Impossibile trovare un oggetto per accettare il messaggio.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo se il filtro non gestisce i messaggi di controllo qualità. Questo metodo passa il messaggio a uno degli oggetti seguenti, in ordine di preferenza:

-   Un gestore del controllo di qualità esterno, se è stato chiamato il metodo [**IQualityControl::SetSink.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)
-   Pin di output upstream.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> <dt>

[Gestione del controllo di qualità](quality-control-management.md)
</dt> </dl>

 

 




