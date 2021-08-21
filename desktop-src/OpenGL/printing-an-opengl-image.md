---
title: Stampa di un'immagine OpenGL
description: È possibile stampare immagini OpenGL di cui è stato eseguito il rendering in metafile migliorati.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL su Windows,stampa
- stampa di immagini OpenGL OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d5cb2e08a247ad8ebd5d333a8a680b57e38a3fc1a9c2281dfb2bd8671f4c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117980705"
---
# <a name="printing-an-opengl-image"></a>Stampa di un'immagine OpenGL

È possibile stampare immagini OpenGL di cui è stato eseguito il rendering in metafile migliorati. Quando si esegue il rendering in un dispositivo di stampa (HDC), deve essere supportato da uno spooler di metafile. OpenGL usa la memoria per profondità, colore e altri buffer per archiviare l'output grafico in una stampante. Poiché la risoluzione tipica della stampante richiede una quantità significativa di memoria per archiviare l'output grafico, la stampa di un'immagine OpenGL potrebbe richiedere più memoria di quella disponibile nel sistema. Per superare questa limitazione, l'implementazione corrente di OpenGL stampa grafica OpenGL in bande. Tuttavia, ciò aumenta il tempo necessario per stampare le immagini OpenGL.

Prima di stampare un'immagine OpenGL, è necessario chiamare la funzione [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) per completare l'inizializzazione di un contesto di dispositivo della stampante. Dopo aver **chiamato StartDoc,** è possibile creare contesti di rendering (HGLRC) per il rendering nel dispositivo stampante. Se si creano contesti di rendering prima di **chiamare StartDoc,** non è possibile determinare se è in corso lo spooling di un metafile.

L'esempio di codice seguente illustra come stampare un'immagine OpenGL:

``` syntax
HDC            hDC;
DOCINFO        di;
HGLRC          hglrc;

// Call StartDoc to start the document 
StartDoc( hDC, &di );

// Prepare the printer driver to accept data 
StartPage(hDC);

// Create a rendering context using the metafile DC 
hglrc = wglCreateContext ( hDCmetafile );

// Do OpenGL rendering operations here 
    . . .
wglMakeCurrent(NULL, NULL); // Get rid of rendering context 
    . . .
EndPage(hDC); // Finish writing to the page 
EndDoc(hDC); // End the print job
```

Per altre informazioni sull'uso dei metafile, vedere [Operazioni avanzate sui metafile.](/windows/desktop/gdi/enhanced-metafile-operations)

 

 