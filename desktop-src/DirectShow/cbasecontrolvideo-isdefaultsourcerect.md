---
description: Il metodo IsDefaultSourceRect determina se il renderer usa il rettangolo di origine predefinito (virtuale puro).
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: Metodo CBaseControlVideo.IsDefaultSourceRect (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8cdce3f01bc3a0ed28ee9ce758ef6cb136676a9bd8b4b314547103045e5b284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056871"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a>Metodo CBaseControlVideo.IsDefaultSourceRect

Il `IsDefaultSourceRect` metodo determina se il renderer usa il rettangolo di origine predefinito (virtuale puro).

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK se il renderer usa l'origine predefinita; in caso contrario, restituisce S \_ FALSE.

## <a name="remarks"></a>Commenti

Questa funzione membro deve essere implementata nella classe derivata. Viene chiamato dalla funzione membro [**CBaseControlVideo::IsUsingDefaultSource.**](cbasecontrolvideo-isusingdefaultsource.md)

Nell'esempio seguente viene illustrata un'implementazione di questa funzione in una classe derivata.


```C++
// Return S_OK if using the default source; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultSourceRect()
{
    RECT SourceRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetSourceRect(&SourceRect);

    // Check the coordinates that match the video dimensions.

    if (SourceRect.left != 0 || SourceRect.top != 0 ||
            SourceRect.right != pHeader->biWidth ||
                SourceRect.bottom != pHeader->biHeight) {
                    return S_FALSE;
    }
    return S_OK;
}
```



In questo esempio CVideoText è una classe derivata da [**CBaseControlVideo**](cbasecontrolvideo.md), m pRenderer contiene un oggetto di una classe derivata da \_ [**CBaseVideoRenderer**](cbasevideorenderer.md)e il membro dati m DrawImage, definito nella classe derivata, contiene un \_ oggetto [**CDrawImage.**](cdrawimage.md) Il membro dati m mtIn, definito anche nella classe derivata, contiene un \_ [**oggetto CMediaType**](cmediatype.md) con il tipo di supporto del pin di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




