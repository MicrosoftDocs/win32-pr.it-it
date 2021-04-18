---
title: Porting degli elenchi di visualizzazione modificati
description: Sebbene non sia possibile modificare gli elenchi di visualizzazione OpenGL, è possibile ottenere risultati simili nidificando gli elenchi di visualizzazione e quindi eliminando e creando nuove versioni dei sottoelenchi.
ms.assetid: b7f7ffed-c3de-43d4-bff2-f244faa3a27a
keywords:
- Porting di IRIS GL, elenchi di visualizzazione
- porting da IRIS GL, elenchi di visualizzazione
- porting in OpenGL da IRIS GL, elenchi di visualizzazione
- Porting OpenGL da IRIS GL, elenchi di visualizzazione
- visualizzare elenchi, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5555c850d4695ba3732b61c0a41b7aedd8af0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298547"
---
# <a name="porting-edited-display-lists"></a>Porting degli elenchi di visualizzazione modificati

Sebbene non sia possibile modificare gli elenchi di visualizzazione OpenGL, è possibile ottenere risultati simili nidificando gli elenchi di visualizzazione e quindi eliminando e creando nuove versioni dei sottoelenchi. Ad esempio:

``` syntax
glNewList (1, GL_COMPILE); 
    glIndexi(MY_RED); 
glEndlist(); 
 
glNewList(2, GL_COMPILE); 
    glScalef(1.2, 1.2, 1.0); 
glEndList(); 
 
glNewList(3, GL_COMPILE); 
    glCallList(1); 
    glCallList(2); 
glEndList(); 
 
glDeleteLists(1, 2); 
glNewList(1, GL_COMPILE); 
    glIndexi(MY_CYAN); 
glEndList(); 
glNewList(2, GL_COPILE); 
    glScalef(0.5, 0.5, 1.0); 
glEndList;
```

 

 




