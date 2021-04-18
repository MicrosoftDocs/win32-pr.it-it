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
# <a name="porting-defs-binds-and-sets"></a><span data-ttu-id="4b979-118">Porting di defs, binding e set</span><span class="sxs-lookup"><span data-stu-id="4b979-118">Porting Defs, Binds, and Sets</span></span>

<span data-ttu-id="4b979-119">OpenGL non contiene tabelle di definizioni archiviate; non è possibile definire i modelli di illuminazione, il materiale, le trame, gli stili di linea o i modelli come oggetti separati come in IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="4b979-119">OpenGL doesn't have tables of stored definitions; you can't define lighting models, material, textures, line styles, or patterns as separate objects as you can in IRIS GL.</span></span> <span data-ttu-id="4b979-120">Quindi OpenGL non ha equivalenti diretti alle seguenti funzioni di IRIS GL:</span><span class="sxs-lookup"><span data-stu-id="4b979-120">Thus OpenGL has no direct equivalents to the following IRIS GL functions:</span></span>

-   <span data-ttu-id="4b979-121">**Imdef** e **imbind**</span><span class="sxs-lookup"><span data-stu-id="4b979-121">**Imdef** and **Imbind**</span></span>
-   <span data-ttu-id="4b979-122">**tevdef** e **tevbind**</span><span class="sxs-lookup"><span data-stu-id="4b979-122">**tevdef** and **tevbind**</span></span>
-   <span data-ttu-id="4b979-123">**textdef** e **textbind**</span><span class="sxs-lookup"><span data-stu-id="4b979-123">**textdef** and **textbind**</span></span>
-   <span data-ttu-id="4b979-124">**definestyle** e **Sestyle**</span><span class="sxs-lookup"><span data-stu-id="4b979-124">**definestyle** and **setstyle**</span></span>
-   <span data-ttu-id="4b979-125">**defpattern** e **sepattern**</span><span class="sxs-lookup"><span data-stu-id="4b979-125">**defpattern** and **setpattern**</span></span>

<span data-ttu-id="4b979-126">È possibile usare gli elenchi di visualizzazione OpenGL per simulare il meccanismo di definizione/binding IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="4b979-126">You can use OpenGL display lists to mimic the IRIS GL def/bind mechanism.</span></span> <span data-ttu-id="4b979-127">Ad esempio, di seguito viene illustrata una definizione di materiale in IRIS GL:</span><span class="sxs-lookup"><span data-stu-id="4b979-127">For example, here is a material definition in IRIS GL:</span></span>


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



<span data-ttu-id="4b979-128">Nell'esempio di codice OpenGL seguente viene definito lo stesso materiale in un elenco di visualizzazione a cui viene fatto riferimento dal numero di elenco definito da **materiali**.</span><span class="sxs-lookup"><span data-stu-id="4b979-128">The following OpenGL code sample defines the same material in a display list that is referred to by the list number defined by **MYMATERIAL**.</span></span>


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



 

 




