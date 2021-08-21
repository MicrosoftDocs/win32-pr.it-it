---
title: Porting di def, associazioni e set
description: Porting di def, associazioni e set
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- portabilità IRIS GL, definizioni
- porting from IRIS GL,definitions
- porting to OpenGL from IRIS GL,definitions
- Portabilità OpenGL da IRIS GL, definizioni
- portabilità IRIS GL, binding
- porting from IRIS GL,binds
- porting to OpenGL from IRIS GL,binds
- Portabilità OpenGL da IRIS GL, binding
- portabilità IRIS GL, set
- porting from IRIS GL,sets
- porting to OpenGL from IRIS GL,sets
- Portabilità OpenGL da IRIS GL,set
- definitions
- Lega
- Imposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a4c3776d3e5eb8000a4e81578bb5df95658a37e0793944a9cda6923fc7a2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132663"
---
# <a name="porting-defs-binds-and-sets"></a>Porting di def, associazioni e set

OpenGL non dispone di tabelle di definizioni archiviate. Non è possibile definire modelli di illuminazione, materiali, trame, stili di linea o modelli come oggetti separati come in IRIS GL. OpenGL non ha quindi equivalenti diretti alle funzioni IRIS GL seguenti:

-   **Imdef** e **Imbind**
-   **tevdef** e **tevbind**
-   **textdef** e **textbind**
-   **definestyle** e **setstyle**
-   **defpattern** e **setpattern**

È possibile usare gli elenchi di visualizzazione OpenGL per simulare il meccanismo di def/binding IRIS GL. Ecco, ad esempio, una definizione materiale in IRIS GL:


```C++
float mat() = { 
    AMBIENT, .1, .1, .1, 
    DIFFUSE, 0, .369, .165, 
    SPECULAR, .5, .5, .5, 
    SHININESS, 10, 
    LMNULL 
}; 
lmdef(DEFMATERIAL, 1, 0, mat); 
lmbind(MATERIAL, 1);
```



L'esempio di codice OpenGL seguente definisce lo stesso materiale in un elenco di visualizzazione a cui fa riferimento il numero di elenco definito da **MYMATERIAL.**


```C++
#define MYMATERIAL 10 
 
GLfloat        mat_amb[] = {.1, .1, .1, 1.0}; 
GLfloat        mat_dif[] = {0, .369, .165, 1.0}; 
GLfloat        mat_spec[] = {.5, .5, .5, 1.0}; 
 
glNewList(MYMATERIAL, GL_COMPILE); 
    glMaterialfv(GL_FRONT, GL_AMBIENT, mat_amb); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_dif); 
    glMaterialfv(GL_FRONT, GL_SHININESS, 10); 
glEndList(); 
 
glCallList( MYMATERIAL );
```



 

 




