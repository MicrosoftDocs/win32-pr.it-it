---
title: Funzioni di base da usare all'interno di un contesto di dispositivo
description: Le funzioni WCS seguenti offrono funzionalità di mapping dei colori di base all'interno di contesti di dispositivo. Sono utili per tutte le applicazioni che devono implementare la gestione dei colori con un sovraccarico ridotto e un intervento minimo dell'utente.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Windows Color System (WCS), funzioni
- WCS (Windows Color System), funzioni
- Gestione colori immagine, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Riferimento a WCS, funzioni
- informazioni di riferimento su WCS, funzioni
- Windows Color System (WCS), contesti di dispositivo
- WCS (sistema di colori Windows), contesti di dispositivo
- Gestione colori immagine, contesti di dispositivo
- gestione dei colori, contesti di dispositivo
- colori, contesti di dispositivo
- Riferimento a WCS, contesti di dispositivo
- informazioni di riferimento per WCS, contesti di dispositivo
- contesti di dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde99ed077af108ddc20c73f86e17bedfe1d4a8c
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "106320188"
---
# <a name="basic-functions-for-use-within-a-device-context"></a>Funzioni di base da usare all'interno di un contesto di dispositivo

Le funzioni WCS seguenti offrono funzionalità di [mapping dei colori](c.md) di base all'interno di contesti di dispositivo. Sono utili per tutte le applicazioni che devono implementare la gestione dei colori con un sovraccarico ridotto e un intervento minimo dell'utente.



| Funzione                                                           | Descrizione                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckColorsInGamut**](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | Controlla se i colori specificati si trovano nel gamut del dispositivo.                                                                                                     |
| [**ColorCorrectPalette**](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | Corregge le voci in una tavolozza per un contesto di dispositivo.                                                                                             |
| [**ColorMatchToTarget**](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | Esegue il mapping dei colori a scopo di anteprima.                                                                                                        |
| [**CreateColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | Crea uno spazio colore.                                                                                                                              |
| [**DeleteColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | Elimina uno spazio colore.                                                                                                                              |
| [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | Enumera i profili dei colori di output disponibili per un determinato contesto di dispositivo.                                                                              |
| [**EnumICMProfilesProcCallback**](/windows/desktop/api/Wingdi/) | Funzione di callback definita dall'applicazione per [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa). Il nome di questa funzione viene definito anche dall'applicazione. |
| [**GetColorSpace**](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | Ottiene lo spazio del colore di input corrente in un contesto di dispositivo. |
| [**GetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | Ottiene il profilo del colore di output corrente di un contesto di dispositivo.                                                                                          |
| [**GetLogColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | Ottiene la struttura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) di un contesto di dispositivo.                                                                      |
| [**SetColorSpace**](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | Imposta lo spazio colore di input di un contesto di dispositivo.                                                                                                          |
| [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | Attiva o disattiva la gestione dei colori in un contesto di dispositivo.                                                                                               |
| [**SetICMProfile**](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | Imposta il profilo del colore di output per un contesto di dispositivo specificato.                                                                                           |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | Enumera tutti i profili colori che soddisfano i criteri di enumerazione nell'ambito di gestione del profilo specificato.                                      |



 

 

 




