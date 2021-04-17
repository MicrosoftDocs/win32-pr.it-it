---
title: Stampa di un'immagine OpenGL
description: È possibile stampare le immagini OpenGL sottoposte a rendering nei metafile avanzati.
ms.assetid: 6099cbe2-82f9-46ec-a3ca-74486c111639
keywords:
- OpenGL per Windows, stampa
- stampa di immagini OpenGL OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca0c5260a084796915a7564f793f0e252b5228c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300335"
---
# <a name="printing-an-opengl-image"></a>Stampa di un'immagine OpenGL

È possibile stampare le immagini OpenGL sottoposte a rendering nei metafile avanzati. Quando si esegue il rendering in un dispositivo di stampa (HDC), questo deve essere supportato da uno spooler del metafile. OpenGL usa memoria per la profondità, il colore e altri buffer per archiviare l'output grafico in una stampante. Poiché la risoluzione tipica della stampante richiede una quantità significativa di memoria per archiviare l'output della grafica, la stampa di un'immagine OpenGL potrebbe richiedere una quantità di memoria maggiore di quella disponibile nel sistema. Per ovviare a questa limitazione, l'implementazione corrente di OpenGL stampa le immagini OpenGL in bande. Tuttavia, questo aumenta il tempo necessario per stampare le immagini OpenGL.

Prima di stampare un'immagine OpenGL, è necessario chiamare la funzione [StartDoc](/windows/desktop/api/wingdi/nf-wingdi-startdoca) per completare l'inizializzazione di un contesto di dispositivo stampante (DC). Dopo aver chiamato **StartDoc**, è possibile creare contesti di rendering (HGLRC) per eseguire il rendering sul dispositivo di stampa. Se si creano contesti di rendering prima di chiamare **StartDoc**, non è possibile determinare se è stato eseguito lo spooling di un metafile.

Nell'esempio di codice seguente viene illustrato come stampare un'immagine OpenGL:

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

Per altre informazioni sull'uso dei metafile, vedere [operazioni Metafile avanzate](/windows/desktop/gdi/enhanced-metafile-operations).

 

 