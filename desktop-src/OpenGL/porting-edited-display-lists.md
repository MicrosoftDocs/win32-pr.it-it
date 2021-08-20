---
title: Porting Edited Display Lists
description: Anche se non è possibile modificare gli elenchi di visualizzazione OpenGL, è possibile ottenere risultati simili annidando gli elenchi di visualizzazione e quindi creando nuove versioni degli elenchi secondari.
ms.assetid: b7f7ffed-c3de-43d4-bff2-f244faa3a27a
keywords:
- Porting IRIS GL, elenchi di visualizzazione
- porting da IRIS GL,visualizzare elenchi
- porting a OpenGL da IRIS GL, visualizzazione di elenchi
- Porting OpenGL da IRIS GL, visualizzazione di elenchi
- elenchi di visualizzazione, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13f1630b0560091482d47f85e038d908dcfab202ae772c4d35dc388324b46075
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485581"
---
# <a name="porting-edited-display-lists"></a>Porting Edited Display Lists

Anche se non è possibile modificare gli elenchi di visualizzazione OpenGL, è possibile ottenere risultati simili annidando gli elenchi di visualizzazione e quindi creando nuove versioni degli elenchi secondari. Ad esempio:

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

 

 




