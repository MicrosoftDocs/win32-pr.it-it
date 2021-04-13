---
title: Selezione
description: Selection restituisce il contenuto corrente dello stack dei nomi, ovvero una matrice di nomi con valori interi.
ms.assetid: 66902d2c-0cd7-49b3-a685-5c0bdba0df1c
keywords:
- modalità di selezione OpenGL
- selezione riscontri OpenGL
- hit record OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851fac28cda979a383d183a12c79656bfebcbb0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330671"
---
# <a name="selection"></a>Selezione

Selection restituisce il contenuto corrente dello stack dei nomi, ovvero una matrice di nomi con valori interi. Assegnare i nomi e compilare lo stack dei nomi all'interno del codice di modellazione che specifica la geometria degli oggetti che si desidera creare. Quindi, in modalità di selezione, ogni volta che una primitiva interseca il volume di clip, si verifica un riscontro di selezione. Il record di hit, scritto nella matrice di selezione fornita con [**glSelectBuffer**](glselectbuffer.md), contiene informazioni sul contenuto dello stack dei nomi al momento del raggiungimento.

> [!Note]  
> Chiamare [**glSelectBuffer**](glselectbuffer.md) prima di inserire OpenGL in modalità di selezione con [**glRenderMode**](glrendermode.md). Non è garantito che l'intero contenuto dello stack dei nomi venga restituito fino a quando non si chiama **glRenderMode** per portare OpenGL fuori dalla modalità di selezione.

 

Modificare lo stack dei nomi con [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)e [**glPopName**](glpopname.md). È anche possibile usare [**gluPickMatrix**](glupickmatrix.md) per la selezione.

 

 




