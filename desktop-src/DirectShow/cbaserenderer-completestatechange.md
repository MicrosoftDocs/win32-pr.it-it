---
description: Il metodo CompleteStateChange determina se una transizione allo stato sospeso è stata completata.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Metodo CBaseRenderer.CompleteStateChange (Renbase.h)
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
ms.openlocfilehash: 260cd5692e10fb6e6adaa3ed715944eb773064afaea68f5e0909fa08f45adfb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872361"
---
# <a name="cbaserenderercompletestatechange-method"></a>Metodo CBaseRenderer.CompleteStateChange

Il `CompleteStateChange` metodo determina se una transizione allo stato sospeso è stata completata.

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

Stato prima della transizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se la transizione è stata completata. In caso contrario, restituisce S \_ FALSE.

## <a name="remarks"></a>Commenti

Il [**metodo CBaseRenderer::P ause**](cbaserenderer-pause.md) chiama questo metodo per aggiornare lo stato della transizione di stato. In generale, la transizione a sospesa non termina fino a quando il filtro non riceve un campione. Tuttavia, in alcune situazioni la transizione viene completata immediatamente, ad esempio se il filtro non è interconnesso o se è stata raggiunta la fine del flusso. Questo metodo controlla i vari criteri e quindi chiama il metodo [**CBaseRenderer::Ready**](cbaserenderer-ready.md) o il metodo [**CBaseRenderer::NotReady**](cbaserenderer-notready.md) per aggiornare lo stato della transizione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




