---
title: Strategie di disegno OpenGL multithread
description: GDI non supporta più thread.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL in Windows multithreading
- disegno OpenGL multithread OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d928a481e4334f97cad2f7009f008c899ad8378f3fd15cf9e117e6b9599393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937256"
---
# <a name="multithread-opengl-drawing-strategies"></a>Strategie di disegno OpenGL multithread

GDI non supporta più thread. È necessario usare un contesto di dispositivo distinto e un contesto di rendering distinto per ogni thread. Ciò tende a limitare i vantaggi in termini di prestazioni dell'uso di più thread con sistemi a processore singolo che eseguono applicazioni OpenGL. Esistono tuttavia modi per usare i thread con un sistema a processore singolo per aumentare notevolmente le prestazioni. Ad esempio, è possibile usare un thread separato per passare le chiamate di rendering OpenGL all'hardware 3D dedicato.

I sistemi SMP (Symmetric Multiprocessing) possono trarre vantaggio dall'uso di più thread. Una strategia ovvia consiste nell'usare un thread separato per ogni processore per gestire il rendering OpenGL in finestre separate. Ad esempio, in un'applicazione di simulazione di volo è possibile usare processori e thread separati per eseguire il rendering delle visualizzazioni frontale, posteriore e laterale.

Un thread può avere un solo contesto di rendering attivo corrente. Quando si usano più thread e più contesti di rendering, è necessario fare attenzione a sincronizzarne l'uso. Ad esempio, usare un solo thread per chiamare [**SwapBuffers al**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) termine del disegno di tutti i thread.

 

 




