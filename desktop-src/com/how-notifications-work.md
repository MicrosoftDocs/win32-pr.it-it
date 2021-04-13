---
title: Come funzionano le notifiche
description: Come funzionano le notifiche
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9665b327d164a4e105f8adba3328be284fbe1fa0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399788"
---
# <a name="how-notifications-work"></a>Come funzionano le notifiche

Le notifiche hanno origine nell'applicazione oggetto e vengono propagate al contenitore tramite il gestore dell'oggetto. Se l'oggetto è un oggetto collegato, l'oggetto collegato intercetta le notifiche dal gestore dell'oggetto e notifica direttamente il contenitore.

Un'applicazione oggetto deve gestire le richieste di registrazione, tenendo traccia del punto in cui inviare le notifiche e inviare tali notifiche quando appropriato. OLE fornisce due oggetti componente per semplificare questa attività: OleAdviseHolder per le notifiche di documenti compositi e DataAdviseHolder per le notifiche dati.

Le applicazioni oggetto determinano le condizioni che richiedono l'invio di ogni notifica specifica e la frequenza con cui ogni notifica deve essere inviata. Quando è appropriato per l'invio di più notifiche, non è importante quale notifica venga inviata per prima; possono essere inviati in qualsiasi ordine.

La tempistica delle notifiche influiscono sulle prestazioni e sul coordinamento tra un'applicazione oggetto e i relativi contenitori. Mentre le notifiche hanno inviato troppo spesso un'elaborazione lenta, le notifiche inviate con una frequenza eccessiva di un contenitore non sincronizzato. La frequenza di notifica può essere confrontata con la velocità di ridisegno di un'applicazione. Pertanto, l'utilizzo di una logica simile per la tempistica delle notifiche (come viene utilizzato per il ridisegno) è consigliabile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[**CreateOleAdviseHolder**](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[Notifications](notifications.md)
</dt> </dl>

 

 