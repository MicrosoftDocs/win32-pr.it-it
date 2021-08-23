---
title: Funzionamento delle notifiche
description: Funzionamento delle notifiche
ms.assetid: faf66654-8233-49ac-a0fa-6cae51df0bea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e90dfeb6e1df6de50ddaa3264a8c5475d280f30a72ad2d8c6acfffd39d60fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756371"
---
# <a name="how-notifications-work"></a>Funzionamento delle notifiche

Le notifiche hanno origine nell'applicazione dell'oggetto e vengono inviate al contenitore tramite il gestore dell'oggetto. Se l'oggetto è un oggetto collegato, l'oggetto collegato intercetta le notifiche dal gestore dell'oggetto e invia una notifica direttamente al contenitore.

Un'applicazione oggetto deve gestire le richieste di registrazione, tenendo traccia di dove inviare le notifiche e inviando tali notifiche quando appropriato. OLE fornisce due oggetti componente per semplificare questa attività: OleAdviseHolder per le notifiche di documenti composti e DataAdviseHolder per le notifiche dei dati.

Le applicazioni oggetto determinano le condizioni che determinano l'invio di ogni notifica specifica e la frequenza con cui ogni notifica deve essere inviata. Quando è appropriato per l'invio di più notifiche, non è importante quale notifica viene inviata per prima; possono essere inviati in qualsiasi ordine.

La tempistica delle notifiche influisce sulle prestazioni e sul coordinamento tra un'applicazione oggetto e i relativi contenitori. Mentre le notifiche inviate troppo spesso rallentano l'elaborazione, le notifiche inviate troppo raramente comportano un contenitore non sincronizzato. La frequenza di notifica può essere confrontata con la frequenza di ridisegno di un'applicazione. Pertanto, è opportuno usare una logica simile per la tempistica delle notifiche (come viene usata per il ridisegno).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)
</dt> <dt>

[**CreateOleAdviseHolder**](/windows/desktop/api/Ole2/nf-ole2-createoleadviseholder)
</dt> <dt>

[Notifications](notifications.md)
</dt> </dl>

 

 