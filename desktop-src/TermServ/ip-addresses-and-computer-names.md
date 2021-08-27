---
title: Indirizzi IP e nomi di computer
description: Non è opportuno presupporre che il nome del computer o l' indirizzo IP assegnato al computer sia associato a un singolo utente poiché più utenti possono accedere contemporaneamente a un server Host sessione Desktop remoto.
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45aa6027a5cf7714d2d88fd3527182d5586982e02417e5ddb26ea3c086b9219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129538"
---
# <a name="ip-addresses-and-computer-names"></a>Indirizzi IP e nomi di computer

È possibile accedere contemporaneamente a più utenti a Desktop remoto server Host sessione Desktop remoto. Di conseguenza, non è sicuro presupporre che il nome del computer o l'indirizzo IP assegnato al computer siano associati a un singolo utente. Questo comportamento è diverso da quello di un Windows utente singolo, in cui è connesso un solo utente alla volta.

Le applicazioni che usano il nome del computer o l'indirizzo IP per le licenze o per identificare un'iterazione dell'applicazione in rete non funzioneranno correttamente in un ambiente Servizi Desktop remoto, perché il nome computer o l'indirizzo IP del server può essere associato a molti utenti.

In un ambiente Servizi Desktop remoto, ogni terminale client o emulatore del terminale ha un indirizzo IP e un nome computer separati. Per recuperare l'indirizzo IP e il nome del computer di un client, chiamare la [**funzione WTSQuerySessionInformation.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) Altre funzioni che recuperano questi indirizzi di rete e nomi di computer recuperano il nome e l'indirizzo del server Host sessione Desktop remoto. Ad esempio, la [**funzione GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) restituisce il nome computer del server.

 

 