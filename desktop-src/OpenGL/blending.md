---
title: Fusione
description: La fusione combina i valori R, G, B e i valori di un frammento con quelli archiviati nel framebuffer nella posizione corrispondente.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- Pipeline di elaborazione OpenGL, fusione
- fusione di OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0fe7cd2893700d8015148fcc5c25707d19676c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329940"
---
# <a name="blending"></a>Fusione

La fusione combina i valori R, G, B e i valori di un frammento con quelli archiviati nel framebuffer nella posizione corrispondente. La fusione, che viene eseguita solo in modalità RGBA, dipende dal valore alfa del frammento e dal corrispondente pixel attualmente archiviato; può inoltre dipendere dai valori RGB. È possibile controllare la fusione con [**glBlendFunc**](glblendfunc.md), con cui si indicano i fattori di combinazione di origine e destinazione.

 

 




