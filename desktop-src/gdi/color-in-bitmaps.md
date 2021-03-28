---
description: Il sistema gestisce i colori nelle bitmap in modo diverso rispetto ai colori in penne, pennelli e testo.
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: Colore nelle bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130818"
---
# <a name="color-in-bitmaps"></a>Colore nelle bitmap

Il sistema gestisce i colori nelle bitmap in modo diverso rispetto ai colori in penne, pennelli e testo. Le bitmap compatibili, create tramite la funzione [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) o [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , sono specifiche del dispositivo e mantengono le informazioni sui colori in un formato dipendente dal dispositivo. Non viene usato alcun valore di colore e i colori non sono soggetti ad approssimazioni e dithering.

Le bitmap indipendenti dal dispositivo conservano le informazioni sui colori come valori dei colori o indici della tavolozza dei colori. Se vengono utilizzati i valori dei colori, i colori sono soggetti a approssimazione, ma non a rethering. Gli indici della tavolozza dei colori possono essere usati solo con i dispositivi che supportano le tavolozze dei colori. Anche se il sistema non approssimativo o i colori di dithering identificati da indici, il colore risultante può essere diverso da quello previsto, perché gli indici restituiscono risultati validi solo nel contesto della tavolozza dei colori che era corrente al momento della creazione della bitmap. Se la tavolozza viene modificata, eseguire i colori nella bitmap. Per ulteriori informazioni sugli indici della tavolozza, vedere [default palette](default-palette.md) and [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).

Oltre a fare riferimento alla tavolozza logica, un'applicazione può anche fare riferimento a un valore in una tabella dei colori DIB. Per selezionare un colore in una tabella di colori DIB, chiamare [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex). Si noti che questo è possibile solo per un contesto di dispositivo in cui è stata selezionata una DIB.

 

 



