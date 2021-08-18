---
title: Modalità colore OpenGL e gestione Windows tavolozza
description: L'implementazione Microsoft di OpenGL in Windows supporta due modalità dati pixel di colore RGBA e modalità di indicizzazione dei colori. Windows due modi analoghi per gestire la gestione del colore reale e della tavolozza.
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL su Windows,modalità colore
- OpenGL in Windows,gestione della tavolozza
- Gestione della tavolozza OpenGL
- modalità colore OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf91ebb45e99368596cb48cb625f0eb6de025e6664144f104f6a9c17951a1e7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144134"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a>Modalità colore OpenGL e gestione Windows tavolozza

L'implementazione Microsoft di OpenGL in Windows supporta due modalità dati pixel di colore: RGBA e modalità di indicizzazione dei colori. Windows due modi analoghi per gestire i colori: la gestione dei colori e della tavolozza.

I dispositivi a colori reale, in grado di accettare 16, 24 o più bit di informazioni sui colori per pixel, possono visualizzare decine di migliaia, decine di milioni o più colori contemporaneamente. Le complessità si verificano, tuttavia, quando un'applicazione deve gestire la modalità RGBA o l'indice dei colori in un dispositivo di tipo tavolozza. I dispositivi di tipo tavolozza, ad esempio uno schermo VGA a 256 colori, sono limitati al numero di colori che possono visualizzare contemporaneamente. Le applicazioni devono gestire una serie di dettagli difficili per usare correttamente i dispositivi di tipo tavolozza. Poiché i programmi in modalità indice colori non usano una tavolozza hardware, sono più difficili da usare con i dispositivi di colore reale rispetto ai programmi che usano la modalità RGBA.

 

 




