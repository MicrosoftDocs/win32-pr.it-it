---
title: Porting di piani di ritaglio
description: OpenGL implementa i piani di ritaglio in modo analogo a IRIS GL. In OpenGL è inoltre possibile eseguire query sui piani di ritaglio. La tabella seguente elenca le funzioni del piano di ritaglio di IRIS GL e le relative funzioni OpenGL equivalenti.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- Porting di IRIS GL, piani di ritaglio
- porting da IRIS GL, piani di ritaglio
- porting in OpenGL da IRIS GL, piani di ritaglio
- Porting OpenGL da IRIS GL, piani di ritaglio
- ritaglio di piani
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b531b39daf6670a3a99d9a4cbcf55158ea2d4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713582"
---
# <a name="porting-clipping-planes"></a>Porting di piani di ritaglio

OpenGL implementa i piani di ritaglio in modo analogo a IRIS GL. In OpenGL è inoltre possibile eseguire query sui piani di ritaglio. La tabella seguente elenca le funzioni del piano di ritaglio di IRIS GL e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL                          | OpenGL (funzione)                                                                               | Significato                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| **clipplane** (i, **CP \_ on**, params)     | [**glEnable**](glenable.md) (GL \_ clip \_ planei)                                             | Abilita il ritaglio sul piano i.             |
| **clipplane**(i, **CP \_ define**, Plane) | [**glClipPlane**](glclipplane.md) (GL \_ clip \_ Planes, Plane)                                | Definisce il piano di ritaglio.                  |
|                                           | [**glGetClipPlane**](glgetclipplane.md)                                                      | Restituisce l'equazione del piano di ritaglio.         |
|                                           | [**glIsEnabled**](glisenabled.md) (GL \_ clip \_ planei)                                       | Restituisce true se il piano di ritaglio i è abilitato. |
| **scrmask**                               | [**glScissor**](glscissor.md)                                                                | Definisce la casella a forbice.                 |
| **getscrmask**                            | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ casella GL Scissor \_ ) | Restituisce la casella a forbice corrente.         |



 

Per attivare il test a forbice, chiamare **glEnable** usando \_ \_ la casella della forbice GL come parametro.

??

 

 




