---
title: Rendere un contesto di rendering non corrente
description: Per scollegare un contesto di rendering da un thread, renderlo non corrente. A tale scopo, chiamare la funzione wglMakeCurrent con i parametri impostati su NULL. Di seguito è riportato un esempio di questa semplice attività.
ms.assetid: fe76e3d3-5480-448d-95aa-a5af0da309f3
keywords:
- OpenGL in Windows,contesti di rendering
- contesti di rendering OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914bbed6e2d595d23cfcf8dc38820efc18153f4433a2a48446090ec16818b671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937364"
---
# <a name="making-a-rendering-context-not-current"></a>Rendere un contesto di rendering non corrente

Per scollegare un contesto di rendering da un thread, renderlo non corrente. A tale scopo, chiamare la [**funzione wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) con i parametri impostati su **NULL.** Di seguito è riportato un esempio di questa semplice attività.

``` syntax
// detach the current rendering context from the thread  
wglMakeCurrent(NULL, NULL);
```

 

 




