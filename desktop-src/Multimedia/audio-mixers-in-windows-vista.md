---
title: Mixer audio in Windows Vista
description: Mixer audio in Windows Vista
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- audio multimediale, mixer audio di Windows Vista
- audio, mixer audio di Windows Vista
- mixer audio, Windows Vista
- mixer, Windows Vista
- Mixer audio di Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104560859"
---
# <a name="audio-mixers-in-windows-vista"></a>Mixer audio in Windows Vista

A partire da Windows Vista, alcuni controlli mixer sono implementati nel software anziché nell'hardware. I controlli volume, ad esempio, vengono implementati mediante l'API di sessione audio di Windows (WASAPI). Questi controlli non influiscono direttamente sulle impostazioni hardware. Inoltre, sono associati a una sessione audio specifica del processo, quindi le modifiche interessano l'applicazione chiamante, ma non influiscono sulle altre applicazioni.

Ogni dispositivo dell'endpoint audio ha un layout di mixer standard, implementato nel software.

-   Ogni endpoint di rendering audio contiene una riga di destinazione che contiene gli elementi seguenti:
    -   Controllo volume
    -   Disattiva controllo
    -   Origine riga: waveform-output audio.
    -   Riga di origine: CD audio.
-   Ogni endpoint di acquisizione audio contiene una riga di destinazione che contiene gli elementi seguenti:
    -   Controllo volume
    -   Disattiva controllo
    -   Riga di origine: input audio. Il tipo di componente dipende dal dispositivo di input, ad esempio un microfono.

Ogni riga di codice sorgente contiene un controllo del volume e un controllo di silenziamento. Il diagramma seguente illustra i componenti degli endpoint di rendering e degli endpoint di acquisizione.

![layout mixer predefiniti](images/mixer1.gif)

Tutti i controlli per un endpoint modificano lo stesso controllo software sottostante. Se pertanto si modificano le impostazioni in un controllo, si riceverà una notifica di modifica del controllo sugli altri controlli. (Vedere la pagina relativa alla [**\_ \_ \_ modifica del controllo MIXM mm**](mm-mixm-control-change.md)).

Questo layout standard viene fornito per la compatibilità con le applicazioni esistenti che usano le funzioni del mixer audio. Le nuove applicazioni devono evitare di usare queste funzioni.

 

 




