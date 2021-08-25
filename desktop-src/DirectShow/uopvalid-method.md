---
description: Il metodo UOPValid recupera un valore che indica se l'operazione utente specificata è attualmente valida.
ms.assetid: 0d2c4693-95eb-4cc8-a8f6-61fd0b6d57be
title: Metodo UOPValid (Segment.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eee8f11fbcc51c982b2a619f35fdd56b0f0eebe86945e84f18d6ce62afa783b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078671"
---
# <a name="uopvalid-method"></a>Metodo UOPValid

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `UOPValid` metodo recupera un valore che indica se l'operazione utente specificata è attualmente valida.

``` syntax
[ bIsValid = ] MSWebDVD.UOPValid(iUOP)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iUOP"></span><span id="iuop"></span><span id="IUOP"></span>*iUOP*
</dt> <dd>

Specifica l'operazione utente (UOP) come integer.



| Valore | Descrizione                                                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | [**PlayTitle,**](playtitle-method.md) [**PlayAtTime**](playattime-method.md)[**PlayAtTimeInTitle**](playattimeintitle-method.md)                                                                                      |
| 1     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 2     | [**PlayTitle**](playtitle-method.md)                                                                                                                                                                                    |
| 3     | [**Fermare**](stop-method.md)                                                                                                                                                                                              |
| 4     | [**ReturnFromSubmenu**](returnfromsubmenu-method.md)                                                                                                                                                                    |
| 5     | [**PlayChapter**](playchapter-method.md)                                                                                                                                                                                |
| 6     | [**PlayPrevChapter**](playprevchapter-method.md), [ **ReplayChapter**](replaychapter-method.md)                                                                                                                         |
| 7     | [**PlayNextChapter**](playnextchapter-method.md)                                                                                                                                                                        |
| 8     | [**PlayForwards**](playforwards-method.md)                                                                                                                                                                              |
| 9     | [**PlayBackwards**](playbackwards-method.md)                                                                                                                                                                            |
| 10    | [**ShowMenu**](showmenu-method.md) con valore di parametro 2 (TITOLO \_ MENU \_ DVD)                                                                                                                                       |
| 11    | [**ShowMenu**](showmenu-method.md) con valore di parametro 3 (RADICE \_ MENU \_ DVD)                                                                                                                                        |
| 12    | [**ShowMenu**](showmenu-method.md) con valore di parametro 4 \_ (sottopicture MENU \_ DVD)                                                                                                                                  |
| 13    | [**ShowMenu**](showmenu-method.md) con valore di parametro 5 (DVD \_ MENU \_ Audio)                                                                                                                                       |
| 14    | [**ShowMenu**](showmenu-method.md) con valore di parametro 6 (ANGOLO \_ MENU \_ DVD)                                                                                                                                       |
| 15    | [**ShowMenu**](showmenu-method.md) con valore di parametro 7 (capitolo \_ MENU \_ DVD)                                                                                                                                     |
| 16    | [**Riprendi**](resume-method.md)                                                                                                                                                                                          |
| 17    | [**SelectLeftButton,**](selectleftbutton-method.md) [**SelectRightButton,**](selectrightbutton-method.md) [**SelectUpperButton,**](selectupperbutton-method.md) [**SelectLowerButton**](selectlowerbutton-method.md) |
| 18    | [**StillOff**](stilloff-method.md)                                                                                                                                                                                      |
| 19    | [**Sospendi**](pause-method.md)                                                                                                                                                                                            |
| 20    | [**CurrentAudioStream**](currentaudiostream-property.md)                                                                                                                                                                |
| 21    | [**CurrentSubpictureStream**](currentsubpicturestream-property.md)                                                                                                                                                      |
| 22    | [**CurrentAngle**](currentangle-property.md), [ **SelectParentalLevel**](selectparentallevel-method.md)                                                                                                                 |
| 23    | [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)                                                                                                                                            |
| 24    | Selezionare la preferenza modalità video.                                                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se l'operazione specificata è consentita dal controllo UOP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Segment.h</dt> </dl> |



 

 




