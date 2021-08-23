---
title: Porting dei piani di ritaglio
description: OpenGL implementa i piani di ritaglio in modo simile a IRIS GL. Inoltre, in OpenGL è possibile eseguire query su piani di ritaglio. Nella tabella seguente sono elencate le funzioni del piano di ritaglio IRIS GL e le funzioni OpenGL equivalenti.
ms.assetid: bfca59c3-b7ef-4545-8b8d-022ea782569b
keywords:
- Porting IRIS GL, piani di ritaglio
- porting da IRIS GL, piani di ritaglio
- porting in OpenGL da IRIS GL, piani di ritaglio
- Porting OpenGL da IRIS GL, piani di ritaglio
- piani di ritaglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f314b7c6453de3b0933970b7d520a8c161d6eef4a9bb98ea891c73665fba4933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777121"
---
# <a name="porting-clipping-planes"></a>Porting dei piani di ritaglio

OpenGL implementa i piani di ritaglio in modo simile a IRIS GL. Inoltre, in OpenGL è possibile eseguire query su piani di ritaglio. Nella tabella seguente sono elencate le funzioni del piano di ritaglio IRIS GL e le funzioni OpenGL equivalenti.



| Funzione GL IRIS                          | Funzione OpenGL                                                                               | Significato                                  |
|-------------------------------------------|-----------------------------------------------------------------------------------------------|------------------------------------------|
| **clipplane** (i, **CP \_ ON**, params)     | [**glEnable**](glenable.md) ( GL \_ CLIP \_ PLANEi )                                             | Abilita il ritaglio sul piano i.             |
| **clipplane**( i, **CP \_ DEFINE**, plane ) | [**glClipPlane**](glclipplane.md) ( GL \_ CLIP \_ PLANEi, plane )                                | Definisce il piano di ritaglio.                  |
|                                           | [**glGetClipPlane**](glgetclipplane.md)                                                      | Restituisce l'equazione del piano di ritaglio.         |
|                                           | [**glIsEnabled**](glisenabled.md) ( GL \_ CLIP \_ PLANEi )                                       | Restituisce true se il piano di ritaglio i è abilitato. |
| **scrmask**                               | [**glScissor**](glscissor.md)                                                                | Definisce la casella di forbice.                 |
| **getscrmask**                            | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL \_ SCISSOR \_ BOX ) | Restituisce la casella di forbice corrente.         |



 

Per attivare il test della forbice, chiamare **glEnable** usando GL \_ SCISSOR \_ BOX come parametro.

??

 

 




