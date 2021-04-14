---
title: Creazione di un contesto di rendering non corrente
description: Per scollegare un contesto di rendering da un thread, renderlo non aggiornato. Questa operazione può essere eseguita chiamando la funzione wglMakeCurrent con i parametri impostati su NULL. Di seguito è riportato un esempio di questa semplice attività.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL per Windows, contesti di rendering
- rendering di contesti OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12b3e0184a606faef7792b990d674054c5ddf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329511"
---
# <a name="making-a-rendering-context-not-current"></a>Creazione di un contesto di rendering non corrente

Per scollegare un contesto di rendering da un thread, renderlo non aggiornato. Questa operazione può essere eseguita chiamando la funzione [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) con i parametri impostati su **null**. Di seguito è riportato un esempio di questa semplice attività.

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




