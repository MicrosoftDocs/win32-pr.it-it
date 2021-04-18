---
description: Gestione Quality-Control
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Gestione Quality-Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303702"
---
# <a name="quality-control-management"></a>Gestione Quality-Control

Il controllo qualità è un meccanismo che consente di regolare la frequenza del flusso di dati attraverso il grafico filtro in risposta alle prestazioni in fase di esecuzione. Se un filtro renderer riceve una quantità eccessiva di dati o di dati troppo piccoli, può inviare un *messaggio di qualità*. Il messaggio qualitativo richiede la regolazione della velocità dei dati. Per impostazione predefinita, i messaggi di qualità viaggiano a Monte dal renderer fino a quando non raggiungono un filtro in grado di rispondere (se presente). Un'applicazione può anche implementare un gestore di qualità personalizzato. In tal caso, il renderer passa i messaggi di qualità direttamente al gestore qualità dell'applicazione.

Questo articolo contiene gli argomenti seguenti.

-   [Messaggi di qualità](quality-messages.md)
-   [Controllo qualità predefinito](default-quality-control.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flusso di dati per sviluppatori di filtri](data-flow-for-filter-developers.md)
</dt> <dt>

[Scrittura di filtri DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



