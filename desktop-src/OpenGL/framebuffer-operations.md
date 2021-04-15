---
title: Operazioni framebuffer
description: Per selezionare il buffer in cui vengono scritti i valori dei colori, utilizzare glDrawBuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Pipeline di elaborazione OpenGL, operazioni framebuffer
- framebuffer, operazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6199700d00a6628548404870dd6ef6ce3e2c825
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515598"
---
# <a name="framebuffer-operations"></a>Operazioni framebuffer

Per selezionare il buffer in cui vengono scritti i valori dei colori, utilizzare [**glDrawBuffer**](gldrawbuffer.md). È possibile utilizzare quattro funzioni diverse per mascherare la scrittura di bit in ogni framebuffer logico dopo che sono state eseguite tutte le operazioni per frammento:

-   [**glIndexMask**](glindexmask.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glStencilMask**](glstencilmask.md)

La funzione [**glAccum**](glaccum.md) controlla l'operazione del buffer di accumulo. Infine, [**glClear**](glclear.md) imposta ogni pixel in un subset specificato di buffer sul valore specificato con [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)o [**glClearAccum**](glclearaccum.md).

 

 




