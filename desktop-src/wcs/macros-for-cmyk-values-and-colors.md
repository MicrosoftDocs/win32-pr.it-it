---
title: Macro per valori e colori CMYK
description: Le macro seguenti sono utili per modificare i valori CMYK.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Windows Sistema colori (WCS), macro CMYK
- WCS (Windows Color System),macro CMYK
- gestione dei colori delle immagini, macro CMYK
- gestione dei colori, macro CMYK
- colori, macro CMYK
- Informazioni di riferimento su WCS, macro CMYK
- informazioni di riferimento per le macro WCS,CMYK
- Macro CMYK
- ciano magenta giallo nero (CMYK)
- CMYK (nero giallo magenta ciano)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591c479686db45f1b0d6fc6097d5134de481307b144200604a15b360bcf2c146
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593361"
---
# <a name="macros-for-cmyk-values-and-colors"></a>Macro per valori e colori CMYK

Le macro seguenti sono utili per modificare i valori CMYK.



| Macro                          | Descrizione                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [**Cmyk**](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | Compila un valore CMYK da singoli valori ciano, magenta, giallo e nero. |
| [**GetCValue**](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | Recupera il valore del colore ciano da un valore di colore CMYK.                      |
| [**GetKValue**](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | Recupera il valore del colore nero da un valore di colore CMYK.                     |
| [**GetMValue**](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | Recupera il valore magenta da un valore di colore CMYK.                         |
| [**GetYValue**](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | Recupera il valore del colore giallo da un valore di colore CMYK.                    |



 

Le macro seguenti vengono usate con il colore.



| Macro                                | Descrizione                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBValue**](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | Ottiene un valore RGB blu.                                                                                                                               |
| [**GetGValue**](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | Ottiene un valore RGB verde.                                                                                                                              |
| [**GetRValue**](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | Ottiene un valore RGB rosso.                                                                                                                                |
| [**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85)) | Accetta un indice per una voce della tavolozza dei colori logici e restituisce un identificatore di voce della tavolozza.                                                              |
| [**PALETTERGB**](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | Accetta tre valori che rappresentano le intensità relative di rosso, verde e blu e restituisce un identificatore RGB (Red, Green, Blue) relativo alla tavolozza. |
| [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | Seleziona un colore rosso, verde, blu (RGB) in base all'argomento fornito e alle funzionalità di colore del dispositivo di output.                               |



 

 

 