---
description: Questa sezione descrive come pianificare, sviluppare e testare le pagine di riferimento degli eventi e come distribuirle in un esperto o in un monitoraggio. Per informazioni sugli EERP e su come usarli con Network Monitor, vedere Pagina di riferimento eventi.
ms.assetid: 78d6e8cf-785e-4d5f-a78d-9ef9da9bc3e0
title: Creazione di pagine di riferimento per gli eventi expert e monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5826ab0aaa71461f6b4e56b9330e00c5af6aae26952d84af88c380da6dfe41fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144234"
---
# <a name="creating-expert-and-monitor-event-reference-pages"></a>Creazione di pagine di riferimento per gli eventi expert e monitor

Questa sezione descrive come pianificare, sviluppare e testare le pagine di riferimento degli eventi e come distribuirle in un esperto o in un monitoraggio. Per informazioni sugli EERP e su come usarli con Network Monitor, vedere [Pagina di](event-reference-page.md)riferimento eventi .

Per sviluppare un nuovo ERP, il primo passaggio consiste nel determinare gli eventi che richiedono singoli ERP per l'esperto o [il](experts.md) [monitoraggio personalizzato.](monitors.md) È necessario creare EP separati per ogni evento che si vuole visualizzare nel Network Monitor Visualizzatore eventi. Si supponga, ad esempio, che:

-   Si sviluppa un monitoraggio denominato Game Monitor e Stock Watcher.
-   Il monitoraggio si trova in un file denominato Gamemon.dll.
-   Il monitoraggio genera due eventi, Game Running e My Internet Stock Soars.
-   Si prevede di sviluppare due EP, Gamemon1.htm e Gamemon2.htm.

> [!Note]  
> Non è necessario avere una corrispondenza uno-a-uno di EP per monitorare o eventi esperti.

 

Dopo aver stabilito un elenco di ERP univoci, seguire questa procedura per creare ogni ERP.

-   [Scrivere il documento di origine HTML](writing-an-event-reference-page.md).
-   [Salvare e assegnare](naming-an-event-reference-page.md) un nome al file di origine HTML come .htm file.
-   [Testare il programma ERP](testing-an-event-reference-page.md) con l'esperto o il monitoraggio completato.

 

 



