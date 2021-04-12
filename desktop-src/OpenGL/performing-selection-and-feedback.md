---
title: Esecuzione di selezioni e commenti
description: Esecuzione di selezioni e commenti
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL, selezione
- OpenGL, commenti e suggerimenti
- OpenGL, rendering
- modalità di selezione OpenGL
- modalità feedback OpenGL
- modalità di rendering OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329996"
---
# <a name="performing-selection-and-feedback"></a>Esecuzione di selezioni e commenti

Selezione, feedback e rendering si escludono a vicenda modalità di funzionamento. Il rendering è la modalità standard predefinita durante la quale i frammenti vengono prodotti dalla rasterizzazione.

Nelle modalità selezione e feedback non viene prodotto alcun frammento; Pertanto, non si verifica alcuna modifica del framebuffer. In modalità di selezione è possibile determinare quali primitive verranno disegnate in una determinata area di una finestra; in modalità feedback, le informazioni sulle primitive che verranno rasterizzate vengono riportate all'applicazione.

È possibile scegliere tra queste tre modalità con [**glRenderMode**](glrendermode.md).

-   [Selezione](selection.md)
-   [Commenti e suggerimenti](feedback.md)
-   [Guida di riferimento a selezione e feedback](selection-and-feedback-reference.md)

 

 




