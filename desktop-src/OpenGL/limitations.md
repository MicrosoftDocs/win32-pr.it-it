---
title: Limitazioni
description: Limitazioni
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL in Windows,limitazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d058570c049f471dcf6e92c4eb55eb1365948d581127c68a46deb8d863ccc34d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937418"
---
# <a name="limitations"></a>Limitazioni

L'implementazione generica presenta le limitazioni seguenti:

-   Stampa.

    È possibile stampare un'immagine OpenGL direttamente su una stampante usando solo metafile. Per altre informazioni, vedere [Stampa di un'immagine OpenGL.](printing-an-opengl-image.md)

-   Gli elementi grafici OpenGL e GDI non possono essere misti in una finestra con doppio buffer.

    Un'applicazione può disegnare direttamente grafica OpenGL e grafica GDI in una finestra a buffer singolo, ma non in una finestra a doppio buffer.

-   Non sono disponibili tavolozze colori hardware per finestra.

    Windows dispone di una singola tavolozza dei colori hardware di sistema, che si applica all'intero schermo. Una finestra OpenGL non può avere un proprio riquadro hardware, ma può avere un proprio riquadro logico. A tale scopo, deve diventare un'applicazione in grado di riconoscere il riquadro. Per altre informazioni, vedere [Modalità colori OpenGL e gestione Windows tavolozza](opengl-color-modes-and-windows-palette-management.md).

-   Non è disponibile alcun supporto diretto per Gli Appunti, DDE (Dynamic Data Exchange) o OLE.

    Una finestra con grafica OpenGL non supporta direttamente queste Windows funzionalità. Esistono tuttavia soluzioni alternative per l'uso degli Appunti. Per altre informazioni, vedere [Copia di un'immagine OpenGL negli Appunti.](copying-an-opengl-image-to-the-clipboard.md)

-   La libreria di classi C++ di Inventor 2.0 non è inclusa.

    La libreria di classi di Inventor, basata su OpenGL, fornisce costrutti di livello superiore per la programmazione di grafica 3D. Non è incluso nella versione corrente dell'implementazione microsoft di OpenGL per Windows.

-   Non è disponibile alcun supporto per le funzionalità di formato pixel seguenti: immagini stereoscopiche, bitplani alfa e buffer ausiliari.

    È tuttavia disponibile il supporto per diversi buffer accessori, tra cui buffer di stencil, buffer di accumulo, buffer nascosto (doppio buffer), buffer del piano di sovrapposizione e sottostante e buffer di profondità (asse z).

 

 




