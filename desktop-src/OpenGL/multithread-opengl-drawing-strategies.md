---
title: Strategie di disegno OpenGL multithread
description: GDI non supporta più thread.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL per Windows, disegno multithread
- OpenGL disegno OpenGL multithread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bccb08d48bd8ccb62584f15911a1eb65080c4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329503"
---
# <a name="multithread-opengl-drawing-strategies"></a>Strategie di disegno OpenGL multithread

GDI non supporta più thread. È necessario usare un contesto di dispositivo distinto e un contesto di rendering distinto per ogni thread. Ciò tende a limitare i vantaggi in termini di prestazioni dell'utilizzo di più thread con sistemi a processore singolo che eseguono applicazioni OpenGL. Esistono tuttavia modi per utilizzare i thread con un sistema a processore singolo per migliorare significativamente le prestazioni. Ad esempio, è possibile usare un thread separato per passare le chiamate di rendering OpenGL a hardware 3D dedicato.

I sistemi SMP (Symmetric Multiprocessor) possono trarre notevole vantaggio dall'uso di più thread. Una strategia ovvia consiste nell'usare un thread separato per ogni processore per gestire il rendering OpenGL in finestre separate. Ad esempio, in un'applicazione di simulazione del volo è possibile usare processori e thread distinti per eseguire il rendering delle visualizzazioni front, back e Side.

Un thread può avere un solo contesto di rendering attivo e corrente. Quando si usano più thread e più contesti di rendering, è necessario prestare attenzione a sincronizzarne l'uso. Usare, ad esempio, un solo thread per chiamare [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) al termine del disegno di tutti i thread.

 

 




