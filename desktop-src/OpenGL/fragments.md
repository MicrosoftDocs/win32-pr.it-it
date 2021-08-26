---
title: Frammenti
description: Frammenti
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, frammenti
- pipeline di elaborazione OpenGL, frammenti
- frammenti OpenGL
- buffer frame, frammenti che modificano pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab5d4124445455e518e4f091730e6e38e899442785b9f86ef73a230b99fbd41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082411"
---
# <a name="fragments"></a>Frammenti

Un frammento prodotto dalla rasterizzazione modifica il pixel corrispondente nel buffer frame solo se supera i test seguenti:

-   [Test di proprietà pixel](pixel-ownership-test.md)
-   [Test di scissor](scissor-test.md)
-   [Test alfa](alpha-test.md)
-   [Test degli stencil](stencil-test.md)
-   [Test del buffer di profondità](depth-buffer-test.md)

Se passa, i dati del frammento possono sostituire i valori framebuffer esistenti oppure è possibile combinarli con i dati esistenti in framebuffer, a seconda dello stato di determinate modalità. È possibile combinare il frammento con i dati nel buffer frame:

-   [Fusione](blending.md)
-   [Dithering](dithering.md)
-   [Operazioni logiche](logical-operations.md)

 

 




