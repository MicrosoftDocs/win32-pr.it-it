---
title: Porting di applicazioni di sistema X Window
description: Porting di applicazioni di sistema X Window
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL per Windows, porting
- porting in OpenGL, X Window System
- Porting OpenGL, sistema X Window
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e52a06ffa458e07a70a7c4823e0291639d878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221527"
---
# <a name="porting-x-window-system-applications"></a>Porting di applicazioni di sistema X Window

Analogamente a Windows, il sistema X Window è un sistema basato su messaggi di gestione degli eventi che usa i controlli e i menu della finestra. Il codice OpenGL nell'applicazione di sistema X Window è probabilmente situato in aree che corrispondono approssimativamente al punto in cui verrà visualizzato quando lo si trasferisce a Windows. La maggior parte del codice OpenGL non cambia, ma è necessario riscrivere il codice specifico del sistema X Window.

**Utilizzare la seguente procedura generale per trasferire i programmi OpenGL di sistema X Window a Windows**

1.  Riscrivere il codice specifico del sistema X Window usando il codice di Windows equivalente. Individuare il codice per la creazione e la gestione degli eventi della finestra. Il sistema della finestra X e le finestre sono sistemi di gestione degli eventi, basati su messaggi, che semplificano la determinazione del punto in cui apportare le modifiche appropriate. Tuttavia, in particolare per le applicazioni di grandi dimensioni, la riscrittura di un'applicazione da un sistema operativo a un altro può essere un'impresa complessa e difficile.
2.  Individuare il codice che utilizza le funzioni GLX. Queste sono le funzioni che verranno convertite nelle funzioni Windows equivalenti.
3.  Trasla le funzioni di formato pixel GLX e funzioni visive/ridotte nel formato Windows/OpenGL pixel appropriato e nelle funzioni di contesto del dispositivo.
4.  Tradurre le funzioni del contesto di rendering GLX in funzioni di contesto di rendering Windows/OpenGL.
5.  Trasla le funzioni GLX pixmap in funzioni Windows equivalenti.
6.  Tradurre il framebuffer GLX e altre funzioni GLX nelle funzioni di Windows appropriate.

 

 




