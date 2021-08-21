---
title: Trasformazione delle coordinate
description: La libreria di utilità OpenGL (GLU) fornisce diverse funzioni di trasformazione di matrici di uso comune.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- Utilità OpenGL (GLU), funzioni di trasformazione matrice
- GLU (utilità OpenGL), funzioni di trasformazione matrice
- Funzioni di trasformazione matrice OpenGL
- Utilità OpenGL (GLU), trasformazione delle coordinate
- GLU (utilità OpenGL), trasformazione delle coordinate
- trasformazione di coordinate OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3c2e4f8c0dd9540e8ba7963640072ebf44997cf9d99e807f31914ddf8eed4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553571"
---
# <a name="transforming-coordinates"></a>Trasformazione delle coordinate

La libreria di utilità OpenGL (GLU) fornisce diverse funzioni di trasformazione di matrici di uso comune. È possibile configurare un'area di visualizzazione ortogonale bidimensionale con [**gluOrtho2D,**](gluortho2d.md)un volume di visualizzazione prospettica standard usando [**gluPerspective**](gluperspective.md)o un volume di visualizzazione centrato su un punto di vista specificato con [**gluLookAt.**](glulookat.md) Ognuna di queste funzioni crea la matrice desiderata e la applica alla matrice corrente [**usando glMultMatrix**](glmultmatrix.md).

La [**funzione gluPickMatrix**](glupickmatrix.md) semplifica la selezione di una matrice di selezione creando una matrice che limita il disegno a una piccola area del viewport. Se si esegue di nuovo il rendering della scena in modalità di selezione dopo l'applicazione di questa matrice, verranno selezionati tutti gli oggetti che verrebbero disegnati accanto al cursore e le relative informazioni verranno archiviate nel buffer di selezione. Per altre informazioni sulla modalità di selezione, vedere "Performing Selection and Feedback" [Performing Selection and Feedback](performing-selection-and-feedback.md).

Per determinare dove viene disegnato un oggetto nella finestra, usare [**gluProject**](gluproject.md), che converte le coordinate dell'oggetto specificate *objx*, *objy* e *objz* in coordinate della finestra usando *modelMatrix*, *projMatrix* e *viewport*. Il risultato viene archiviato in *winx,* *winy* e *winz*. Se la funzione ha esito positivo, il valore restituito è GL \_ TRUE. Se la funzione ha esito negativo, il valore restituito è GL \_ FALSE.

La [**funzione gluUnProject**](gluunproject.md) esegue la conversione inversa: trasforma le coordinate della finestra *specificate winx*, *winy* e *winz* in coordinate dell'oggetto usando *modelMatrix*, *projMatrix* e *viewport*. Il risultato viene archiviato in *objx*, *objy* e *objz*. Se la funzione ha esito positivo, il valore restituito è GL \_ TRUE. Se la funzione ha esito negativo, il valore restituito è GL \_ FALSE.

 

 




