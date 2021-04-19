---
description: Il materiale seguente fornisce linee guida sull'uso di TAPI per scrivere applicazioni per le comunicazioni tra l'utente finale e il server. Queste informazioni sono inoltre estremamente rilevanti per i programmatori del provider di servizi.
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: Applicazioni TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317642"
---
# <a name="tapi-applications"></a>Applicazioni TAPI

Il materiale seguente fornisce linee guida sull'uso di TAPI per scrivere applicazioni per le comunicazioni tra l'utente finale e il server. Queste informazioni sono inoltre estremamente rilevanti per i programmatori del provider di servizi.

La prima decisione che un programmatore deve eseguire nell'uso di TAPI è il livello di servizio necessario. Se, ad esempio, un'applicazione richiede una selezione di menu che può comporre un numero di telefono, probabilmente non è necessaria un'applicazione TAPI completa. La telefonia assistita consente di abilitare questa opzione in modo rapido e semplice. Per ulteriori informazioni sulla distinzione tra le applicazioni TAPI complete e la telefonia assistita, vedere [livelli di servizio TAPI](tapi-levels-of-service.md) .

La seconda decisione importante è se usare TAPI 2. x, l'API basata su C o TAPI 3. x, basata su COM. Vedere [TAPI 3. x e TAPI 2. x](tapi-3-x-versus-tapi-2-x.md) per una descrizione delle considerazioni importanti per decidere quale usare.

Il diagramma seguente illustra i blocchi predefiniti di base di un'applicazione TAPI completa. TAPI 2. x e TAPI 3. x sono entrambi trattati in queste sezioni. Il materiale che è molto specifico per uno viene trattato nelle sezioni Panoramica per TAPI 2. x o TAPI 3. x.

![blocchi predefiniti di un'applicazione TAPI](images/tapior3.png)

I collegamenti seguenti forniscono contenuto che corrisponde alle figure nell'immagine precedente:

| Figura | Documentazione                                                                    |
|--------|----------------------------------------------------------------------------------|
| 1      | [Inizializzazione TAPI](tapi-initialization.md)                                   |
| 2      | [Controllo della sessione](session-control.md)                                           |
| 3      | [Controllo dei dispositivi](device-control.md)                                             |
| 4      | [Controllo multimediale](media-control.md)                                               |
| 5      | [Informazioni sui controlli Call Center](about-call-center-controls.md)                     |
| 6      | [Conferenza telefonica IP Rendezvous](rendezvous-ip-telephony-conferencing.md) |
| 7      | [Arresto TAPI](tapi-shutdown.md)                                               |



 

 

 



