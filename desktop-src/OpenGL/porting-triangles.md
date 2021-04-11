---
title: Triangoli di porting
description: È possibile creare tre tipi di triangoli in triangoli separati di OpenGL, strisce triangolari e ventole a triangolo.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- Porting di IRIS GL, triangoli
- porting da IRIS GL, triangoli
- porting in OpenGL da IRIS GL, triangoli
- Porting OpenGL da IRIS GL, triangoli
- funzioni di disegno, triangoli
- triangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c7a0af4b538bb951cf0d1c5f2e12b2e1badda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330988"
---
# <a name="porting-triangles"></a>Triangoli di porting

È possibile creare tre tipi di triangoli in OpenGL: triangoli separati, strisce triangolari e ventole di triangolo.

OpenGL non ha un equivalente per la funzione **swaptmesh** di Iris GL. È possibile ottenere lo stesso effetto usando una combinazione di triangoli, strisce triangolari e ventole di triangolo.

La tabella seguente elenca le funzioni di IRIS GL per il disegno di triangoli e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL           | Parametro glBegin equivalente | Significato                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | triangoli GL \_                | Triple di vertici interpretati come triangoli. |
| **bgntmesh**, **endtmesh** | \_striscia del triangolo GL \_          | Strisce collegate di triangoli.                   |
|                            | \_ventola del triangolo GL \_            | Fan collegati di triangoli.                     |



 

??

 

 




