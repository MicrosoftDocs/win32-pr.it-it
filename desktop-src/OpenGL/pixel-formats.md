---
title: Formati pixel
description: Formati pixel
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL su Windows,pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbcd49b17c298d00d0ab41391172c8ae4c3bce8cb295db619d1c9787a2bca36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486191"
---
# <a name="pixel-formats"></a>Formati pixel

Un *formato pixel specifica* diverse proprietà di una superficie di disegno OpenGL. Alcune delle proprietà specificate da un formato pixel sono:

-   Indica se il buffer in pixel è a buffer singolo o doppio.
-   Indica se i dati in pixel sono in formato RGBA o con indice colore.
-   Numero di bit utilizzati per archiviare i dati relativi ai colori.
-   Numero di bit utilizzati per il buffer di profondità (asse z).
-   Numero di bit utilizzati per il buffer degli stencil.
-   Numero di piani sovrapposti e sottostanti.
-   Varie maschere di visibilità.

L'implementazione Microsoft di OpenGL per Windows usa la struttura dei dati [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) per trasmettere i dati in formato pixel. I membri della struttura specificano le proprietà precedenti e molte altre.

Un determinato contesto di dispositivo può supportare diversi formati di pixel. Windows identifica i formati pixel supportati da un contesto di dispositivo con valori di indice consecutivi in base uno (1, 2, 3, 4 e così via). Un contesto di dispositivo può avere un solo formato pixel corrente, scelto dal set di formati di pixel supportati.

Ogni finestra ha il proprio formato pixel corrente in OpenGL in Windows. Ciò significa, ad esempio, che un'applicazione può visualizzare contemporaneamente finestre OpenGL RGBA e con indice dei colori o finestre OpenGL a buffer singolo e doppio. Questa funzionalità di formato pixel per finestra è limitata alle finestre OpenGL.

In genere, si ottiene un contesto di dispositivo, si imposta il formato pixel del contesto di dispositivo e quindi si crea un contesto di rendering OpenGL adatto per tale dispositivo.

> [!Note]  
> Impostare il formato pixel prima di creare un contesto di rendering perché il contesto di rendering eredita il formato pixel del contesto di dispositivo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di formato pixel](pixel-format-functions.md)
</dt> </dl>

 

 




