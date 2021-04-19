---
description: Il metodo SetSourceRect imposta il rettangolo del video di origine corrente (virtuale puro). Si tratta di una funzione membro interna che viene chiamata quando il rettangolo di origine viene modificato.
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: Metodo CBaseControlVideo. SetSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e3be6cc3819e1452fd196d4906377204a6e90bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332354"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a>CBaseControlVideo. SetSourceRect, metodo

Il `SetSourceRect` metodo imposta il rettangolo del video di origine corrente (virtuale puro). Si tratta di una funzione membro interna che viene chiamata quando il rettangolo di origine viene modificato.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Puntatore al rettangolo di origine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Le classi derivate devono eseguire l'override di questa funzione membro per capire quando viene modificato il rettangolo di origine. Viene chiamato dalle funzioni membro seguenti.

-   [**CBaseControlVideo::SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)
-   [**CBaseControlVideo::p UT \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)
-   [**CBaseControlVideo::p UT \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)
-   [**CBaseControlVideo::p UT \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**CBaseControlVideo::p UT \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)

Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
    return NOERROR;
}
```



In questo esempio, CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m \_ pRenderer include un oggetto di una classe derivata da [**CBaseVideoRenderer**](cbasevideorenderer.md)e il \_ membro dati DrawImage m, definito nella classe derivata, include un oggetto [**CDrawImage**](cdrawimage.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




