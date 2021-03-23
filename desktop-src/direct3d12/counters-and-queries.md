---
title: Contatori, query e predicazione
description: I contatori output del flusso e UAV funzionano in Direct3D 12 in un metodo simile a Direct3D 11, sebbene ora la memoria per i contatori debba essere allocata dall'app, il driver non esegue questa operazione.
ms.assetid: 8BDDAFEF-57D4-4EF5-BB0C-6C96AF557A45
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314c01b05ac31e5d5f8348b775c8955ae382f5ed
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "104548882"
---
# <a name="counters-queries-and-predication"></a>Contatori, query e predicazione

Questo argomento descrive i contatori di output di flusso, i contatori UAV, le query e predicazione.

I contatori output del flusso e UAV funzionano in Direct3D 12 in un metodo simile a Direct3D 11, sebbene ora la memoria per i contatori debba essere allocata dall'app, il driver non esegue questa operazione. Le query in Direct3D 12 sono più diverse da quelle in Direct3D 11, con l'aggiunta di barriere e altri processi che eliminano la necessità di alcuni tipi di query.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                           | Descrizione                                                                                                                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Contatori output flusso](stream-output-counters.md)<br/> | L'output del flusso è la capacità della GPU di scrivere i vertici in un buffer. Lo stato del monitoraggio dei contatori di output del flusso.<br/>                                                               |
| [Contatori UAV](uav-counters.md)<br/>                     | I contatori UAV possono essere usati per associare un contatore atomico a 32 bit a una visualizzazione non ordinata (UAV).<br/>                                                                                |
| [Query](queries.md)<br/>                               | In Direct3D 12, le query vengono raggruppate in matrici di query chiamate heap di query. Un heap di query dispone di un tipo che definisce i tipi di query validi che possono essere utilizzati con tale heap.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Misurazione delle prestazioni](performance-measurement.md)
</dt> </dl>

 

 





