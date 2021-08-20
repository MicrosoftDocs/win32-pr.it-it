---
title: Operazioni con gli indici
description: Operazioni con gli indici
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- Windows Media Format SDK, indici
- Advanced Systems Format (ASF), indexes
- ASF (Advanced Systems Format), indici
- indici, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9146913106c7824ed1557f09d277ac6928a8acfb4f3f327b0e8b7a60255ab35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027327"
---
# <a name="working-with-indexes"></a>Operazioni con gli indici

L Windows Media Format SDK supporta la ricerca e la ricerca di contenuti. La ricerca consente di specificare una posizione nella sequenza temporale del file per iniziare la riproduzione. Striding consente di inoltrare rapidamente e riavvolgere l'output di un file. I file devono essere indicizzati per sfruttare queste funzionalità. Un indice è una serie di valori che rappresentano le posizioni nel file (orari di presentazione, numeri di fotogrammi o codici di ora SMTPE) con offset corrispondenti nella sezione dei dati del file per ognuno. L'indicizzazione è più importante per i flussi video, in quanto il tempo di presentazione del flusso audio può essere facilmente stimato. Tuttavia, alcuni flussi audio possono richiedere anche indici. Per impostazione predefinita, il writer indicizza ogni nuovo file ASF. Se vengono apportate modifiche al contenuto di un file, è necessario aggiornare l'indice manualmente usando l'oggetto indicizzatore.

L'indicizzatore supporta sia l'indicizzazione temporale che basata su frame, nonché l'indicizzazione in base ai codici temporali SMPTE (se presenti). Il writer creerà un indice temporale per impostazione predefinita per ogni nuovo flusso video codificato in un file. È necessario configurare e chiamare in modo esplicito l'indicizzatore per creare un indice time code basato su frame o SMPTE.

Quando vengono apportate modifiche al contenuto di un file ASF, è necessario indicizzarlo nuovamente.

Le sezioni seguenti illustrano codice di esempio per l'esecuzione di attività di indicizzazione comuni.

-   [Per disabilitare l'indicizzazione automatica](to-disable-automatic-indexing.md)
-   [Per configurare l'indicizzatore](to-configure-the-indexer.md)
-   [Per indicizzare un file ASF](to-index-an-asf-file.md)
-   [Per arrestare l'indicizzazione in corso](to-stop-indexing-in-progress.md)

Inoltre, l'applicazione di esempio DSCopy illustra l'uso dell'indicizzatore. Per altre informazioni, vedere [Applicazioni di esempio.](sample-applications.md)

 

 




