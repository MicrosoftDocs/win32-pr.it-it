---
title: Reflection del messaggio
description: Reflection del messaggio
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044035"
---
# <a name="message-reflection"></a>Reflection del messaggio

Si consiglia vivamente che un contenitore di controlli ActiveX supporti la reflection del messaggio. Questo comporterà un'operazione più efficiente per i controlli sottoclassati. Se è supportata la reflection del messaggio, la proprietà di ambiente MessageReflect deve essere supportata e avere un valore **true**. Se un contenitore non implementa la reflection del messaggio, il CDK OLE crea due finestre per ogni controllo sottoclassato, per fornire la reflection del messaggio per conto del contenitore di controlli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

 




