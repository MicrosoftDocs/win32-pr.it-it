---
title: Operazioni con gli indici
description: Operazioni con gli indici
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- Windows Media Format SDK, indici
- ASF (Advanced Systems Format), indici
- ASF (formato avanzato dei sistemi), indici
- indici, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855765"
---
# <a name="working-with-indexes"></a>Operazioni con gli indici

Windows Media Format SDK supporta la ricerca e l'ingrandimento del contenuto. La ricerca consente di specificare una posizione nella sequenza temporale del file per iniziare la riproduzione. A grandi passi è possibile velocizzare e riavvolgere l'output di un file. Per sfruttare i vantaggi di queste funzionalità, è necessario indicizzare i file. Un indice è una serie di valori che rappresentano le posizioni nel file (tempi di presentazione, numeri di fotogrammi o codici temporali SMTP) con offset corrispondenti nella sezione dei dati del file per ognuno di essi. L'indicizzazione è particolarmente importante per i flussi video, in quanto il tempo di presentazione del flusso audio può essere facilmente stimato. Tuttavia, alcuni flussi audio possono richiedere anche indici. Per impostazione predefinita, ogni nuovo file ASF viene indicizzato dal writer. Se vengono apportate modifiche al contenuto di un file, è necessario aggiornare l'indice manualmente utilizzando l'oggetto indicizzatore.

L'indicizzatore supporta l'indicizzazione temporale e basata su frame, nonché l'indicizzazione basata sui codici temporali SMPTE (se presente). Per impostazione predefinita, il writer creerà un indice temporale per ogni nuovo flusso video codificato in un file. È necessario configurare e chiamare l'indicizzatore in modo esplicito per creare un indice del codice ora SMPTE o basato su frame.

Quando vengono apportate modifiche al contenuto di un file ASF, è necessario indicizzarlo di nuovo.

Nelle sezioni seguenti è presente un codice di esempio per l'esecuzione di attività di indicizzazione comuni.

-   [Per disabilitare l'indicizzazione automatica](to-disable-automatic-indexing.md)
-   [Per configurare l'indicizzatore](to-configure-the-indexer.md)
-   [Per indicizzare un file ASF](to-index-an-asf-file.md)
-   [Per arrestare l'indicizzazione in corso](to-stop-indexing-in-progress.md)

Inoltre, l'applicazione di esempio DSCopy illustra l'uso dell'indicizzatore. Per altre informazioni, vedere [applicazioni di esempio](sample-applications.md).

 

 




