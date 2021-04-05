---
title: Trasformazione delle coordinate
description: La libreria di utilità OpenGL (GLU) fornisce diverse funzioni di trasformazione della matrice comunemente utilizzate.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- Utilità OpenGL (GLU), funzioni di trasformazione matrice
- GLU (utilità OpenGL), funzioni di trasformazione matrice
- funzioni di trasformazione matrice OpenGL
- Utilità OpenGL (GLU), trasformazione delle coordinate
- GLU (utilità OpenGL), trasformazione delle coordinate
- trasformazione di coordinate OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713936"
---
# <a name="transforming-coordinates"></a>Trasformazione delle coordinate

La libreria di utilità OpenGL (GLU) fornisce diverse funzioni di trasformazione della matrice comunemente utilizzate. È possibile configurare un'area di visualizzazione ortogonale bidimensionale con [**gluOrtho2D**](gluortho2d.md), un volume di visualizzazione prospettico standard usando [**gluPerspective**](gluperspective.md)o un volume di visualizzazione centrato su un osservazione specificato con [**gluLookAt**](glulookat.md). Ognuna di queste funzioni crea la matrice desiderata e la applica alla matrice corrente usando [**glMultMatrix**](glmultmatrix.md).

La funzione [**gluPickMatrix**](glupickmatrix.md) semplifica la selezione di una matrice di selezione creando una matrice che limita il disegno a una piccola area del viewport. Se si esegue nuovamente il rendering della scena in modalità di selezione dopo che questa matrice è stata applicata, verranno selezionati tutti gli oggetti che verranno disegnati accanto al cursore e le relative informazioni verranno archiviate nel buffer di selezione. Per ulteriori informazioni sulla modalità di selezione, vedere l'argomento relativo all'esecuzione di selezioni e commenti [e suggerimenti](performing-selection-and-feedback.md).

Per determinare la posizione della finestra in cui viene disegnato un oggetto, usare [**gluProject**](gluproject.md), che converte le coordinate dell'oggetto specificato *objX*, *objy* e *objz* in coordinate della finestra usando *modelMatrix*, *projMatrix* e *viewport*. Il risultato viene archiviato in *Winx*, *vinoso* e *Winz*. Se la funzione ha esito positivo, il valore restituito è GL \_ true. Se la funzione ha esito negativo, il valore restituito è GL \_ false.

La funzione [**gluUnProject**](gluunproject.md) esegue la conversione inversa: trasforma la finestra specificata le coordinate *Winx*, *vinoso* e *Winz* nelle coordinate dell'oggetto usando *modelMatrix*, *projMatrix* e *viewport*. Il risultato viene archiviato in *objX*, *objy* e *objz*. Se la funzione ha esito positivo, il valore restituito è GL \_ true. Se la funzione ha esito negativo, il valore restituito è GL \_ false.

 

 




