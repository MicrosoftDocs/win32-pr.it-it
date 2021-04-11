---
title: Uso di oggetti mosaico
description: Poiché viene descritto un poligono complesso e tassellati, sono necessari dati associati, ad esempio i vertici, i bordi e le funzioni di callback.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- Utilità OpenGL (GLU), oggetti a mosaico
- GLU (utilità OpenGL), oggetti a mosaico
- oggetti a mosaico OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590ab571e656fcd346da265bfa921cb965fdf540
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329196"
---
# <a name="using-tessellation-objects"></a>Uso di oggetti mosaico

Poiché viene descritto un poligono complesso e tassellati, sono necessari dati associati, ad esempio i vertici, i bordi e le funzioni di callback. Tutti questi dati sono associati a un singolo oggetto a mosaico. Per conteggiarla suddividerla un poligono, è necessario innanzitutto usare la funzione [**gluNewTess**](glunewtess.md) che crea un nuovo oggetto a mosaico e restituisce un puntatore. Se la funzione ha esito negativo, viene restituito un puntatore null.

Se un oggetto a mosaico non è più necessario, è possibile eliminarlo e liberare tutta la memoria associata con [**gluDeleteTess**](gludeletetess.md).

È possibile riutilizzare un unico oggetto a mosaico per tutti i tassellature. Questo oggetto è necessario solo perché le funzioni di libreria potrebbero dover eseguire la propria tassellature e devono essere in grado di eseguire questa operazione senza interferire con i mosaico eseguiti dal programma. Sono inoltre utili più oggetti a mosaico se si desidera utilizzare set di callback diversi per tassellature diversi. In genere, tuttavia, si alloca un singolo oggetto a mosaico e lo si usa per tutti tassellature. Non è necessario liberarlo, perché usa una piccola quantità di memoria. D'altra parte, se si sta scrivendo una funzione di libreria che usa il mosaico di GLU, prestare attenzione a liberare tutti gli oggetti a mosaico creati.

 

 




