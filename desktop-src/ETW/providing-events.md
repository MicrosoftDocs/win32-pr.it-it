---
description: I provider sono applicazioni che contengono la strumentazione di traccia eventi.
ms.assetid: b522f16d-8d61-4db3-9194-d965b6d859ec
title: Invio di eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc53daa602662dfabd163560e8e9d69a888be610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977634"
---
# <a name="providing-events"></a>Invio di eventi

I provider sono applicazioni che contengono la strumentazione di traccia eventi. Dopo la registrazione di un provider, un controller può quindi abilitare o disabilitare la traccia eventi nel provider. Il provider definisce l'interpretazione dell'abilitazione o disabilitazione. In genere, un provider abilitato genera eventi e un provider disabilitato non lo consente. In questo modo è possibile aggiungere la traccia eventi all'applicazione senza che sia necessario generare eventi sempre.

Questa sezione illustra come eseguire le operazioni seguenti:

-   [Eventi di scrittura](writing-events.md)
-   [Scrivi eventi correlati](writing-related-events-in-an-end-to-end-scenario.md)
-   [Pubblicare lo schema dell'evento da condividere con gli utenti](publishing-your-event-schema.md)

Per informazioni sul controllo delle sessioni di traccia eventi, vedere [controllo delle sessioni di traccia eventi](controlling-event-tracing-sessions.md). Per informazioni sull'utilizzo di eventi da un provider di traccia eventi, vedere [utilizzo degli eventi](consuming-events.md).

 

 



