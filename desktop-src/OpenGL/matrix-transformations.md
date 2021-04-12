---
title: Trasformazioni matrice
description: I vertici e le normali sono trasformati dalle matrici Modelview e projection prima di essere usati per produrre un'immagine nel framebuffer.
ms.assetid: 9fd0b236-9152-4494-b5c7-dadb5943269e
keywords:
- Pipeline di elaborazione OpenGL, matrici
- matrici OpenGL
- matrice Modelview
- matrice di proiezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db0ebd8bd13b8d2cee32b8873f697ab073140bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221330"
---
# <a name="matrix-transformations"></a>Trasformazioni matrice

I vertici e le normali sono trasformati dalle matrici Modelview e projection prima di essere usati per produrre un'immagine nel framebuffer. Usare funzioni come [**glMatrixMode**](glmatrixmode.md), [**glMultMatrix \***](glmultmatrix.md), [**glRotate \***](glrotate.md), [**glTranslate \***](gltranslate.md)e [**glScale \***](glscale.md) per comporre le trasformazioni desiderate. Oppure specificare matrici direttamente con [**glLoadMatrix \***](glloadmatrix.md) e [**glLoadIdentity**](glloadidentity.md). Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare Modelview e matrici di proiezione nei rispettivi stack.

 

 




