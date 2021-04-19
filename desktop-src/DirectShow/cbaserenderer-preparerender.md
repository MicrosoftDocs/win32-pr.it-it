---
description: Il metodo PrepareRender viene chiamato prima che il filtro esegua il rendering di un campione.
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: Metodo CBaseRenderer. PrepareRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee5739a839222900458ae334de6f97fb6d18876b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333340"
---
# <a name="cbaserendererpreparerender-method"></a>CBaseRenderer. PrepareRender, metodo

Il `PrepareRender` metodo viene chiamato prima che il filtro esegua il rendering di un campione.

## <a name="syntax"></a>Sintassi


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il filtro chiama questo metodo prima di chiamare il metodo [**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) o il metodo [**CBaseRenderer:: Render**](cbaserenderer-render.md) . `PrepareRender` non esegue alcuna operazione nella classe di base. La classe derivata può eseguire l'override di questa classe per eseguire le azioni necessarie prima del rendering. Un renderer video, ad esempio, può eseguire l'override di questo metodo per realizzare la relativa tavolozza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




