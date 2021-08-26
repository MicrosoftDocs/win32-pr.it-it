---
title: Uso Windows agente di raccolta eventi
description: In questa sezione sono elencati gli argomenti che illustrano le attività che è possibile eseguire usando Windows Event Collector SDK. Esempi di codice e spiegazioni per tutte le attività sono inclusi in ognuno degli argomenti seguenti.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b928dddcd3e70848d510a8986962d478bedbe6f2f8bffcbec19c276983328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006011"
---
# <a name="using-windows-event-collector"></a>Uso Windows agente di raccolta eventi

In questa sezione sono elencati gli argomenti che illustrano le attività che è possibile eseguire usando Windows Event Collector SDK. Esempi di codice e spiegazioni per tutte le attività sono inclusi in ognuno degli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Creazione di una sottoscrizione avviata dall'agente di raccolta](creating-an-event-collector-subscription.md)

    Fornisce informazioni e un esempio di codice C++ per la creazione di una sottoscrizione avviata dall'agente di raccolta. Una sottoscrizione avviata dall'agente di raccolta consente di ricevere eventi in un computer locale (l'agente di raccolta eventi) che vengono inoltrati da un computer remoto (un'origine eventi).

-   [Configurazione di una sottoscrizione avviata dall'origine](setting-up-a-source-initiated-subscription.md)

    Fornisce informazioni e un esempio di codice C++ per la creazione di una sottoscrizione avviata dall'origine. Una sottoscrizione avviata dall'origine consente di ricevere eventi in un computer locale (l'agente di raccolta eventi) che vengono inoltrati da un computer remoto (un'origine eventi) senza specificare le origini eventi nella sottoscrizione.

-   [Aggiunta di un'origine evento a una sottoscrizione avviata dall'agente di raccolta](adding-an-event-source-to-an-event-collector-subscription.md)

    Fornisce informazioni e un esempio di codice C++ per l'aggiunta di un'origine evento (computer locale o computer remoto) a una sottoscrizione avviata dall'agente di raccolta. Una sottoscrizione avviata dall'agente di raccolta non può avviare la raccolta di eventi finché non viene aggiunta un'origine eventi alla sottoscrizione.

-   [Creazione di sottoscrizioni di eventi hardware](creating-hardware-event-subscriptions.md)

    Fornisce informazioni su come creare una sottoscrizione di eventi per ricevere eventi hardware da un computer in cui è installato un controller di gestione di Baseboard( BMC).

-   [Eliminazione di una sottoscrizione dell'agente di raccolta eventi](deleting-an-event-collector-subscription.md)

    Fornisce informazioni e un esempio di codice C++ per l'eliminazione di una sottoscrizione dell'agente di raccolta eventi da un computer locale.

-   [Visualizzazione delle proprietà di una sottoscrizione dell'agente di raccolta eventi](displaying-the-properties-of-an-event-collector-subscription.md)

    Fornisce informazioni e un esempio di codice C++ per visualizzare i valori delle proprietà di una sottoscrizione dell'agente di raccolta eventi. I valori delle proprietà possono fornire informazioni utili, ad esempio gli indirizzi delle origini eventi, lo stato della sottoscrizione e delle origini eventi e informazioni sul modo in cui vengono recapitati gli eventi.

-   [Visualizzazione dello stato di una sottoscrizione dell'agente di raccolta eventi](displaying-the-status-of-an-event-collector-subscription.md)

    Fornisce informazioni e un esempio di codice C++ per visualizzare lo stato di esecuzione delle origini eventi associate a una sottoscrizione dell'agente di raccolta eventi. In questo modo è possibile visualizzare i messaggi di errore che consentono di risolvere i problemi, impedendo a un'origine evento di inoltrare eventi.

-   [Elenco delle sottoscrizioni dell'agente di raccolta eventi](listing-event-collector-subscriptions.md)

    Fornisce informazioni e un esempio di codice C++ per elencare le sottoscrizioni presenti in un computer locale. È possibile usare i nomi delle sottoscrizioni ottenuti con questo esempio per eliminare una sottoscrizione, aggiungere un'origine evento a una sottoscrizione, recuperare le proprietà di una sottoscrizione o visualizzare lo stato di una sottoscrizione.

-   [Rimozione di un'origine evento da una sottoscrizione avviata dall'agente di raccolta](removing-an-event-source-from-an-event-collector-subscription.md)

    Fornisce informazioni e un esempio di codice C++ per la rimozione di un'origine evento da una sottoscrizione avviata dall'agente di raccolta. È possibile rimuovere un'origine evento da una sottoscrizione avviata dall'agente di raccolta senza disabilitare la sottoscrizione.

-   [Nuovo tentativo di una sottoscrizione dell'agente di raccolta eventi](retrying-an-event-collector-subscription.md)

    Fornisce informazioni e un esempio di codice C++ per ritentare una sottoscrizione dell'agente di raccolta eventi in caso di errore di una o più origini eventi. È possibile ritentare una singola origine eventi oppure ripetere l'intera sottoscrizione.

 

 




