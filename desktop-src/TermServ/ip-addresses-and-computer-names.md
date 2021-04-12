---
title: Indirizzi IP e nomi di computer
description: Non è opportuno presupporre che il nome del computer o l' indirizzo IP assegnato al computer sia associato a un singolo utente poiché più utenti possono accedere contemporaneamente a un server Host sessione Desktop remoto.
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338887"
---
# <a name="ip-addresses-and-computer-names"></a>Indirizzi IP e nomi di computer

È possibile eseguire l'accesso simultaneo a più utenti a un server di host sessione Desktop remoto (host sessione Desktop remoto). Di conseguenza, non è sicuro presupporre che il nome del computer o l'indirizzo IP assegnato al computer siano associati a un singolo utente. Questo comportamento è diverso da un ambiente Windows a utente singolo, in cui solo un utente è connesso alla volta.

Le applicazioni che utilizzano il nome del computer o l'indirizzo IP per la gestione delle licenze o come mezzo per identificare un'iterazione dell'applicazione nella rete non funzioneranno correttamente in un ambiente di Servizi Desktop remoto, perché il nome del computer o l'indirizzo IP del server può essere associato a molti utenti.

In un ambiente di Servizi Desktop remoto, ogni terminale client o emulatore di terminale ha un indirizzo IP e un nome computer distinti. Per recuperare l'indirizzo IP e il nome computer di un client, chiamare la funzione [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) . Altre funzioni che recuperano questi indirizzi di rete e nomi di computer recuperano il nome e l'indirizzo del server Host sessione Desktop remoto. Ad esempio, la funzione [**presunto GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) restituisce il nome computer del server.

 

 