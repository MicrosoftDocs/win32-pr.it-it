---
description: Il metodo GetSourceRect recupera il rettangolo di origine. Si tratta di un metodo interno.
ms.assetid: 51028b79-6aab-4abc-8ee8-2965bda9d191
title: Metodo CBaseControlVideo.GetSourceRect (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a637e0f5ab5c97494dc072458a29920110363a3e4f07ba8bb7313947996bdad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057051"
---
# <a name="cbasecontrolvideogetsourcerect-method"></a>Metodo CBaseControlVideo.GetSourceRect

Il `GetSourceRect` metodo recupera il rettangolo di origine. Si tratta di un metodo interno.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT GetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSourceRect* 
</dt> <dd>

Puntatore al rettangolo di origine recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro deve essere sottoposta a override nella classe derivata per restituire il rettangolo di origine contenuto nel renderer video. Viene chiamato dalle funzioni membro [**CBaseControlVideo**](cbasecontrolvideo.md) seguenti.

-   [**CBaseControlVideo::GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)
-   [**CBaseControlVideo::put \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)
-   [**CBaseControlVideo::get \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)
-   [**CBaseControlVideo::put \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)
-   [**CBaseControlVideo::get \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)
-   [**CBaseControlVideo::put \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**CBaseControlVideo::get \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)
-   [**CBaseControlVideo::put \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)
-   [**CBaseControlVideo::get \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)

Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.


```C++
// Return the current source rectangle
HRESULT CVideoText::GetSourceRect(RECT *pSourceRect)
{
    ASSERT(pSourceRect);
    m_pRenderer->m_DrawImage.GetSourceRect(pSourceRect);
    return NOERROR;
}
```



In questo esempio CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m pRenderer contiene un oggetto di una classe derivata da \_ [**CBaseVideoRenderer**](cbasevideorenderer.md)e il membro dati m DrawImage, definito nella classe derivata, contiene un \_ oggetto [**CDrawImage.**](cdrawimage.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




