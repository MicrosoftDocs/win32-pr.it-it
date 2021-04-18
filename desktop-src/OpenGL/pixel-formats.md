---
title: Formati pixel
description: Formati pixel
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL per Windows, pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16f9f78edc0cf935fb602de8d88792091588ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298889"
---
# <a name="pixel-formats"></a>Formati pixel

Un *formato pixel* specifica diverse proprietà di una superficie di disegno OpenGL. Di seguito sono riportate alcune delle proprietà specificate da un formato pixel:

-   Indica se il buffer pixel è a buffer singolo o doppio.
-   Indica se i dati pixel sono in formato RGBA o di indice colore.
-   Numero di bit usati per archiviare i dati di colore.
-   Numero di bit utilizzati per il buffer di profondità (asse z).
-   Numero di bit utilizzati per il buffer dello stencil.
-   Numero di piani sovrapposti e sottoposti a sovrimpressione.
-   Diverse maschere di visibilità.

L'implementazione Microsoft di OpenGL per Windows usa la struttura dei dati [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) per trasferire i dati in formato pixel. I membri della struttura specificano le proprietà precedenti e altre ancora.

Un determinato contesto di dispositivo può supportare diversi formati pixel. Windows identifica i formati pixel supportati da un contesto di dispositivo con valori di indice consecutivi in base uno (1, 2, 3, 4 e così via). Un contesto di dispositivo può avere un solo formato pixel corrente, scelto dal set di formati pixel supportati.

Ogni finestra ha il proprio formato pixel corrente in OpenGL in Windows. Ciò significa, ad esempio, che un'applicazione può visualizzare contemporaneamente RGBA e le finestre OpenGL con indicizzazione dei colori, o finestre OpenGL con buffer singolo e doppio. Questa funzionalità di formato pixel per finestra è limitata alle finestre OpenGL.

In genere si ottiene un contesto di dispositivo, si imposta il formato pixel del contesto di dispositivo e quindi si crea un contesto di rendering OpenGL adatto per tale dispositivo.

> [!Note]  
> È possibile impostare il formato pixel prima di creare un contesto di rendering perché il contesto di rendering eredita il formato pixel del contesto di dispositivo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni in formato pixel](pixel-format-functions.md)
</dt> </dl>

 

 




