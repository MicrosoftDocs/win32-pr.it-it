---
title: Porting del codice di fusione
description: In IRIS GL, quando si disegnano i buffer di primo e indietro, la fusione viene eseguita leggendo uno dei buffer, combinando con tale colore e quindi scrivendo il risultato in entrambi i buffer. In OpenGL, tuttavia, ogni buffer viene letto a sua volta, mescolato e quindi scritto.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- Porting di IRIS GL, fusione
- porting da IRIS GL, blending
- porting in OpenGL da IRIS GL, blending
- Porting OpenGL da IRIS GL, blending
- sfumatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7956c675848f454b660126a7a17869295a827438
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298729"
---
# <a name="porting-blending-code"></a>Porting del codice di fusione

In IRIS GL, quando si disegnano i buffer di primo e indietro, la fusione viene eseguita leggendo uno dei buffer, combinando con tale colore e quindi scrivendo il risultato in entrambi i buffer. In OpenGL, tuttavia, ogni buffer viene letto a sua volta, mescolato e quindi scritto.

La tabella seguente elenca le funzioni di blending IRIS GL e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL  | OpenGL (funzione)                            | Significato                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | [**glEnable**](glenable.md) (GL \_ Blend) | Attiva la fusione.          |
| **BlendFunction** | [**glBlendFunc**](glblendfunc.md)         | Specifica una funzione Blend. |



 

La funzione **glBlendFunc** di OpenGL e la funzione **BlendFunction** di Iris GL sono quasi identiche. La tabella seguente elenca i fattori di Blend di IRIS GL e i rispettivi equivalenti OpenGL.



| GL IRIS          | OpenGL                     | Note             |
|------------------|----------------------------|-------------------|
| BF \_ zero         | \_zero GL                   |                   |
| BF \_ uno          | GL \_ uno                    |                   |
| \_sa BF           | \_alfa src \_ GL             |                   |
| MSA di BF \_          | GL \_ 1 \_ meno \_ src \_ Alpha |                   |
| BF \_ da           | \_alfa del DST GL \_             |                   |
| \_MDA BF          | GL \_ 1 \_ meno \_ DST \_ Alpha |                   |
| BF \_ SC           | \_colore GL src \_             |                   |
| BF \_ MSC          | GL \_ uno \_ meno \_ il \_ colore src | Solo destinazione. |
| \_DC BF           | \_colore GL DST \_             | Solo origine.      |
| BF \_ MDC          | GL \_ uno \_ meno \_ il \_ colore DST | Solo origine.      |
| \_Assistente al \_ \_ debug gestito min BF | \_ \_ satura Alpha di GL src \_   |                   |



 

??

 

 




