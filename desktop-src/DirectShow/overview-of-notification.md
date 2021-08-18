---
description: Panoramica della notifica degli eventi
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Panoramica della notifica degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ca5e6ffb4737054f773fc5be35d56939e711442a3b31761cd23c144ed00ac1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148534"
---
# <a name="overview-of-event-notification"></a>Panoramica della notifica degli eventi

Un filtro invia una notifica a Filter Graph Manager su un evento inviando una notifica dell'evento. L'evento potrebbe essere un evento previsto, ad esempio la fine di un flusso, oppure può rappresentare un errore, ad esempio un errore durante il rendering di un flusso. Gestione filtri Graph gestisce alcuni eventi di filtro da solo e ne lascia altri che l'applicazione deve gestire. Se Filter Graph Manager non gestisce un evento di filtro, inserisce la notifica dell'evento in una coda. Il grafico dei filtri può anche accodarne le notifiche degli eventi per l'applicazione.

Un'applicazione recupera gli eventi dalla coda e risponde a essi in base al tipo di evento. La notifica degli eventi DirectShow è pertanto simile allo schema di accodamento messaggi Windows microsoft. Un'applicazione può anche annullare il comportamento Graph di Gestione filtri per un determinato tipo di evento. Gestione Graph filtra quindi inserisce tali eventi direttamente nella coda per la gestione da parte dell'applicazione.

Questo meccanismo abilita

-   Il filtro Graph Manager per comunicare con l'applicazione.
-   Filtri per comunicare sia con l'applicazione che con Filter Graph Manager.
-   Applicazione per determinarne il grado di coinvolgimento nella gestione degli eventi.

 

 



