---
title: Scelta tra RGBA e modalità Color-Index
description: In generale, usare la modalità RGBA per le applicazioni OpenGL; offre maggiore flessibilità rispetto alla modalità di indice dei colori per gli effetti come ombreggiatura, illuminazione, mappatura dei colori, nebbia, anti-aliasing e fusione.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL in Windows, modalità RGBA
- OpenGL per Windows, modalità indice colori
- OpenGL in modalità RGBA
- OpenGL modalità di indice colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368461d6ece7b823a8627f664daace027fd76c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710423"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a>Scelta tra RGBA e modalità Color-Index

In generale, usare la modalità RGBA per le applicazioni OpenGL; offre maggiore flessibilità rispetto alla modalità di indice dei colori per gli effetti come ombreggiatura, illuminazione, mappatura dei colori, nebbia, anti-aliasing e fusione.

Provare a usare la modalità di indice dei colori nei casi seguenti:

-   Se è disponibile un numero limitato di bitplane; la modalità di indicizzazione dei colori può produrre ombreggiatura meno grossolana rispetto alla modalità RGBA.
-   Se non si è interessati a usare i colori "reali"; ad esempio, usando più colori in una mappa topografica per designare le elevazioni relative.
-   Quando si esegue il porting di un'applicazione esistente che usa ampiamente la modalità di indice colori.
-   Quando si desidera utilizzare l'animazione e gli effetti della mappa dei colori nell'applicazione. Questa operazione non è possibile nei dispositivi con colori reali.

 

 




