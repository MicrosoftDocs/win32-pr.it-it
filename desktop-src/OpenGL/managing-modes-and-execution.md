---
title: Gestione di modalità ed esecuzione
description: Gestione di modalità ed esecuzione
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, modalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427e04b856c79c9adfdfebf4061f7e96f09db835
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298054"
---
# <a name="managing-modes-and-execution"></a>Gestione di modalità ed esecuzione

L'effetto di molte funzioni OpenGL dipende dal fatto che sia attiva una modalità specifica. Le funzioni [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) impostano tali modalità; [**glIsEnabled**](glisenabled.md) determina se è impostata una modalità specifica.

È possibile controllare l'esecuzione delle funzioni OpenGL precedentemente rilasciate con [**glFinish**](glfinish.md), che impone il completamento di tutte le funzioni di questo tipo, o [**glFlush**](glflush.md), che garantisce che tutte queste funzioni verranno completate in un intervallo di tempo limitato.

In una particolare implementazione di OpenGL, potrebbe essere possibile controllare determinati comportamenti con hint usando [**glHint**](glhint.md). Questi comportamenti sono la qualità dell'interpolazione delle coordinate di trama e colore; accuratezza dei calcoli di nebbia; e la qualità di campionamento di punti, linee o poligoni con alias.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modalità e riferimento all'esecuzione](modes-and-execution-reference.md)
</dt> </dl>

 

 




