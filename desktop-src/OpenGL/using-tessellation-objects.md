---
title: Uso di oggetti a tessellazione
description: Poiché un poligono complesso viene descritto e a tessellato, sono necessari dati associati, ad esempio vertici, bordi e funzioni di callback.
ms.assetid: b6102e25-280c-4d0d-9350-d0038d1a0306
keywords:
- Utilità OpenGL (GLU), oggetti a tessellazione
- GLU (utilità OpenGL), oggetti a tessellazione
- Oggetti a tessellazione OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efc2ca11fd037f79a88fed1568c97a24692060d723327cde0c8e8842ed21d084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011899"
---
# <a name="using-tessellation-objects"></a>Uso di oggetti a tessellazione

Poiché un poligono complesso viene descritto e a tessellato, sono necessari dati associati, ad esempio vertici, bordi e funzioni di callback. Tutti questi dati sono associati a un singolo oggetto a tassellamento. Per eseguire la tessellazione di un poligono, è prima di tutto necessario usare la funzione [**gluNewTess**](glunewtess.md) che crea un nuovo oggetto a tessellazione e restituisce un puntatore a esso. Se la funzione ha esito negativo, viene restituito un puntatore Null.

Se non è più necessario un oggetto a tassellamento, è possibile eliminarlo e liberare tutta la memoria associata [**con gluDeleteTess**](gludeletetess.md).

È possibile riutilizzare un singolo oggetto a tassellamento per tutte le tessellazioni. Questo oggetto è obbligatorio solo perché le funzioni di libreria potrebbero dover eseguire le proprie tessellazioni e dovrebbero essere in grado di eseguire questa operazione senza interferire con qualsiasi a tessellazione eseguita dal programma. Più oggetti a tessellazione sono utili anche se si vogliono usare set diversi di callback per diverse tessellazioni. In genere, tuttavia, si alloca un singolo oggetto a tessellazione e lo si usa per tutte le tessellazioni. Non è necessario liberarlo perché usa una piccola quantità di memoria. D'altra parte, se si scrive una funzione di libreria che usa la tessellazione GLU, prestare attenzione a liberare tutti gli oggetti a tessellazione creati.

 

 




