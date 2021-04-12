---
title: Modalità colori OpenGL e gestione tavolozza Windows
description: L'implementazione Microsoft di OpenGL in Windows supporta due modalità di dati pixel di colore RGBA e modalità di indice dei colori. Windows offre due modi analoghi per gestire la gestione dei colori e della tavolozza true.
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL per Windows, modalità colori
- OpenGL per Windows, gestione tavolozza
- gestione tavolozza OpenGL
- modalità colori OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3d63778301ec55b962f3f66e79d99cee09be9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329495"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a>Modalità colori OpenGL e gestione tavolozza Windows

L'implementazione Microsoft di OpenGL in Windows supporta due modalità di dati dei pixel a colori: RGBA e modalità di indice dei colori. In Windows sono disponibili due modalità analoghe di gestione del colore, ovvero la gestione dei colori e della tavolozza.

I dispositivi con colori reali, in grado di accettare 16, 24 o più bit di informazioni sui colori per pixel, possono visualizzare decine di migliaia, decine di milioni o più colori contemporaneamente. Tuttavia, le complessità si verificano quando un'applicazione deve gestire RGBA o la modalità di indice dei colori in un dispositivo di tipo tavolozza. I dispositivi di tipo tavolozza, ad esempio la visualizzazione VGA a colori 256, sono limitati al numero di colori che possono essere visualizzati contemporaneamente. Per usare correttamente i dispositivi di tipo tavolozza, le applicazioni devono gestire una serie di dettagli complessi. Poiché i programmi in modalità di indice dei colori non usano una tavolozza hardware, sono più difficili da usare con i dispositivi con colori reali rispetto ai programmi che usano la modalità RGBA.

 

 




