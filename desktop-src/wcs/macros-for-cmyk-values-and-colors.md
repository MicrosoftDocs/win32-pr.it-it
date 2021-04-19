---
title: Macro per i valori e i colori CMYK
description: Le macro seguenti sono utili per modificare i valori CMYK.
ms.assetid: e5d107fb-e010-400b-9ec5-90c2c0381dbe
keywords:
- Windows Color System (WCS), macro CMYK
- WCS (Windows Color System), macro CMYK
- Gestione colori immagine, macro CMYK
- gestione dei colori, macro CMYK
- colori, macro CMYK
- Riferimento a WCS, macro CMYK
- informazioni di riferimento sul WCS, le macro CMYK
- Macro CMYK
- cyan magenta giallo nero (CMYK)
- CMYK (cyan magenta giallo nero)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a0efcbb6b0dc25f8f93f420113cc8c0797cba46
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320166"
---
# <a name="macros-for-cmyk-values-and-colors"></a>Macro per i valori e i colori CMYK

Le macro seguenti sono utili per modificare i valori CMYK.



| Macro                          | Descrizione                                                                  |
|--------------------------------|------------------------------------------------------------------------------|
| [**CMYK**](/windows/desktop/api/Wingdi/nf-wingdi-cmyk)           | Compila un valore CMYK dai singoli valori ciano, magenta, giallo e nero. |
| [**GetCValue**](/windows/desktop/api/Wingdi/nf-wingdi-getcvalue) | Recupera il valore del colore ciano da un valore di colore CMYK.                      |
| [**GetKValue**](/windows/desktop/api/Wingdi/nf-wingdi-getkvalue) | Recupera il valore del colore nero da un valore di colore CMYK.                     |
| [**GetMValue**](/windows/desktop/api/Wingdi/nf-wingdi-getmvalue) | Recupera il valore magenta da un valore di colore CMYK.                         |
| [**GetYValue**](/windows/desktop/api/Wingdi/nf-wingdi-getyvalue) | Recupera il valore di colore giallo da un valore di colore CMYK.                    |



 

Le macro seguenti vengono usate con il colore.



| Macro                                | Descrizione                                                                                                                                           |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetBValue**](/windows/win32/api/wingdi/nf-wingdi-getbvalue)       | Ottiene un valore blu RGB.                                                                                                                               |
| [**GetGValue**](/windows/win32/api/wingdi/nf-wingdi-getgvalue)       | Ottiene un valore verde RGB.                                                                                                                              |
| [**GetRValue**](/windows/win32/api/wingdi/nf-wingdi-getrvalue)       | Ottiene un valore rosso RGB.                                                                                                                                |
| [**PALETTEINDEX**](/previous-versions//dd162770(v=vs.85)) | Accetta un indice in una voce della tavolozza dei colori logici e restituisce un identificatore di voce della tavolozza.                                                              |
| [**PALETTERGB**](/windows/win32/api/wingdi/nf-wingdi-palettergb)     | Accetta tre valori che rappresentano le intensità relative di rosso, verde e blu e restituisce un identificatore rosso, verde, blu (RGB) relativo alla tavolozza. |
| [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb)                       | Seleziona un colore rosso, verde, blu (RGB) basato sugli argomenti forniti e sulle funzionalità di colore del dispositivo di output.                               |



 

 

 