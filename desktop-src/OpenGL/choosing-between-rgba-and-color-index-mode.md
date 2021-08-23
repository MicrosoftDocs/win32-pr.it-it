---
title: Scelta tra RGBA e Color-Index modalità
description: In generale, usare la modalità RGBA per le applicazioni OpenGL. offre maggiore flessibilità rispetto alla modalità di indice dei colori per effetti quali ombreggiatura, illuminazione, mapping dei colori, nebbia, antialiasing e fusione.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL in Windows,modalità RGBA
- OpenGL in modalità Windows,color-index
- OpenGL in modalità RGBA
- Modalità indice colori OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa78096369ec9ba01d6e0dcd3d67535a0d368ef7a5018d3679f9f64dcdf74d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554631"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a>Scelta tra RGBA e Color-Index modalità

In generale, usare la modalità RGBA per le applicazioni OpenGL. offre maggiore flessibilità rispetto alla modalità di indice dei colori per effetti quali ombreggiatura, illuminazione, mapping dei colori, nebbia, antialiasing e fusione.

Provare a usare la modalità color-index nei casi seguenti:

-   Se è disponibile un numero limitato di bitplan; la modalità di indice dei colori può produrre un'ombreggiatura meno grosso modo rispetto alla modalità RGBA.
-   Se non si è interessati all'uso di colori "reali"; ad esempio l'uso di diversi colori in una mappa topografica per designare elevazioni relative.
-   Quando si esegue il porting di un'applicazione esistente che usa ampiamente la modalità indice colori.
-   Quando si vuole usare l'animazione e gli effetti della mappa colori nell'applicazione. Questa operazione non è possibile nei dispositivi a colori veri.

 

 




