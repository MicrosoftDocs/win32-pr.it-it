---
title: Tavolozze e gestione tavolozze
description: Gestione tavolozze di Windows, che fa parte di GDI, è destinato in modo specifico a schede di visualizzazione a 8 bit con una tavolozza hardware di 256 voci di colori.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL per Windows, gestione tavolozze
- OpenGL per Windows, tavolozze hardware
- gestione tavolozze OpenGL
- tavolozze hardware OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dac7d122ec36201e0156a141efc3291a87c7150
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298203"
---
# <a name="palettes-and-the-palette-manager"></a>Tavolozze e gestione tavolozze

Gestione tavolozze di Windows, che fa parte di GDI, è destinato in modo specifico a schede di visualizzazione a 8 bit con una *tavolozza hardware* di 256 voci di colori. I pixel sullo schermo vengono archiviati come indice a 8 bit nella tavolozza hardware. Ogni voce della tavolozza hardware in genere definisce un colore a 24 bit (8 ciascuno di rosso, verde e blu).

Gestione tavolozze gestisce una *tavolozza di sistema* che è una copia della tavolozza hardware. La tavolozza di sistema è divisa in due sezioni: 20 colori riservati e i rimanenti colori 236, che è possibile impostare tramite Gestione tavolozze.

Una *tavolozza logica* di 20 colori predefinita viene selezionata e realizzata in un contesto di dispositivo. È possibile creare e usare una nuova tavolozza logica. Per modificare la tavolozza di sistema, selezionare e realizzare la tavolozza logica creata.

Probabilmente si creerà una tavolozza logica per specificare i colori che si desidera visualizzare nell'applicazione OpenGL. Utilizzando determinate chiamate GDI, è possibile sostituire temporaneamente la maggior parte della tavolozza di sistema con una tavolozza logica. Utilizzando una tavolozza logica, è possibile definire i colori dei pixel per GDI utilizzando la modalità RGBA o l'indice dei colori. Le dimensioni massime di una tavolozza logica sono 256 colori per i dispositivi a 8 bit e 4.096 colori in un dispositivo a colori true (16, 24 e 32 bit).

Per ulteriori informazioni sulle modalità di RGBA e di indice dei colori, vedere modalità [RGBA e gestione tavolozza Windows](rgba-mode-and-windows-palette-management.md) e [modalità colori OpenGL e gestione tavolozza di Windows](opengl-color-modes-and-windows-palette-management.md).

 

 




