---
title: Utilizzo dell'agente di raccolta eventi di Windows
description: In questa sezione sono elencati gli argomenti che illustrano le attività che è possibile eseguire tramite l'SDK di raccolta eventi di Windows. Gli esempi di codice e le spiegazioni per tutte le attività sono inclusi in ciascuno degli argomenti seguenti.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc618ced4cefc7f17fb63b27bb1e097e65b3adac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298121"
---
# <a name="using-windows-event-collector"></a>Utilizzo dell'agente di raccolta eventi di Windows

In questa sezione sono elencati gli argomenti che illustrano le attività che è possibile eseguire tramite l'SDK di raccolta eventi di Windows. Gli esempi di codice e le spiegazioni per tutte le attività sono inclusi in ciascuno degli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Creazione di una sottoscrizione avviata dall'agente di raccolta](creating-an-event-collector-subscription.md)

    Vengono fornite informazioni e un esempio di codice C++ per la creazione di una sottoscrizione avviata dall'agente di raccolta. Una sottoscrizione avviata dall'agente di raccolta consente di ricevere gli eventi in un computer locale, ovvero l'agente di raccolta eventi, che vengono trasmessi da un computer remoto (origine evento).

-   [Configurazione di una sottoscrizione avviata dall'origine](setting-up-a-source-initiated-subscription.md)

    Vengono fornite informazioni e un esempio di codice C++ per la creazione di una sottoscrizione avviata dall'origine. Una sottoscrizione avviata dall'origine consente di ricevere eventi in un computer locale, ovvero l'agente di raccolta eventi, che vengono trasmessi da un computer remoto (origine evento) senza specificare le origini eventi nella sottoscrizione.

-   [Aggiunta di un'origine evento a una sottoscrizione avviata dall'agente di raccolta](adding-an-event-source-to-an-event-collector-subscription.md)

    Vengono fornite informazioni e un esempio di codice C++ per l'aggiunta di un'origine evento (computer locale o computer remoto) a una sottoscrizione avviata dall'agente di raccolta. Una sottoscrizione avviata dall'agente di raccolta non può iniziare a raccogliere eventi fino a quando non viene aggiunta un'origine evento alla sottoscrizione.

-   [Creazione di sottoscrizioni di eventi hardware](creating-hardware-event-subscriptions.md)

    Vengono fornite informazioni su come creare una sottoscrizione di eventi per ricevere eventi hardware da un computer in cui è installato un controller di gestione di battiscopa (BMC).

-   [Eliminazione di una sottoscrizione di raccolta eventi](deleting-an-event-collector-subscription.md)

    Fornisce informazioni e un esempio di codice C++ per l'eliminazione di una sottoscrizione di raccolta eventi da un computer locale.

-   [Visualizzazione delle proprietà di una sottoscrizione di raccolta eventi](displaying-the-properties-of-an-event-collector-subscription.md)

    Vengono fornite informazioni e un esempio di codice C++ per visualizzare i valori delle proprietà di una sottoscrizione di raccolta eventi. I valori delle proprietà possono fornire informazioni utili, ad esempio gli indirizzi delle origini eventi, lo stato della sottoscrizione e le origini eventi e le informazioni sulla modalità di recapito degli eventi.

-   [Visualizzazione dello stato di una sottoscrizione dell'agente di raccolta eventi](displaying-the-status-of-an-event-collector-subscription.md)

    Fornisce informazioni e un esempio di codice C++ per visualizzare lo stato della fase di esecuzione delle origini eventi associate a una sottoscrizione dell'agente di raccolta eventi. Questo consente di visualizzare i messaggi di errore che consentono di risolvere i problemi che impediscono l'invio di eventi da un'origine evento.

-   [Elenco delle sottoscrizioni degli agenti di raccolta eventi](listing-event-collector-subscriptions.md)

    Vengono fornite informazioni e un esempio di codice C++ per elencare le sottoscrizioni esistenti in un computer locale. È possibile utilizzare i nomi delle sottoscrizioni ottenuti con questo esempio per eliminare una sottoscrizione, aggiungere un'origine evento a una sottoscrizione, recuperare le proprietà di una sottoscrizione o visualizzare lo stato di una sottoscrizione.

-   [Rimozione di un'origine evento da una sottoscrizione avviata dall'agente di raccolta](removing-an-event-source-from-an-event-collector-subscription.md)

    Vengono fornite informazioni e un esempio di codice C++ per la rimozione di un'origine evento da una sottoscrizione avviata dall'agente di raccolta. È possibile rimuovere un'origine evento da una sottoscrizione avviata dall'agente di raccolta senza disabilitare la sottoscrizione.

-   [Nuovo tentativo di sottoscrizione di un agente di raccolta eventi](retrying-an-event-collector-subscription.md)

    Fornisce informazioni e un esempio di codice C++ per ritentare una sottoscrizione dell'agente di raccolta eventi quando una o più origini evento non sono riuscite. È possibile ritentare una singola origine evento oppure ritentare l'intera sottoscrizione.

 

 




