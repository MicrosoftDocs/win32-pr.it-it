---
title: Pipeline di elaborazione OpenGL
description: Pipeline di elaborazione OpenGL
ms.assetid: 98ac89d1-0d7b-45b2-8d6e-c421b9289d60
keywords:
- OpenGL, pipeline di elaborazione
- elaborazione della pipeline OpenGL
- OpenGL della pipeline
- framebuffer, pipeline di elaborazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73d67447066b9d397bbb272932f51c6d3003f11e
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104567942"
---
# <a name="opengl-processing-pipeline"></a>Pipeline di elaborazione OpenGL

Molte funzioni OpenGL vengono usate in modo specifico per disegnare oggetti quali punti, linee, poligoni e bitmap. Alcune funzioni controllano il modo in cui si verificano alcuni di questi disegni, ad esempio quelli che abilitano l'anti-aliasing o la texturing. Altre funzioni sono specificamente interessate dalla manipolazione del framebuffer. Negli argomenti di questa sezione viene descritto il funzionamento combinato di tutte le funzioni OpenGL per creare la pipeline di elaborazione OpenGL. In questa sezione vengono inoltre esaminate in dettaglio le fasi in cui i dati vengono effettivamente elaborati e le fasi vengono legate alle funzioni OpenGL.

Il diagramma seguente illustra la pipeline di elaborazione OpenGL. Per la maggior parte della pipeline, è possibile visualizzare tre frecce verticali tra le fasi principali. Queste frecce rappresentano i vertici e i due tipi di dati principali che possono essere associati ai vertici, ovvero i valori dei colori e le coordinate di trama. Si noti inoltre che i vertici vengono assemblati in primitive, quindi in frammenti e infine in pixel nel framebuffer. Questa progressione viene discussa in modo più dettagliato in [vertici](vertices.md), [primitivi](primitives.md), [frammenti](fragments.md)e [pixel](pixels.md).

![Diagramma che illustra la pipeline di elaborazione OpenGL.](images/proc01.png)

 

 




