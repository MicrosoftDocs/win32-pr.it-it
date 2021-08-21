---
title: Reflection dei messaggi
description: Reflection dei messaggi
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9191e0e189f8653518aaabb3c31785cde960538b0828d56669096ebf1d63f1e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048049"
---
# <a name="message-reflection"></a>Reflection dei messaggi

È consigliabile che un contenitore ActiveX di controllo supporti la reflection dei messaggi. Ciò comporta un'operazione più efficiente per i controlli sottoclassati. Se la reflection del messaggio è supportata, la proprietà di ambiente MessageReflect deve essere supportata e il valore **è TRUE.** Se un contenitore non implementa la reflection dei messaggi, la chiave CDK OLE crea due finestre per ogni controllo sottoclassato, per fornire la reflection del messaggio per conto del contenitore del controllo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contenitori](containers.md)
</dt> </dl>

 

 




