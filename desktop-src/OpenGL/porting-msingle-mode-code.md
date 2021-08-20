---
title: Porting del codice in modalità MSINGLE
description: OpenGL non ha alcun equivalente per la modalità a matrice singola MSINGLE.
ms.assetid: 7de933b8-150c-432d-89ee-5f5799ad8443
keywords:
- Porting IRIS GL, modalità MSINGLE
- porting da IRIS GL, modalità MSINGLE
- porting a OpenGL da IRIS GL, modalità MSINGLE
- Porting OpenGL da IRIS GL, modalità MSINGLE
- Modalità MSINGLE
- Porting IRIS GL, modalità a matrice singola
- porting da IRIS GL, modalità a matrice singola
- porting a OpenGL da IRIS GL, modalità a matrice singola
- Porting OpenGL da IRIS GL, modalità a matrice singola
- modalità a matrice singola
- modalità a matrice doppia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83716cead9134ba7823f4206fb6479d323bd35bddee480e9353a7ceb9aad38ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132390"
---
# <a name="porting-msingle-mode-code"></a>Porting del codice in modalità MSINGLE

OpenGL non ha alcun equivalente per **MSINGLE,** modalità a matrice singola. Anche se l'uso di questa modalità è stato sconsigliato, è l'impostazione predefinita per IRIS GL. Se il programma IRIS GL usa la modalità a matrice singola, è necessario riscriverla per usare solo la modalità a matrice doppia. OpenGL è sempre in modalità a matrice doppia e inizialmente è in \_ modalità GL MODELVIEW.

La maggior parte del codice GL IRIS in modalità MSINGLE è simile alla seguente:

``` syntax
projectionmatrix();
```

dove *projectionmatrix* è uno dei seguenti: **ortho**, **ortho2**, **perspective** o **window**. Per eseguire la porta a OpenGL, sostituire la funzione *projectionmatrix* **MSINGLE** -mode con:


```C++
glMatrixMode( GL_PROJECTION ); 
glLoadMatrix( identity matrix ); 
 
/* call one of these functions here: */ 
/* glFrustrum(), glOrtho(), glOrtho2(), gluPerspective()}; */ 
 
glMatrixMode( GL_MODELVIEW ); 
glLoadMatrix( identity matrix );
```



 

 




