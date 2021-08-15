---
description: Il metodo AbortPlayback viene usato per segnalare un errore di streaming. Invia un evento EC ERRORABORT a Filter Graph Manager e invia una notifica di fine \_ flusso a valle.
ms.assetid: b48ec72f-d220-4b27-98fc-88eaa4f663eb
title: Metodo CVideoTransformFilter.AbortPlayback (Vtrans.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.AbortPlayback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6560e7ce704423bfecc519c709c2c08733fe90a2346324f9e1282571530293ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821936"
---
# <a name="cvideotransformfilterabortplayback-method"></a>Metodo CVideoTransformFilter.AbortPlayback

Il `AbortPlayback` metodo viene usato per segnalare un errore di streaming. Invia un [**evento EC \_ ERRORABORT**](ec-errorabort.md) a Filter Graph Manager e invia una notifica downstream di fine flusso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AbortPlayback(
   HRESULT hr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*h* 
</dt> <dd>

**Valore HRESULT** dell'operazione non riuscita. Questo valore viene usato come primo parametro di evento per \_ l'evento EC ERRORABORT.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore del *parametro hr.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Vtrans.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CVideoTransformFilter**](cvideotransformfilter.md)
</dt> </dl>

 

 




