---
description: Il metodo UOPValid recupera un valore che indica se l'operazione utente specificata (UOP) è attualmente valida.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Metodo UOPValid (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3051ad20c496713880407270c7054839520ce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326627"
---
# <a name="uopvalid-method"></a>Metodo UOPValid

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `UOPValid` metodo recupera un valore che indica se l'operazione utente specificata (UOP) è attualmente valida.

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*
</dt> <dd>

Specifica l'operazione dell'utente (UOP) come Integer.



| Valore | Descrizione                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | [**PlayTitle**](playtitle-method.md), [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)                                                                                      |
| 1     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 2     | [**PlayTitle**](playtitle-method.md)                                                                                                                                                                                    |
| 3     | [**Interrompere**](stop-method.md)                                                                                                                                                                                              |
| 4     | [**ReturnFromSubmenu**](returnfromsubmenu-method.md)                                                                                                                                                                    |
| 5     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 6     | [**PlayPrevChapter**](playprevchapter-method.md), [ **ReplayChapter**](replaychapter-method.md)                                                                                                                         |
| 7     | [**PlayNextChapter**](playnextchapter-method.md)                                                                                                                                                                        |
| 8     | [**PlayForwards**](playforwards-method.md)                                                                                                                                                                              |
| 9     | [**PlayBackwards**](playbackwards-method.md)                                                                                                                                                                            |
| 10    | [**ShowMenu**](showmenu-method.md) con un valore di parametro di 2 ( \_ titolo del menu DVD \_ )                                                                                                                                       |
| 11    | [**ShowMenu**](showmenu-method.md) con un valore del parametro 3 ( \_ radice del menu DVD \_ )                                                                                                                                        |
| 12    | [**ShowMenu**](showmenu-method.md) con un valore di parametro 4 ( \_ menu di scelta rapida del menu DVD \_ )                                                                                                                                  |
| 13    | [**ShowMenu**](showmenu-method.md) con valore parametro 5 ( \_ audio menu DVD \_ )                                                                                                                                       |
| 14    | [**ShowMenu**](showmenu-method.md) con un valore di parametro di 6 ( \_ angolo del menu DVD \_ )                                                                                                                                       |
| 15    | [**ShowMenu**](showmenu-method.md) con un valore di parametro pari a 7 \_ ( \_ capitolo menu DVD)                                                                                                                                     |
| 16    | [**Riprendi**](resume-method.md)                                                                                                                                                                                          |
| 17    | [**SelectLeftButton**](selectleftbutton-method.md), [**SelectRightButton**](selectrightbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md) |
| 18    | [**StillOff**](stilloff-method.md)                                                                                                                                                                                      |
| 19    | [**Sospendere**](pause-method.md)                                                                                                                                                                                            |
| 20    | [**CurrentAudioStream**](currentaudiostream-property.md)                                                                                                                                                                |
| 21    | [**CurrentSubpictureStream**](currentsubpicturestream-property.md)                                                                                                                                                      |
| 22    | [**CurrentAngle**](currentangle-property.md), [ **SelectParentalLevel**](selectparentallevel-method.md)                                                                                                                 |
| 23    | [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| 24    | Selezionare preferenza modalità video.                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se l'operazione specificata è consentita dal controllo UOP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segmento. h</dt> </dl> |



 

 




