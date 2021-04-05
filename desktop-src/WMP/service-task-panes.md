---
title: Riquadri attività servizio
description: Riquadri attività servizio
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Windows Media Player Online Stores, riquadri attività servizio
- archivi online, riquadri attività del servizio
- digitare 2 archivi online, riquadri attività servizio
- Windows Media Player Online Stores, riquadri attività
- archivi online, riquadri attività
- digitare 2 archivi online, riquadri attività
- Media Player di Windows, riquadri attività servizio
- Media Player di Windows, riquadri attività
- riquadri attività servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f882e46a7252792db5b551b25869c7711f9d31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044860"
---
# <a name="service-task-panes"></a>Riquadri attività servizio

In Windows Media Player 10, i provider di archivio online possono configurare Windows Media Player per visualizzare fino a tre riquadri attività, detti riquadri attività del servizio. Ogni riquadro attività del servizio è rappresentato da un pulsante personalizzabile visualizzato da Windows Media Player sul lato destro della barra delle applicazioni delle funzionalità.

Ogni riquadro attività del servizio ospita una pagina Web che rappresenta l'interfaccia utente per una particolare funzionalità di negozio online. L'aspetto dei riquadri attività del servizio è definito dal documento XML ServiceInfo. In questo documento i riquadri attività del servizio sono rappresentati da tre elementi: **ServiceTask1**, **ServiceTask2** e **ServiceTask3**. Questi riquadri attività del servizio sono progettati per fornire quanto segue:

-   Un servizio musicale.
-   Un servizio video.
-   Un servizio radio.

È possibile posizionare queste funzionalità in Windows Media Player in qualsiasi ordine, ma è necessario che **ServiceTask1** sia il riquadro attività principale per l'attivazione delle attività commerciali.

La pagina Web ospitata in ogni riquadro attività del servizio può accedere all'oggetto **esterno** . Questo oggetto fornisce metodi, proprietà e un evento che forniscono funzionalità speciali per le pagine Web in Windows Media Player. Ad esempio, è possibile usare l'evento e le proprietà da **External** per fare in modo che l'aspetto della pagina Web corrisponda alla combinazione di colori scelta dall'utente per Windows Media Player.

In Windows Media Player 11 non sono presenti riquadri attività del servizio. È invece disponibile una singola scheda **Store online** che ospita la pagina Web principale per lo Store online attivo. Nel documento ServiceInfo la scheda **Store online** è rappresentata dall'elemento **ServiceTask1** . gli elementi **ServiceTask2** e **ServiceTask3** vengono ignorati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sui negozi online di tipo 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Oggetto esterno per i negozi di tipo 2 online**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo per un negozio online di tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




