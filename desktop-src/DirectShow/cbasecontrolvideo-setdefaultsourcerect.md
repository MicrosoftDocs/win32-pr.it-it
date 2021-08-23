---
description: Il metodo SetDefaultSourceRect imposta il rettangolo video di origine predefinito (virtuale puro). In una funzione membro interna che viene chiamata quando viene reimpostato il rettangolo di origine.
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: Metodo CBaseControlVideo.SetDefaultSourceRect (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae7f2e88e170b0c21187b2615029fcb4ed2bed4717af09b60eb4309aee2bea0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432611"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a>Metodo CBaseControlVideo.SetDefaultSourceRect

Il `SetDefaultSourceRect` metodo imposta il rettangolo video di origine predefinito (virtuale puro). In una funzione membro interna che viene chiamata quando viene reimpostato il rettangolo di origine.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Le classi derivate devono eseguire l'override di questo metodo per reimpostare il rettangolo di origine. Viene chiamato da [**CBaseControlVideo::SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md).

Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



In questo esempio CVideoText è una classe derivata da [**CBaseControlVideo,**](cbasecontrolvideo.md)m pRenderer contiene un oggetto di una classe derivata da \_ [**CBaseVideoRenderer**](cbasevideorenderer.md)e il membro dati m DrawImage, definito nella classe derivata, contiene un oggetto \_ [**CDrawImage.**](cdrawimage.md) Il membro dati m mtIn, definito anche nella classe derivata, contiene un oggetto CMediaType con il tipo di supporto \_ del pin di input. [](cmediatype.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




