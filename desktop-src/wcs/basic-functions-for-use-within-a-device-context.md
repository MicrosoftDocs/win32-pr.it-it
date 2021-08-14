---
title: Funzioni di base da usare all'interno di un contesto di dispositivo
description: Le funzioni WCS seguenti offrono funzionalità di base per il mapping dei colori all'interno dei contesti di dispositivo. Sono utili per tutte le applicazioni che devono implementare la gestione dei colori con sovraccarico ridotto e intervento minimo da parte dell'utente.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Windows Sistema colori (WCS), funzioni
- WCS (Windows Color System),funzioni
- gestione dei colori delle immagini, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Informazioni di riferimento su WCS, funzioni
- informazioni di riferimento per WCS, funzioni
- Windows Sistema colori (WCS), contesti di dispositivo
- WCS (Windows Color System),contesti di dispositivo
- gestione dei colori delle immagini, contesti di dispositivo
- gestione dei colori, contesti di dispositivo
- colori, contesti di dispositivo
- Informazioni di riferimento su WCS, contesti di dispositivo
- informazioni di riferimento per WCS, contesti di dispositivo
- contesti di dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a934c1737a7eea8b32a9589325e73300db82334a40ee47b411922b89cb61f568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118210980"
---
# <a name="basic-functions-for-use-within-a-device-context"></a>Funzioni di base da usare all'interno di un contesto di dispositivo

Le funzioni WCS seguenti offrono funzionalità di [base per il mapping dei colori](c.md) all'interno dei contesti di dispositivo. Sono utili per tutte le applicazioni che devono implementare la gestione dei colori con sovraccarico ridotto e intervento minimo da parte dell'utente.



| Funzione                                                           | Descrizione                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | Controlla se i colori sono nella gamma di un dispositivo.                                                                                                     |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | Corregge le voci in una tavolozza per un contesto di dispositivo.                                                                                             |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | Esegue il mapping dei colori a scopo di anteprima.                                                                                                        |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | Crea uno spazio colore.                                                                                                                              |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | Elimina uno spazio colore.                                                                                                                              |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | Enumera i profili colori di output disponibili per un determinato contesto di dispositivo.                                                                              |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/) | Funzione di callback definita dall'applicazione [**per EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa). Il nome di questa funzione è definito anche dall'applicazione. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Ottiene lo spazio colore di input corrente in un contesto di dispositivo. |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | Ottiene il profilo colore di output corrente di un contesto di dispositivo.                                                                                          |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | Ottiene la [**struttura LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) di un contesto di dispositivo.                                                                      |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | Imposta lo spazio colore di input di un contesto di dispositivo.                                                                                                          |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | Attiva o disattiva la gestione dei colori in un contesto di dispositivo.                                                                                               |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | Imposta il profilo colore di output per un determinato contesto di dispositivo.                                                                                           |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | Enumera tutti i profili colori che soddisfano i criteri di enumerazione nell'ambito di gestione dei profili specificato.                                      |



 

 

 




