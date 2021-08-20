---
title: Funzioni di porting dei commenti e suggerimenti
description: Con IRIS GL, il modo in cui viene gestito il feedback varia a seconda del computer che esegue IRIS GL.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- portabilità IRIS GL, feedback
- porting da IRIS GL, feedback
- porting to OpenGL from IRIS GL,feedback
- Porting OpenGL da IRIS GL, feedback
- feedback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0f4ab584dfbd9038d45e7d24c006857f278a9239fc6f9da4d38a75363f0d585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132633"
---
# <a name="porting-feedback-functions"></a>Funzioni di porting dei commenti e suggerimenti

Con IRIS GL, il modo in cui viene gestito il feedback varia a seconda del computer che esegue IRIS GL. OpenGL standardizza le funzioni di feedback in modo da poter contare su feedback coerente tra le varie piattaforme hardware. La tabella seguente elenca le funzioni di feedback IRIS GL e le funzioni OpenGL equivalenti.



| Funzione GL IRIS | Funzione OpenGL                                                                                            | Significato                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| **Valutazione**     | [**glRenderMode**](glrendermode.md) ( GL \_ FEEDBACK )                                                      | Passa alla modalità feedback.                    |
| **endfeedback**  | [**glRenderMode**](glrendermode.md) ( GL \_ RENDER )[**glFeedbackBuffer**](glfeedbackbuffer.md)<br/> | Passa alla modalità di rendering.                   |
| **Passthrough**  | [**glPassThrough**](glpassthrough.md)                                                                     | Inserisce un marcatore di token nel buffer di feedback. |



 

 

 





