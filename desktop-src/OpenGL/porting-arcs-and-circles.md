---
title: Porting di archi e cerchi
description: Con OpenGL, gli archi e i cerchi pieni vengono disegnati con le stesse chiamate degli archi e dei cerchi non riempiti. La tabella seguente elenca le funzioni di arco e cerchio IRIS GL e le relative funzioni OpenGL (GLU) equivalenti.
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- Porting di IRIS GL, archi
- porting da IRIS GL, archi
- porting in OpenGL da IRIS GL, archi
- Porting OpenGL da IRIS GL, archi
- funzioni di disegno, archi
- Porting di IRIS GL, cerchi
- porting da IRIS GL, cerchi
- porting in OpenGL da IRIS GL, cerchi
- Porting OpenGL da IRIS GL, cerchi
- disegno di funzioni, cerchi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce17546ce17f24adf80641549d8843a473c8754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396834"
---
# <a name="porting-arcs-and-circles"></a>Porting di archi e cerchi

Con OpenGL, gli archi e i cerchi pieni vengono disegnati con le stesse chiamate degli archi e dei cerchi non riempiti. La tabella seguente elenca le funzioni di arco e cerchio IRIS GL e le relative funzioni OpenGL (GLU) equivalenti.



| Funzione IRIS GL | OpenGL (funzione)                          | Significato                 |
|------------------|------------------------------------------|-------------------------|
| **arcarcf**      | [**gluPartialDisk**](glupartialdisk.md) | Disegna un arco.           |
| **circcircf**    | [**gluDisk**](gludisk.md)               | Disegna un cerchio o un disco. |



 

È possibile eseguire alcune operazioni con archi e cerchi OpenGL che non possono essere eseguite con IRIS GL. OpenGL chiama archi e cerchi, dischi e dischi parziali rispettivamente.

Quando si portano archi e cerchi, tenere presenti i seguenti aspetti di OpenGL:

-   Gli angoli sono misurati in gradi e non in decimi di gradi.
-   L'angolo iniziale viene misurato dall'asse y positivo e non dall'asse x.
-   L'angolo di sweep è ora in senso orario anziché in senso antiorario.

??

 

 




