---
title: Gestione delle modalità e dell'esecuzione
description: Gestione delle modalità e dell'esecuzione
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, modalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec448fa94c8ed0983be68f8aa1dbbef0974d2e040c4f68b002b026b300406981
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553981"
---
# <a name="managing-modes-and-execution"></a>Gestione delle modalità e dell'esecuzione

L'effetto di molte funzioni OpenGL dipende dal fatto che sia attiva una particolare modalità. Le [**funzioni glEnable**](glenable.md) [**e glDisable**](gldisable.md) impostano tali modalità. [**glIsEnabled determina**](glisenabled.md) se è impostata una particolare modalità.

È possibile controllare l'esecuzione di funzioni OpenGL rilasciate in precedenza con [**glFinish**](glfinish.md), che forza il completamento di tutte queste funzioni, o [**glFlush**](glflush.md), che garantisce che tutte queste funzioni verranno completate in un tempo finito.

In una particolare implementazione di OpenGL, è possibile controllare determinati comportamenti con hint usando [**glHint**](glhint.md). Tali comportamenti sono la qualità dell'interpolazione delle coordinate di colore e trama; l'accuratezza dei calcoli della nebbia; e la qualità di campionamento di punti, linee o poligoni con antialias.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su modalità ed esecuzione](modes-and-execution-reference.md)
</dt> </dl>

 

 




