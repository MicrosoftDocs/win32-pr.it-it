---
title: Modifica delle immagini per l'uso nella texturing
description: La libreria dell'utilità OpenGL (GLU) offre funzioni di ridimensionamento delle immagini e mipmapping automatico per semplificare la specifica delle immagini di trama.
ms.assetid: 20edf665-1fed-4761-b8b1-beee02c78b0d
keywords:
- Utilità OpenGL (GLU), ridimensionamento delle immagini
- GLU (utilità OpenGL), ridimensionamento delle immagini
- Utilità OpenGL (GLU), mipmapping automatico
- GLU (Utilità OpenGL), mipmapping automatico
- Utilità OpenGL (GLU), immagini di trama
- GLU (utilità OpenGL), immagini di trama
- libreria GLU, immagini di trama
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dbe948dc3dbe84c9c2e89e02a43b45cf22d34af0198e422a883afd8f3384606
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553911"
---
# <a name="manipulating-images-for-use-in-texturing"></a>Modifica delle immagini per l'uso nella texturing

La libreria dell'utilità OpenGL (GLU) offre funzioni di ridimensionamento delle immagini e mipmapping automatico per semplificare la specifica delle immagini di trama. La [**funzione gluScaleImage**](gluscaleimage.md) ridimensiona un'immagine specificata in base a una dimensione di trama accettata. è possibile passare l'immagine risultante a OpenGL come trama. Le funzioni di mipmapping automatico, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) e [**gluBuild2DMipmaps,**](glubuild2dmipmaps.md)creano immagini di trama mipmapped da un'immagine specificata e le passano rispettivamente a [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D.**](glteximage2d.md)

 

 




