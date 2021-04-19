---
description: La classe CImageDisplay è una classe helper per i renderer video GDI per gestire il formato di visualizzazione.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: Classe CImageDisplay (Winutil. h)
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
ms.openlocfilehash: a5a7cbb28c53d8ff357d4e5174d24f92ba2d0cad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332275"
---
# <a name="cimagedisplay-class"></a>Classe CImageDisplay

![cimagedisplayclasshierarchy](images/wutil06.png)

La `CImageDisplay` classe è una classe helper per i renderer video GDI per gestire il formato di visualizzazione. L'oggetto archivia una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) che descrive la modalità di visualizzazione corrente, inizializzata nel metodo del costruttore dell'oggetto. Il metodo **CheckMediaType** dell'oggetto verifica se è possibile eseguire il rendering efficiente di un tipo di supporto proposto utilizzando GDI.



| Variabili membro protette                                       | Descrizione                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_visualizzazione m**](cimagedisplay-m-display.md)                    | Struttura **VIDEOINFO** che descrive il formato di visualizzazione corrente.                     |
| Metodi protetti                                                | Descrizione                                                                            |
| [**CheckBitFields**](cimagedisplay-checkbitfields.md)           | Convalida le maschere dei colori in una struttura **VIDEOINFO** .                                |
| [**CountPrefixBits**](cimagedisplay-countprefixbits.md)         | Calcola il numero di bit zero all'inizio di un campo di bit specificato.              |
| [**CountSetBits**](cimagedisplay-countsetbits.md)               | Restituisce il numero di bit impostato su 1 in un campo di bit specificato.                          |
| Metodi pubblici                                                   | Descrizione                                                                            |
| [**CheckHeaderValidity**](cimagedisplay-checkheadervalidity.md) | Convalida una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .                    |
| [**CheckMediaType**](cimagedisplay-checkmediatype.md)           | Determina se un tipo di supporto proposto è compatibile con il formato di visualizzazione.        |
| [**CheckPaletteHeader**](cimagedisplay-checkpaletteheader.md)   | Convalida le voci della tavolozza in una struttura **VIDEOINFO** .                            |
| [**CheckVideoType**](cimagedisplay-checkvideotype.md)           | Verifica se un formato **VIDEOINFO** specificato è compatibile con il formato di visualizzazione. |
| [**CImageDisplay**](cimagedisplay-cimagedisplay.md)             | Metodo del costruttore.                                                                    |
| [**Getmascheramenti**](cimagedisplay-getbitmasks.md)                 | Recupera le maschere dei colori per un formato **VIDEOINFO** specificato.                        |
| [**GetColourMask**](cimagedisplay-getcolourmask.md)             | Recupera le maschere dei colori per il formato di visualizzazione corrente.                              |
| [**GetDisplayDepth**](cimagedisplay-getdisplaydepth.md)         | Recupera la profondità di bit della modalità di visualizzazione corrente.                                   |
| [**GetDisplayFormat**](cimagedisplay-getdisplayformat.md)       | Recupera un formato video che descrive la modalità di visualizzazione corrente.                      |
| [**IsPalettised**](cimagedisplay-ispalettised.md)               | Determina se il formato di visualizzazione corrente è pallettizzati.                           |
| [**RefreshDisplayType**](cimagedisplay-refreshdisplaytype.md)   | Aggiorna il formato video dell'oggetto in modo che corrisponda alla visualizzazione specificata                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




