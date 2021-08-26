---
title: Porting X Window System Applications
description: Porting X Window System Applications
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL in Windows, porting
- porting in OpenGL,X Window System
- Porting OpenGL,X Window System
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07a20de68df3806da40629252246f176beece0a4c3951180d484d9fadc6b325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034761"
---
# <a name="porting-x-window-system-applications"></a>Porting X Window System Applications

Come Windows, X Window System è un sistema basato su messaggi e di gestione degli eventi che usa i controlli finestra e i menu. Il codice OpenGL nell'applicazione X Window System si trova probabilmente in aree che corrispondono approssimativamente alla posizione in cui verrà visualizzato quando lo si esegue il port Windows. La maggior parte del codice OpenGL non cambia, ma è necessario riscrivere il codice specifico di X Window System.

**Usare la procedura generale seguente per eseguire il port dei programmi OpenGL di X Window System Windows**

1.  Riscrivere il codice specifico di X Window System usando codice Windows codice. Individuare il codice di creazione della finestra e di gestione degli eventi. X Window System e Windows sono sistemi di windowing basati su messaggi e di gestione degli eventi, che semplificano la determinazione della posizione in cui apportare le modifiche appropriate. Tuttavia, soprattutto per le applicazioni di grandi dimensioni, la riscrittura di un'applicazione da un sistema operativo a un altro può essere un'impresa complessa e difficile.
2.  Individuare il codice che usa le funzioni GLX. Queste sono le funzioni che verranno convertite nelle funzioni Windows equivalenti.
3.  Convertire le funzioni in formato pixel GLX e le funzioni Visual/Drawable Windows formato pixel/OpenGL e le funzioni del contesto di dispositivo appropriate.
4.  Convertire le funzioni di contesto di rendering GLX in Windows di contesto di rendering OpenGL/OpenGL.
5.  Convertire le funzioni GLX Pixmap in funzioni di Windows equivalenti.
6.  Convertire glX framebuffer e altre funzioni GLX nelle funzioni Windows appropriate.

 

 




