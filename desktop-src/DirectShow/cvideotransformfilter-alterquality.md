---
description: "Il metodo AlterQuality notifica al filtro che è richiesta una modifica di qualità. Questo metodo esegue l'override del metodo CTransformFilter:: AlterQuality."
ms.assetid: 9a1d1379-8557-4b33-ab49-b5c6a684f685
title: Metodo CVideoTransformFilter. AlterQuality (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1de0985b8cb3a8db6f45c247e717042cf344655f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324177"
---
# <a name="cvideotransformfilteralterquality-method"></a>CVideoTransformFilter. AlterQuality, metodo

Il `AlterQuality` metodo notifica al filtro che è richiesta una modifica di qualità. Questo metodo esegue l'override del metodo [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md) .

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*d* 
</dt> <dd>

Struttura di [**qualità**](/windows/win32/api/strmif/ns-strmif-quality) che contiene il messaggio di controllo di qualità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E ha \_ esito negativo.

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato quando il pin di output riceve un messaggio di qualità (tramite il metodo [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) ).

Il valore di ritardo da *q* viene archiviato nella variabile **membro \_ itrLate m** . Il valore restituito di E \_ Fail indica che il renderer dovrebbe essere aggiornato eliminando i frame, sebbene anche la classe **CVideoTransformFilter** elimini i frame nelle condizioni corrette.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> <dt>

[**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)
</dt> </dl>

 

 




