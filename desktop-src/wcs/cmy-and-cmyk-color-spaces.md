---
title: Spazi colori CMY e CMYK
description: Gli spazi colori CMY e CMYK vengono spesso usati nella stampa a colori. Uno spazio colori CMY usa ciano, magenta e giallo (CMY) come colori primari. Rosso, verde e blu sono i colori secondari.
ms.assetid: e135b5ef-fa5c-49b7-8537-5dc31cde2418
keywords:
- Windows Sistema colori (WCS), spazi colori CMY
- WCS (Windows Color System), spazi colori CMY
- gestione del colore delle immagini,spazi colori CMY
- gestione del colore,spazi colori CMY
- colori,spazi colori CMY
- spazi dei colori,CMY
- Spazi colori CMY
- Windows Sistema colori (WCS), spazi colori CMYK
- WCS (Windows Color System), spazi colori CMYK
- gestione del colore delle immagini,spazi colori CMYK
- gestione dei colori, spazi CMYKcolor
- colori,spazi colori CMYK
- spazi dei colori,CMYK
- Spazi colori CMYK
- ciano
- magenta
- yellow
- ciano magenta giallo (CMY)
- CMY (giallo magenta ciano)
- ciano magenta giallo nero (CMYK)
- CMYK (nero giallo magenta ciano)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdcb1ea33bd32346dd541894342ec4af02274e4381eaf0c1925e2a4bc20e10c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452102"
---
# <a name="cmy-and-cmyk-color-spaces"></a>Spazi colori CMY e CMYK

Gli spazi colori CMY e [CMYK](c.md) vengono spesso usati nella stampa a colori. Uno spazio colori CMY usa ciano, magenta e giallo (CMY) come [colori primari.](p.md) Rosso, verde e blu sono i colori secondari.

Le figure seguenti sono rappresentazioni a colori dello spazio colore CMY. Lo spazio colori CMY viene normalizzato.

![Cubo dello spazio colori cmy ai valori massimi](images/cmyclrs1.png)

![Cubo dello spazio colori cmy ai valori minimi](images/cmyclrs2.png)

Lo spazio colore CMY è sottrativo. Pertanto, il bianco è in (0.0, 0.0, 0.0) e il nero è in (1.0, 1.0, 1.0). Se si inizia con il bianco e non si sottraggono colori, si ottiene il bianco. Se si inizia con il bianco e si sottraggono tutti i colori in modo uniforme, si ottiene il nero.

Lo spazio colori CMYK è una variazione nel modello CMY. Aggiunge il nero (Cyan, Magenta, Yellow e blacK). Lo spazio colore CMYK chiude il divario tra teoria e pratica. In teoria, il componente nero aggiuntivo non è necessario. Tuttavia, l'esperienza con vari tipi di inks e paper ha dimostrato che quando i componenti uguali degli inks ciano, magenta e giallo sono misti, il risultato è in genere un marrone scuro, non nero. L'aggiunta dell'input penna nero alla combinazione risolve questo problema.

Gli spazi dei colori CMY e CMYK possono essere indipendenti dal dispositivo, ma nella maggior parte dei casi vengono usati in riferimento a un dispositivo specifico.

 

 




