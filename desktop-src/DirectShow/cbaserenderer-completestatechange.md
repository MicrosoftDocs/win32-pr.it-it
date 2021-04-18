---
description: Il metodo CompleteStateChange determina se una transizione allo stato di sospensione è stata completata.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Metodo CBaseRenderer. CompleteStateChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2465aeed3347f6ebc592dbe01bc3580a30983e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329390"
---
# <a name="cbaserenderercompletestatechange-method"></a>CBaseRenderer. CompleteStateChange, metodo

Il `CompleteStateChange` metodo determina se una transizione allo stato di sospensione è stata completata.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Stato precedente* 
</dt> <dd>

Stato precedente alla transizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se la transizione è completa. In caso contrario, restituisce \_ false.

## <a name="remarks"></a>Commenti

Il metodo [**CBaseRenderer::P ause**](cbaserenderer-pause.md) chiama questo metodo per aggiornare lo stato della transizione di stato. In generale, la transizione a Paused non viene completata fino a quando il filtro non riceve un campione. In alcune situazioni, tuttavia, la transizione viene completata immediatamente: ad esempio, se il filtro è scollegato o se è stata raggiunta la fine del flusso. Questo metodo controlla i vari criteri e quindi chiama il metodo [**CBaseRenderer:: Ready**](cbaserenderer-ready.md) o il metodo [**CBaseRenderer:: nobattistraday**](cbaserenderer-notready.md) per aggiornare lo stato della transizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




