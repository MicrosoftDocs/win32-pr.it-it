---
title: Tavolozze e Gestione tavolozze
description: La Windows Palette Manager, che fa parte di GDI, è destinata in particolare alle schede di visualizzazione a 8 bit con una tavolozza hardware di 256 voci di colore.
ms.assetid: 3bfa5077-37ac-4597-98da-f26ad1c107a1
keywords:
- OpenGL in Windows,gestione palette
- OpenGL su Windows,tavolozze hardware
- Gestione palette OpenGL
- palette hardware OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58407a5ddafe862caa73edd498c4da529b0ac987880828177d0d0b284601efed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936278"
---
# <a name="palettes-and-the-palette-manager"></a>Tavolozze e Gestione tavolozze

La Windows Palette Manager, che fa parte di GDI, è destinata in particolare alle schede di visualizzazione a 8 bit con una tavolozza *hardware* di 256 voci di colore. I pixel sullo schermo vengono archiviati come indice a 8 bit nella tavolozza hardware. Ogni voce nella tavolozza hardware definisce in genere un colore a 24 bit (8 ciascuno di rosso, verde e blu).

Gestione palette gestisce un *riquadro di* sistema che è una copia del riquadro hardware. La tavolozza di sistema è suddivisa in due sezioni: 20 colori riservati e i restanti 236 colori, che è possibile impostare usando Gestione tavolozza.

Una tavolozza logica predefinita a 20 *colori* viene selezionata e realizzata in un contesto di dispositivo. È possibile creare e usare un nuovo riquadro logico. Per modificare il riquadro di sistema, selezionare e realizzare il riquadro logico creato.

Si creerà probabilmente una tavolozza logica per specificare i colori da visualizzare nell'applicazione OpenGL. Usando determinate chiamate GDI, è possibile sostituire temporaneamente la maggior parte del riquadro di sistema con un riquadro logico. Usando una tavolozza logica, è possibile definire i colori dei pixel per GDI usando la modalità RGBA o la modalità di indice dei colori. Le dimensioni massime di una tavolozza logica sono 256 colori per dispositivi a 8 bit e 4.096 colori in un dispositivo a colori reale (16, 24 e 32 bit).

Per altre informazioni sulle modalità RGBA e sugli indici dei colori, vedere [Modalità RGBA](rgba-mode-and-windows-palette-management.md) e Windows Palette Management e [OpenGL Color Modes e Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).

 

 




