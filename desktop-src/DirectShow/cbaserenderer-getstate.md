---
description: Il metodo GetState recupera lo stato dei filtri (in esecuzione, arrestato o sospeso).
ms.assetid: 5d35824c-2509-499a-bbb1-1fb916b51808
title: Metodo CBaseRenderer. GetState (Renbase. h)
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
ms.openlocfilehash: 451078a6167ff7ca89ad4153c416826af8ac6d05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325928"
---
# <a name="cbaserenderergetstate-method"></a>Metodo CBaseRenderer. GetState

Il `GetState` metodo recupera lo stato dei filtri (in esecuzione, arrestato o sospeso).

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

Intervallo di timeout, in millisecondi.

</dd> <dt>

*State* 
</dt> <dd>

Puntatore a una variabile che riceve un membro del tipo enumerato [**\_ dello stato del filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , che indica lo stato del filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                                | Descrizione                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Esito positivo.<br/>                                            |
| <dl> <dt>**\_ \_ stato \_ INTERmedio di VFW**</dt> </dl> | Il filtro sta passando allo stato indicato.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>                  | Argomento puntatore **null** .<br/>                          |



 

## <a name="remarks"></a>Commenti

Questo metodo esegue l'override del metodo [**CBaseFilter:: GetState**](cbasefilter-getstate.md) . Quando il renderer viene sospeso, non viene completata la transizione di stato fino a quando non viene ricevuto un campione per il rendering. Se il timeout scade prima del completamento della transizione di stato, il metodo restituisce l' \_ \_ intermediario dello stato VFW S \_ .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




