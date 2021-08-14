---
title: Specifica dei formati di ora
description: Specifica dei formati di ora
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- Macro MCIWndGetTimeFormat
- Macro MCIWndSetTimeFormat
- Macro MCIWndUseTime
- Macro MCIWndUseFrames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c14303879a3d13d018be8691eb1947ee1ed67907df796ae38cffc3936bf2ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801704"
---
# <a name="specifying-time-formats"></a>Specifica dei formati di ora

I tipi di dati multimediali in genere possono usare il tempo per identificare posizioni significative all'interno del contenuto. I formati di ora comuni sono millisecondi, tracce e fotogrammi. Esistono anche altri formati di ora meno comuni, ad esempio SMPTE (Society of Motion Picture and Television Engineers) 24. L'ora è il formato e il sistema di riferimento per i dati audio waveform-audio, MIDI e CD. Il video supporta il tempo anche se viene registrato come una sequenza di fotogrammi (flusso) che viene in genere riprodotta a una velocità specifica. Sono disponibili diverse macro per la designazione del formato dell'ora.

È possibile recuperare il formato dell'ora corrente per un file o un dispositivo usando la macro [**MCIWndGetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) È possibile modificare il formato dell'ora corrente in qualsiasi altro formato di ora supportato da un dispositivo usando la macro [**MCIWndSetTimeFormat.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) Oppure è possibile impostare il formato dell'ora su millisecondi o fotogrammi usando le macro [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) o [**MCIWndUseFrames.**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)

> [!Note]  
> I formati non contigui, ad esempio tracce e SMPTE, possono causare un comportamento erre della barra degli strumenti. Per questi formati di ora, è possibile disattivare la barra degli strumenti specificando lo stile della finestra MCIWNDF NOPLAYBAR durante la creazione di \_ una finestra MCIWnd.

 

 

 




