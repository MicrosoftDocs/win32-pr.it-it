---
title: Trasformazioni di matrice
description: I vertici e le normali vengono trasformati dalle matrici di visualizzazione del modello e di proiezione prima di essere usati per produrre un'immagine nel framebuffer.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- pipeline di elaborazione OpenGL, matrici
- Matrici OpenGL
- matrice modelview
- matrice di proiezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e3c88ffcfebc989400cfa9a85c16f355c0a7090ff4d16531cf03c3697ee869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937320"
---
# <a name="matrix-transformations"></a>Trasformazioni di matrice

I vertici e le normali vengono trasformati dalle matrici di visualizzazione del modello e di proiezione prima di essere usati per produrre un'immagine nel framebuffer. Usare funzioni come [**glMatrixMode**](glmatrixmode.md), [ * *glMultMatrix \** _](glmultmatrix.md), [_*glRotate \**_](glrotate.md), [_*glTranslate \**_](gltranslate.md)e [_*glScale \**_](glscale.md) per comporre le trasformazioni desiderate. Oppure specificare direttamente le matrici [_*con glLoadMatrix \**_](glloadmatrix.md) e _ [*glLoadIdentity* *](glloadidentity.md). Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare matrici modelview e proiezione nei rispettivi stack.

 

 




