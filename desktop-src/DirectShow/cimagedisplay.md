---
description: La classe CImageDisplay è una classe helper che consente ai renderer video GDI di gestire il formato di visualizzazione.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: Classe CImageDisplay (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 551650e7c8b6b0f830a84aee37bf671bbc300224c9e300a3f6f841ef503a504d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428946"
---
# <a name="cimagedisplay-class"></a>Classe CImageDisplay

![cimagedisplayclasshierarchy](images/wutil06.png)

La `CImageDisplay` classe è una classe helper che consente ai renderer video GDI di gestire il formato di visualizzazione. L'oggetto archivia [**una struttura VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) che descrive la modalità di visualizzazione corrente, inizializzata nel metodo costruttore dell'oggetto. Il metodo **CheckMediaType dell'oggetto** controlla se il rendering di un tipo di supporto proposto può essere eseguito in modo efficiente tramite GDI.



| Variabili membro protette                                       | Descrizione                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**m \_ Display**](cimagedisplay-m-display.md)                    | **Struttura VIDEOINFO** che descrive il formato di visualizzazione corrente.                     |
| Metodi protetti                                                | Descrizione                                                                            |
| [**CheckBitFields**](cimagedisplay-checkbitfields.md)           | Convalida le maschere di colore in una **struttura VIDEOINFO.**                                |
| [**CountPrefixBits**](cimagedisplay-countprefixbits.md)         | Calcola il numero di bit zero all'inizio di un campo di bit specificato.              |
| [**CountSetBits**](cimagedisplay-countsetbits.md)               | Restituisce il numero di bit impostato su 1 in un campo di bit specificato.                          |
| Metodi pubblici                                                   | Descrizione                                                                            |
| [**CheckHeaderValidity**](cimagedisplay-checkheadervalidity.md) | Convalida una [**struttura BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)                    |
| [**CheckMediaType**](cimagedisplay-checkmediatype.md)           | Determina se un tipo di supporto proposto è compatibile con il formato di visualizzazione.        |
| [**CheckPaletteHeader**](cimagedisplay-checkpaletteheader.md)   | Convalida le voci della tavolozza in una **struttura VIDEOINFO.**                            |
| [**CheckVideoType**](cimagedisplay-checkvideotype.md)           | Controlla se un formato **VIDEOINFO** specificato è compatibile con il formato di visualizzazione. |
| [**CImageDisplay**](cimagedisplay-cimagedisplay.md)             | Metodo del costruttore.                                                                    |
| [**GetBitMasks**](cimagedisplay-getbitmasks.md)                 | Recupera le maschere di colore per un formato **VIDEOINFO** specificato.                        |
| [**GetColourMask**](cimagedisplay-getcolourmask.md)             | Recupera le maschere di colore per il formato di visualizzazione corrente.                              |
| [**GetDisplayDepth**](cimagedisplay-getdisplaydepth.md)         | Recupera la profondità in bit della modalità di visualizzazione corrente.                                   |
| [**GetDisplayFormat**](cimagedisplay-getdisplayformat.md)       | Recupera un formato video che descrive la modalità di visualizzazione corrente.                      |
| [**IsPalettised**](cimagedisplay-ispalettised.md)               | Verifica se il formato di visualizzazione corrente è stato cancellato.                           |
| [**RefreshDisplayType**](cimagedisplay-refreshdisplaytype.md)   | Aggiorna il formato video dell'oggetto in modo che corrisponda alla visualizzazione specificata                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




