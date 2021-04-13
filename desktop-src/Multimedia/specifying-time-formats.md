---
title: Specifica di formati di ora
description: Specifica di formati di ora
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- MCIWndGetTimeFormat (macro)
- MCIWndSetTimeFormat (macro)
- MCIWndUseTime (macro)
- MCIWndUseFrames (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330060"
---
# <a name="specifying-time-formats"></a>Specifica di formati di ora

I tipi di dati multimediali possono in genere utilizzare il tempo per identificare posizioni significative all'interno del contenuto. I formati di ora comuni sono millisecondi, tracce e frame; Esistono anche altri formati di tempo meno comuni, ad esempio SMPTE (Society of Motion Picture e Television Engineers) 24. Time è il formato e il sistema di riferimento per i dati audio della forma d'onda, MIDI e CD. Il video supporta il tempo anche se viene registrato come sequenza di frame (flusso) che in genere viene riprodotta a una velocità specifica. Sono disponibili diverse macro per la designazione del formato ora.

È possibile recuperare il formato dell'ora corrente per un file o un dispositivo usando la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) . È possibile modificare il formato dell'ora corrente con qualsiasi altro formato di ora supportato da un dispositivo usando la macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) . In alternativa, è possibile impostare il formato dell'ora su millisecondi o frame usando le macro [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) o [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) .

> [!Note]  
> I formati non continui, ad esempio Tracks e SMPTE, possono causare un comportamento anomalo della barra degli strumenti. Per questi formati temporali, potrebbe essere necessario disattivare la barra degli strumenti specificando lo \_ stile della finestra NOPLAYBAR di MCIWNDF durante la creazione di una finestra di MCIWnd.

 

 

 




