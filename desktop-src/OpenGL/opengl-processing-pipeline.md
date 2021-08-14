---
title: Pipeline di elaborazione OpenGL
description: Pipeline di elaborazione OpenGL
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, pipeline di elaborazione
- pipeline di elaborazione OpenGL
- Pipeline OpenGL
- framebuffer, pipeline di elaborazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b52568de344404e9bddbedbacc40beda064b09d3e3af96c2657f670e677c32a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936866"
---
# <a name="opengl-processing-pipeline"></a>Pipeline di elaborazione OpenGL

Molte funzioni OpenGL vengono usate in modo specifico per disegnare oggetti come punti, linee, poligoni e bitmap. Alcune funzioni controllano il modo in cui si verifica parte di questo disegno, ad esempio quelle che abilitano l'antialiasing o la texturing. Altre funzioni riguardano in modo specifico la manipolazione del framebuffer. Negli argomenti di questa sezione viene descritto il funzionamento di tutte le funzioni OpenGL per creare la pipeline di elaborazione OpenGL. Questa sezione prende anche in esame le fasi in cui i dati vengono effettivamente elaborati e le lega alle funzioni OpenGL.

Il diagramma seguente illustra in dettaglio la pipeline di elaborazione OpenGL. Per la maggior parte della pipeline, è possibile visualizzare tre frecce verticali tra le fasi principali. Queste frecce rappresentano i vertici e i due tipi principali di dati che possono essere associati ai vertici: i valori dei colori e le coordinate della trama. Si noti anche che i vertici vengono assemblati in primitive, quindi in frammenti e infine in pixel nel framebuffer. Questa progressione viene illustrata in modo più dettagliato in [Vertici,](vertices.md) [Primitive,](primitives.md) [Frammenti](fragments.md)e [Pixel.](pixels.md)

![Diagramma che mostra la pipeline di elaborazione OpenGL.](images/proc01.png)

 

 




