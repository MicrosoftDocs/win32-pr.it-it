---
title: Porting di funzioni di feedback
description: Con IRIS GL, il modo in cui viene gestito il feedback varia a seconda del computer che esegue IRIS GL.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- Porting di IRIS GL, commenti e suggerimenti
- porting da IRIS GL, commenti e suggerimenti
- porting in OpenGL da IRIS GL, commenti e suggerimenti
- Porting OpenGL da IRIS GL, commenti e suggerimenti
- feedback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a04bcfe2c1d914a178ad7ad0dca95fb85d86bbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221823"
---
# <a name="porting-feedback-functions"></a>Porting di funzioni di feedback

Con IRIS GL, il modo in cui viene gestito il feedback varia a seconda del computer che esegue IRIS GL. OpenGL standardizza le funzioni di feedback per poter contare su feedback coerenti tra varie piattaforme hardware. La tabella seguente elenca le funzioni di feedback di IRIS GL e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL | OpenGL (funzione)                                                                                            | Significato                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| **feedback**     | [**glRenderMode**](glrendermode.md) ( \_ feedback GL)                                                      | Passa alla modalità di feedback.                    |
| **endfeedback**  | [**glRenderMode**](glrendermode.md) ( \_ rendering GL)[**glFeedbackBuffer**](glfeedbackbuffer.md)<br/> | Passa alla modalità di rendering.                   |
| **pass-through**  | [**glPassThrough**](glpassthrough.md)                                                                     | Inserisce un marcatore del token nel buffer di feedback. |



 

 

 





