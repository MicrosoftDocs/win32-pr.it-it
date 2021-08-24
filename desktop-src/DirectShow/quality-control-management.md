---
description: Quality-Control gestione
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Quality-Control gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824410b697a29ee73fc269748595fdcae91d054a161561b282536a05dcf92ef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747711"
---
# <a name="quality-control-management"></a>Quality-Control gestione

Il controllo qualità è un meccanismo per regolare la frequenza del flusso di dati attraverso il grafico dei filtri in risposta alle prestazioni in fase di esecuzione. Se un filtro renderer riceve troppi dati o dati troppo piccoli, può inviare un messaggio *di qualità*. Il messaggio di qualità richiede una regolazione della velocità dei dati. Per impostazione predefinita, i messaggi di qualità vengono inviati a monte dal renderer fino a raggiungere un filtro in grado di rispondere (se presente). Un'applicazione può anche implementare un gestore qualità personalizzato. In tal caso, il renderer passa i messaggi di qualità direttamente al gestore della qualità dell'applicazione.

Questo articolo contiene gli argomenti seguenti.

-   [Messaggi di qualità](quality-messages.md)
-   [Controllo qualità predefinito](default-quality-control.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Data Flow per sviluppatori di filtri](data-flow-for-filter-developers.md)
</dt> <dt>

[Scrittura DirectShow filtri](writing-directshow-filters.md)
</dt> </dl>

 

 



