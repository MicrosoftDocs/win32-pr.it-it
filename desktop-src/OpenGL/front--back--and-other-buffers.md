---
title: Front, back e altri buffer
description: OpenGL archivia e modifica i dati pixel in un framebuffer.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL per Windows, buffer
- framebuffer OpenGL
- buffer dei colori OpenGL
- buffer di profondità OpenGL
- buffer di accumulo OpenGL
- buffer di stencil OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea487b73af356853bee2054db292cdfe740bd16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396250"
---
# <a name="front-back-and-other-buffers"></a>Front, back e altri buffer

OpenGL archivia e modifica i dati pixel in un framebuffer. Il framebuffer è costituito da un set di buffer logici: i buffer di colore, profondità, accumulo e stencil. Il buffer dei colori è costituito da un set di buffer logici; Questo set può includere un front-left, un front-right, un back-left, un back-right e un certo numero di buffer ausiliari. Un particolare formato pixel o un'implementazione OpenGL non può fornire tutti questi buffer. La versione corrente dell'implementazione di Microsoft OpenGL in Windows, ad esempio, non supporta le immagini stereoscopiche, quindi un formato pixel non può avere buffer di colore sinistro e destro. Inoltre, la versione corrente non supporta i buffer ausiliari. Per altre informazioni sui buffer OpenGL e sulle funzioni OpenGL che operano su di essi, vedere il *Manuale di riferimento per OpenGL* e la guida per *programmatori OpenGL*.

L'implementazione Microsoft di OpenGL in Windows supporta il doppio buffering delle immagini. Si tratta di una tecnica in cui un'applicazione disegna i pixel in un buffer fuori schermo, quindi, quando l'immagine è pronta per la visualizzazione, copia il contenuto del buffer fuori schermo in un buffer a schermo intero. Il doppio buffer consente di apportare modifiche alle immagini, che sono particolarmente importanti per le immagini animate.

Due buffer a colori sono disponibili per le applicazioni che usano il doppio buffer: un buffer anteriore e un buffer nascosto. Per impostazione predefinita, i comandi di disegno vengono indirizzati al buffer nascosto (il buffer fuori schermo), mentre il buffer anteriore viene visualizzato sullo schermo. Quando il buffer fuori schermo è pronto per la visualizzazione, si chiama [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)e Windows copia il contenuto del buffer fuori schermo nel buffer sullo schermo.

L'implementazione generica usa una bitmap indipendente dal dispositivo (DIB) come buffer nascosto e lo schermo viene visualizzato come buffer anteriore. I dispositivi hardware e i relativi driver possono utilizzare approcci diversi.

Il doppio buffer è una proprietà in formato pixel. Per richiedere il doppio buffering per un formato pixel, impostare il \_ flag PFD DOUBLEBUFFER nella struttura dei dati [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) in una chiamata a [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).

La funzione di base OpenGL, [**glDrawBuffer**](gldrawbuffer.md), seleziona i buffer per la scrittura e la cancellazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni buffer](buffer-functions.md)
</dt> </dl>

 

 




