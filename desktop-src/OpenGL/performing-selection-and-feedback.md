---
title: Esecuzione della selezione e del feedback
description: Esecuzione della selezione e del feedback
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL, selezione
- OpenGL, feedback
- OpenGL, rendering
- modalità di selezione OpenGL
- modalità feedback OpenGL
- Modalità di rendering OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95efe3f07e86056cd0364daaed1e6a9c0ef402afc18b14d74cca313c9835479f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936286"
---
# <a name="performing-selection-and-feedback"></a>Esecuzione della selezione e del feedback

Selezione, feedback e rendering sono modalità operative che si escludono a vicenda. Il rendering è la modalità predefinita normale durante la quale i frammenti vengono prodotti dalla rasterizzazione.

Nelle modalità di selezione e feedback non vengono prodotti frammenti. pertanto non viene apportata alcuna modifica al buffer dei frame. In modalità di selezione è possibile determinare quali primitive verranno disegnate in un'area di una finestra. In modalità feedback, le informazioni sulle primitive che verranno rasterizzate vengono riportate all'applicazione.

È possibile scegliere tra queste tre modalità [**con glRenderMode**](glrendermode.md).

-   [Selezione](selection.md)
-   [Commenti e suggerimenti](feedback.md)
-   [Riferimento per la selezione e il feedback](selection-and-feedback-reference.md)

 

 




