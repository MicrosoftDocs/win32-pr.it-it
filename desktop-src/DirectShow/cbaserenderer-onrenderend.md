---
description: Il metodo OnRenderEnd viene chiamato dopo il rendering di un esempio.
ms.assetid: c9b3a3b2-a5c0-4a08-9e55-53c27a4d1032
title: Metodo CBaseRenderer.OnRenderEnd (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5fe720ecaa6cc72a0efae3fceda3bb307573077caee6de5ac4309207883c994d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526537"
---
# <a name="cbaserendereronrenderend-method"></a>Metodo CBaseRenderer.OnRenderEnd

Il `OnRenderEnd` metodo viene chiamato dopo il rendering di un campione.

## <a name="syntax"></a>Sintassi


```C++
virtual void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il [**metodo CBaseRenderer::Render**](cbaserenderer-render.md) chiama questo metodo. Non esegue alcuna operazione nella classe di base, ma la classe derivata può eseguirne l'override; ad esempio per raccogliere dati di controllo qualità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




