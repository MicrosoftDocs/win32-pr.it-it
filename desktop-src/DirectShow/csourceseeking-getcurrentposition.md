---
description: Il metodo GetCurrentPosition recupera la posizione corrente, relativa alla durata totale del flusso. Non implementato.
ms.assetid: 386f41e4-a673-4c67-a28f-e155810fbb5a
title: Metodo CSourceSeeking.GetCurrentPosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff4069c8b1a83ade6897fedf87c16b89b1c63d3c1cef18d21a3bdbd594a3b2cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084058"
---
# <a name="csourceseekinggetcurrentposition-method"></a>Metodo CSourceSeeking.GetCurrentPosition

Il `GetCurrentPosition` metodo recupera la posizione corrente, rispetto alla durata totale del flusso. Non implementato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCurrentPosition(
   LONGLONG *pCurrent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pCurrent* 
</dt> <dd>

Puntatore a una variabile che riceve la posizione corrente, in unità del formato di ora corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ NOTIMPL.

## <a name="remarks"></a>Commenti

I filtri di origine in genere non supportano questo metodo. I filtri del renderer segnalano invece la posizione corrente tramite la [**classe CRendererPosPassThru.**](crendererpospassthru.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




