---
title: Porting del codice in modalità MSINGLE
description: OpenGL non ha un equivalente per la modalità MSINGLE, a matrice singola.
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- Porting di IRIS GL, modalità MSINGLE
- porting da IRIS GL, modalità MSINGLE
- porting in OpenGL da IRIS GL, modalità MSINGLE
- Porting OpenGL da IRIS GL, modalità MSINGLE
- Modalità MSINGLE
- Porting di IRIS GL, modalità a matrice singola
- porting da IRIS GL, modalità a matrice singola
- porting in OpenGL da IRIS GL, modalità a matrice singola
- Porting OpenGL da IRIS GL, modalità a matrice singola
- modalità a matrice singola
- modalità a doppia matrice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b8c62f93fa8e027dd1c91ca0bd40bc8e6ffaf9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396338"
---
# <a name="porting-msingle-mode-code"></a>Porting del codice in modalità MSINGLE

OpenGL non ha un equivalente per la modalità **MSINGLE**, a matrice singola. Anche se l'uso di questa modalità è stato sconsigliato, è l'impostazione predefinita per IRIS GL. Se il programma IRIS GL usa la modalità a matrice singola, è necessario riscriverlo per usare solo la modalità a matrice doppia. OpenGL è sempre in modalità a doppia matrice ed è inizialmente in modalità GL \_ MODELVIEW.

La maggior parte del codice IRIS GL in modalità MSINGLE è simile a quanto segue:

``` syntax
projectionmatrix();
```

dove *ProjectionMatrix* è uno dei seguenti: **Ortho**, **ortho2**, **Perspective** o **Window**. Per eseguire la porta in OpenGL, sostituire la funzione *ProjectionMatrix* in modalità **MSINGLE** con:


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




