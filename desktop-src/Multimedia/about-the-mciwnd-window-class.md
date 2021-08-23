---
title: Informazioni sulla classe della finestra MCIWnd
description: Informazioni sulla classe della finestra MCIWnd
ms.assetid: 7dde7346-5853-4c8f-8788-bf74d01ece83
keywords:
- Classe di finestra MCIWnd, informazioni
- McIWndCreate - funzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07a75f9798c1bfe0ec4f67da0f990018143efd0285541b49a9035b9749a36de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065661"
---
# <a name="about-the-mciwnd-window-class"></a>Informazioni sulla classe della finestra MCIWnd

La classe McIWnd Window è facile da usare. Usando una singola funzione, [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) l'applicazione può creare un controllo che riproduce qualsiasi dispositivo che usa l'interfaccia di controllo multimediale (MCI). Questi dispositivi includono audio CD, audio waveform, MIDI e video.

L'automazione della riproduzione è anche rapida e semplice. Usando una sola funzione e due macro, un'applicazione può creare una finestra MCIWnd con il dispositivo multimediale appropriato, riprodurre il dispositivo e chiudere sia il dispositivo che la finestra al termine della riproduzione del contenuto.

> [!Note]  
> Alcuni dispositivi riproducino contenuto archiviato in file. Altri dispositivi, ad esempio i dispositivi audio CD, riproduceno il contenuto archiviato in un altro supporto. Per maggiore chiarezza, questa panoramica si riferisce a entrambe le circostanze come "riproduzione del dispositivo".

 

 

 




