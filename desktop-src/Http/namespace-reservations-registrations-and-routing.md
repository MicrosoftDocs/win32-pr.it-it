---
title: Prenotazioni, registrazioni e routing dello spazio dei nomi
description: Prenotazione e registrazione sono le operazioni tramite le quali l'API del server HTTP concede l'accesso allo spazio dei nomi URL in un computer.
ms.assetid: dc66960b-36cd-4c09-be0a-3aec9a8a25d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00801629b5b778bb6c87a0bff615cb9d5618f57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332084"
---
# <a name="namespace-reservations-registrations-and-routing"></a>Prenotazioni, registrazioni e routing dello spazio dei nomi

Prenotazione e registrazione sono le operazioni tramite le quali l'API del server HTTP concede l'accesso allo spazio dei nomi URL in un computer. Le applicazioni possono registrarsi per una parte dello spazio dei nomi URL per soddisfare le richieste provenienti dai client HTTP. L'applicazione registra uno spazio dei nomi con l'API del server HTTP usando la funzione [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) . L'API server HTTP aggiunge gli URL alla coda delle richieste per l'applicazione e instrada le richieste alle applicazioni a seconda degli URL nelle code. Prima che l'applicazione possa registrarsi per ricevere le richieste per uno spazio dei nomi URL, tuttavia, l'amministratore di sistema deve effettuare una prenotazione per tale URL per conto dell'utente che esegue l'applicazione. Per impostazione predefinita, lo spazio dei nomi viene chiuso, ovvero solo l'amministratore può registrare prefissi URL fino a quando l'amministratore non immette una prenotazione.

Una prenotazione alloca in modo permanente una parte dello spazio dei nomi URL a singoli utenti, consentendo loro di riservare o "possedere" tale parte dello spazio dei nomi. Le prenotazioni forniscono all'utente il diritto di effettuare la registrazione alle richieste di servizio per lo spazio dei nomi. L'API server HTTP garantisce che gli utenti non registrino URL da parti dello spazio dei nomi di cui non sono proprietari. Per garantire la sicurezza dello spazio dei nomi, gli ACL (elenco di controllo di accesso) vengono applicati alla parte dello spazio dei nomi riservata per ogni utente.

Gli spazi dei nomi riservati sono identificati da stringhe di prefisso URL, formattate allo stesso modo dei prefissi URL usati per le registrazioni. Ciò significa che tutte le varie categorie di identificatori host sono disponibili anche per le prenotazioni.

Le prenotazioni dello spazio dei nomi vengono rese permanente tra i riavvii e le modifiche diventano effettive in modo dinamico, quindi non è necessario arrestare e riavviare il computer.

I concetti seguenti sono ulteriormente chiariti quando si applicano al processo di registrazione e prenotazione degli spazi dei nomi.

-   Registrazione. La registrazione è l'operazione con cui un'applicazione indica l'interesse nella ricezione di richieste per un UrlPrefix specificato. L'API per la registrazione dell'URL è [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl). La registrazione in genere si verifica durante l'avvio dell'applicazione e deve essere eseguita ogni volta che l'applicazione viene avviata.
-   ROUTING. Il routing viene eseguito dall'API del server HTTP per determinare l'applicazione a cui inviare la richiesta, in base al migliore [URLPrefix](urlprefix-strings.md) corrispondente registrato e/o riservato. L'operazione di routing utilizza le informazioni di registrazione e di prenotazione.
-   Prenotazione. Reservation alloca una parte dello spazio dei nomi URL a uno o più utenti. Questa operazione consente agli utenti di effettuare la registrazione per lo spazio dei nomi specificato. Un utente per il quale viene riservato uno spazio dei nomi viene detto "proprietario" della parte dello spazio dei nomi URL. Le prenotazioni dello spazio dei nomi vengono in genere eseguite durante l'installazione dell'applicazione e sono un'operazione poco frequente. Le prenotazioni vengono mantenute tra i riavvii del computer e richiedono privilegi di amministratore per il computer o la proprietà con privilegi di delega da creare o eliminare.
-   Delegazione. I privilegi di delega consentono a un utente che possiede uno spazio dei nomi di passare la proprietà di un sottoalbero a un altro utente da una prenotazione successiva. I privilegi di delega vengono concessi a un utente dall'amministratore di sistema quando viene effettuata la prenotazione. È possibile assegnare i privilegi di delega a uno o più utenti a uno spazio dei nomi.

 

 




