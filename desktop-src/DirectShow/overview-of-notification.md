---
description: Panoramica della notifica degli eventi
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Panoramica della notifica degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746567"
---
# <a name="overview-of-event-notification"></a>Panoramica della notifica degli eventi

Un filtro notifica a Filter Graph Manager informazioni su un evento pubblicando una notifica degli eventi. Potrebbe trattarsi di un evento previsto, ad esempio la fine di un flusso, oppure potrebbe rappresentare un errore, ad esempio un errore di rendering di un flusso. Il gestore del grafico del filtro gestisce alcuni eventi di filtro in modo autonomo e ne lascia gli altri per la gestione dell'applicazione. Se il gestore del grafico del filtro non gestisce un evento di filtro, inserisce la notifica degli eventi in una coda. Il grafico del filtro può anche accodare le proprie notifiche degli eventi per l'applicazione.

Un'applicazione recupera gli eventi dalla coda e li risponde in base al tipo di evento. La notifica degli eventi in DirectShow è pertanto simile allo schema di Accodamento messaggi di Microsoft Windows. Un'applicazione può inoltre annullare il comportamento predefinito di Filter Graph Manager per un determinato tipo di evento. Il gestore del grafico dei filtri inserisce quindi tali eventi direttamente nella coda affinché l'applicazione venga gestita.

Questo meccanismo Abilita

-   Gestore del grafico di filtro per comunicare con l'applicazione.
-   Filtra per comunicare con l'applicazione e con il gestore del grafo dei filtri.
-   Applicazione per determinare il livello di coinvolgimento nella gestione degli eventi.

 

 



