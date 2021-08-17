---
title: Fusione
description: La fusione combina i valori R, G, B e A di un frammento con quelli archiviati nel framebuffer nella posizione corrispondente.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- pipeline di elaborazione OpenGL, fusione
- fusione di OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5b38786d2320a646bd6cac096e535e4e1441df98522ac86a146836b929c0986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361435"
---
# <a name="blending"></a>Fusione

La fusione combina i valori R, G, B e A di un frammento con quelli archiviati nel framebuffer nella posizione corrispondente. La fusione, eseguita solo in modalità RGBA, dipende dal valore alfa del frammento e da quello del pixel attualmente archiviato corrispondente. può anche dipendere dai valori RGB. È possibile controllare la fusione [**con glBlendFunc**](glblendfunc.md), con cui si indicano i fattori di fusione di origine e destinazione.

 

 




