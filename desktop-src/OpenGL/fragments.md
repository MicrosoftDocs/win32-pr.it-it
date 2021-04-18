---
title: Frammenti
description: Frammenti
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, frammenti
- Pipeline di elaborazione OpenGL, frammenti
- frammenti OpenGL
- framebuffer, frammenti che modificano i pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298437"
---
# <a name="fragments"></a>Frammenti

Un frammento generato dalla rasterizzazione modifica il pixel corrispondente nel framebuffer solo se supera i test seguenti:

-   [Test di proprietà pixel](pixel-ownership-test.md)
-   [Test Scissor](scissor-test.md)
-   [Test alfa](alpha-test.md)
-   [Test stencil](stencil-test.md)
-   [Test del buffer di profondità](depth-buffer-test.md)

Se viene superato, i dati del frammento possono sostituire i valori del framebuffer esistenti oppure è possibile combinarli con i dati esistenti nel framebuffer, a seconda dello stato di determinate modalità. È possibile combinare il frammento con i dati nel framebuffer:

-   [Fusione](blending.md)
-   [Dithering](dithering.md)
-   [Operazioni logiche](logical-operations.md)

 

 




