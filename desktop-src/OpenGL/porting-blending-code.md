---
title: Porting del codice di blending
description: In IRIS GL, quando si disegna su buffer front e back, la fusione viene eseguita leggendo uno dei buffer, combinando con tale colore e quindi scrivendo il risultato in entrambi i buffer. In OpenGL, tuttavia, ogni buffer viene letto a sua volta, misto e quindi scritto.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- porting IRIS GL, fusione
- porting da IRIS GL, blending
- porting in OpenGL da IRIS GL, blending
- Porting OpenGL da IRIS GL, blending
- sfumatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13548a2f08821e4f80bf63230077f9a39540ba9b8a37763e7935d211ef0dcdc0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485911"
---
# <a name="porting-blending-code"></a>Porting del codice di blending

In IRIS GL, quando si disegna su buffer front e back, la fusione viene eseguita leggendo uno dei buffer, combinando con tale colore e quindi scrivendo il risultato in entrambi i buffer. In OpenGL, tuttavia, ogni buffer viene letto a sua volta, misto e quindi scritto.

Nella tabella seguente sono elencate le funzioni di fusione IRIS GL e le funzioni OpenGL equivalenti.



| Funzione GL IRIS  | Funzione OpenGL                            | Significato                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | [**glEnable**](glenable.md) ( GL \_ BLEND ) | Attiva la fusione.          |
| **funzione di blend** | [**glBlendFunc**](glblendfunc.md)         | Specifica una funzione di blend. |



 

La funzione OpenGL **glBlendFunc** e la funzione **blendfunction** IRIS GL sono quasi identiche. La tabella seguente elenca i fattori di blend IRIS GL e i relativi equivalenti OpenGL.



| IRIS GL          | Opengl                     | Note             |
|------------------|----------------------------|-------------------|
| BF \_ ZERO         | GL \_ ZERO                   |                   |
| BF \_ ONE          | GL \_ ONE                    |                   |
| BF \_ SA           | GL \_ SRC \_ ALPHA             |                   |
| BF \_ MSA          | GL \_ ONE \_ MINUS \_ SRC \_ ALPHA |                   |
| DAF BF \_           | GL \_ DST \_ ALPHA             |                   |
| Assistente al debug \_ gestito di BF          | GL \_ ONE \_ MINUS \_ DST \_ ALPHA |                   |
| BF \_ SC           | COLORE \_ GL \_ SRC             |                   |
| BF \_ MSC          | GL \_ ONE \_ MINUS \_ SRC \_ COLOR | Solo destinazione. |
| Controller di dominio BF \_           | COLORE \_ ORA \_ LEGALE GL             | Solo origine.      |
| BF \_ MDC          | GL \_ ONE \_ MINUS \_ DST \_ COLOR | Solo origine.      |
| BF \_ MIN \_ SA \_ MDA | GL \_ SRC \_ ALPHA \_ SATURATE   |                   |



 

??

 

 




