---
title: Portabilità di triangoli
description: È possibile disegnare tre tipi di triangoli in triangoli separati OpenGL, strisce di triangoli e ventole di triangolo.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- Portabilità IRIS GL, triangoli
- porting da IRIS GL, triangoli
- porting to OpenGL from IRIS GL,triangles
- Portabilità OpenGL da IRIS GL, triangoli
- funzioni di disegno, triangoli
- triangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85acc650a709650495b93cdd00176400f00168cc8fe6445a23505f12b332abf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011999"
---
# <a name="porting-triangles"></a>Portabilità di triangoli

È possibile disegnare tre tipi di triangoli in OpenGL: triangoli separati, strisce di triangoli e ventole di triangolo.

OpenGL non ha un equivalente per la funzione **swaptmesh** IRIS GL. È possibile ottenere lo stesso effetto usando una combinazione di triangoli, strisce di triangoli e ventole di triangolo.

La tabella seguente elenca le funzioni IRIS GL per disegnare triangoli e le funzioni OpenGL equivalenti.



| Funzione GL IRIS           | Parametro glBegin equivalente | Significato                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | TRIANGOLI GL \_                | Triple di vertici interpretati come triangoli. |
| **bgntmesh**, **endtmesh** | GL \_ TRIANGLE \_ STRIP          | Strisce collegate di triangoli.                   |
|                            | VENTOLA \_ TRIANGOLO GL \_            | Ventole collegate di triangoli.                     |



 

??

 

 




