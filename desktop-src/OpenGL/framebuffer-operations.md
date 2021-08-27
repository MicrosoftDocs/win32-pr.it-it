---
title: Operazioni framebuffer
description: Per selezionare il buffer in cui vengono scritti i valori dei colori, usare glDrawBuffer.
ms.assetid: 5469a183-1dc0-4ec2-bd7e-54060b5a2876
keywords:
- Pipeline di elaborazione OpenGL, operazioni framebuffer
- framebuffers, operazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ad9d3bb04d9c063ecd9ec588843577cc577bbe62f686f136a40cdaddcbfc77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082331"
---
# <a name="framebuffer-operations"></a>Operazioni framebuffer

Per selezionare il buffer in cui vengono scritti i valori dei colori, usare [**glDrawBuffer**](gldrawbuffer.md). Si usano quattro diverse funzioni per mascherare la scrittura di bit in ognuno dei buffer di frame logici dopo l'esecuzione di tutte le operazioni per frammento:

-   [**glIndexMask**](glindexmask.md)
-   [**glColorMask**](glcolormask.md)
-   [**glDepthMask**](gldepthmask.md)
-   [**glStencilMask**](glstencilmask.md)

La [**funzione glAccum**](glaccum.md) controlla il funzionamento del buffer di accumulo. Infine, [**glClear**](glclear.md) imposta ogni pixel in un subset specificato dei buffer sul valore specificato con [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)o [**glClearAccum**](glclearaccum.md).

 

 




