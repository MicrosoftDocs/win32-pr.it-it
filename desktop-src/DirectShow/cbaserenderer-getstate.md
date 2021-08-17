---
description: Il metodo GetState recupera lo stato dei filtri (in esecuzione, arrestato o sospeso).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Metodo CBaseRenderer.GetState (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 532a41bb9e39f844b3a485fc236ae8d03450d45cdcb45d92c8cfa94d9af4a4bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403410"
---
# <a name="cbaserenderergetstate-method"></a>Metodo CBaseRenderer.GetState

Il metodo recupera lo stato dei filtri `GetState` (in esecuzione, arrestato o sospeso).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetState(
   DWORD        dwMilliSecsTimeout,
   FILTER_STATE *State
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwMilliSecsTimeout* 
</dt> <dd>

Intervallo di timeout, espresso in millisecondi.

</dd> <dt>

*State* 
</dt> <dd>

Puntatore a una variabile che riceve un membro del tipo enumerato [**FILTER \_ STATE,**](/windows/win32/api/strmif/ne-strmif-filter_state) che indica lo stato del filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Operazione completata.<br/>                                            |
| <dl> <dt>**VFW \_ S \_ STATE \_ INTERMEDIATE**</dt> </dl> | Il filtro sta per passare allo stato indicato.<br/> |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>                  | Argomento del puntatore **NULL.**<br/>                          |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override [**del metodo CBaseFilter::GetState.**](cbasefilter-getstate.md) Quando il renderer viene sospeso, non completa la transizione di stato fino a quando non riceve un campione di cui eseguire il rendering. Se il timeout scade prima del completamento della transizione dello stato, il metodo restituisce VFW \_ S \_ STATE \_ INTERMEDIATE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




