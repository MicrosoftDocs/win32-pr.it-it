---
title: Accesso all'archivio prenotazioni
description: L'API server HTTP gestisce l'elenco delle prenotazioni degli spazi dei nomi per tutti gli utenti del computer.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Accesso all'archivio prenotazioni HTTP
- Archivio prenotazioni HTTP, accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a138a0a2385e6338877e5e8623527a64a6eca796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396007"
---
# <a name="accessing-the-reservation-store"></a>Accesso all'archivio prenotazioni

L'API server HTTP gestisce l'elenco delle prenotazioni degli spazi dei nomi per tutti gli utenti del computer. Una voce di prenotazione è costituita da un [URLPrefix](urlprefix-strings.md) e da un ACL corrispondente. Ogni UrlPrefix nell'archivio dispone di un ACL che elenca tutti gli utenti autorizzati a eseguire la registrazione per ricevere le richieste per lo spazio dei nomi. Gli utenti con privilegi di delega possono delegare i sottoalberi dello spazio dei nomi che possiedono ad altri utenti o eliminare le prenotazioni esistenti usando le API di configurazione.

Per aggiungere una prenotazione all'archivio prenotazioni persistente, l'applicazione chiama la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con il parametro Configuration ID impostato sul valore **HttpServiceConfigUrlAclInfo** . L'API server HTTP verifica la proprietà dello spazio dei nomi e l'ID utente prima di aggiungere una prenotazione all'archivio.

L'API server HTTP fornisce anche funzioni per eseguire query ed eliminare le configurazioni del servizio per gli spazi dei nomi URL. La funzione [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) chiamata con il parametro ID configurazione è impostata sulle query del valore **HttpServiceConfigUrlAclInfo** e la funzione [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) Elimina nell'archivio dello spazio dei nomi dell'URL.

 

 




