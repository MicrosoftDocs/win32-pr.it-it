---
title: Porting di defs, binding e set
description: Porting di defs, binding e set
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- Porting di IRIS GL, definizioni
- porting da IRIS GL, definizioni
- porting in OpenGL da IRIS GL, definizioni
- Porting OpenGL da IRIS GL, definizioni
- Porting, binding di IRIS GL
- porting da IRIS GL, binding
- porting in OpenGL da IRIS GL, binding
- Porting OpenGL da IRIS GL, binding
- Porting di IRIS GL, set
- porting da IRIS GL, set
- porting in OpenGL da IRIS GL, set
- Porting OpenGL da IRIS GL, set
- definitions
- associa
- Imposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f9a88253390ee99f5b5870fd7a09e272f1c549
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297858"
---
# <a name="porting-defs-binds-and-sets"></a>Porting di defs, binding e set

OpenGL non contiene tabelle di definizioni archiviate; non è possibile definire i modelli di illuminazione, il materiale, le trame, gli stili di linea o i modelli come oggetti separati come in IRIS GL. Quindi OpenGL non ha equivalenti diretti alle seguenti funzioni di IRIS GL:

-   **Imdef** e **imbind**
-   **tevdef** e **tevbind**
-   **textdef** e **textbind**
-   **definestyle** e **Sestyle**
-   **defpattern** e **sepattern**

È possibile usare gli elenchi di visualizzazione OpenGL per simulare il meccanismo di definizione/binding IRIS GL. Ad esempio, di seguito viene illustrata una definizione di materiale in IRIS GL:


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



Nell'esempio di codice OpenGL seguente viene definito lo stesso materiale in un elenco di visualizzazione a cui viene fatto riferimento dal numero di elenco definito da **materiali**.


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



 

 




