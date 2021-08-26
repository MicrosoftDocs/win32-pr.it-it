---
title: Front, back e altri buffer
description: OpenGL archivia e modifica i dati pixel in un framebuffer.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL in Windows,buffer
- framebuffer OpenGL
- buffer di colore OpenGL
- buffer di profondità OpenGL
- buffer di accumulo OpenGL
- Buffer di stencil OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd64f980aad1df8576accd8c37d19521a5368e1fe295393d54c2836f2db8566
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082321"
---
# <a name="front-back-and-other-buffers"></a>Front, back e altri buffer

OpenGL archivia e modifica i dati pixel in un framebuffer. Il framebuffer è costituito da un set di buffer logici: colore, profondità, accumulo e buffer di stencil. Il buffer dei colori stesso è costituito da un set di buffer logici. questo set può includere un front-left, un front-right, un back-left, un back-right e un certo numero di buffer ausiliari. Un particolare formato pixel o un'implementazione OpenGL potrebbe non fornire tutti questi buffer. Ad esempio, la versione corrente dell'implementazione microsoft di OpenGL in Windows non supporta immagini stereoscopiche, pertanto un formato pixel non può avere buffer di colore sinistro e destro. Inoltre, la versione corrente non supporta i buffer ausiliari. Per altre informazioni sui buffer OpenGL e sulle funzioni OpenGL che operano su di essi, vedere il manuale di riferimento *di OpenGL* e *openGL Programming Guide*.

L'implementazione microsoft di OpenGL in Windows supporta il doppio buffer delle immagini. Si tratta di una tecnica in cui un'applicazione disegna pixel in un buffer fuori schermo e quindi, quando l'immagine è pronta per la visualizzazione, copia il contenuto del buffer fuori schermo in un buffer su schermo. Il doppio buffer consente modifiche uniformi delle immagini, particolarmente importanti per le immagini animate.

Sono disponibili due buffer di colore per le applicazioni che usano il doppio buffer: un front buffer e un buffer nascosto. Per impostazione predefinita, i comandi di disegno vengono indirizzati al buffer nascosto (buffer fuori schermo), mentre il front buffer viene visualizzato sullo schermo. Quando il buffer fuori schermo è pronto per la visualizzazione, si chiama [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)e Windows copia il contenuto del buffer fuori schermo nel buffer su schermo.

L'implementazione generica usa una bitmap indipendente dal dispositivo (DIB) come buffer nascosto e la visualizzazione dello schermo come front buffer. I dispositivi hardware e i relativi driver possono usare approcci diversi.

Il doppio buffer è una proprietà in formato pixel. Per richiedere il doppio buffer per un formato pixel, impostare il flag PFD DOUBLEBUFFER nella struttura di dati \_ [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) in una chiamata a [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).

La funzione principale OpenGL, [**glDrawBuffer,**](gldrawbuffer.md)seleziona i buffer per la scrittura e la cancellazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni buffer](buffer-functions.md)
</dt> </dl>

 

 




