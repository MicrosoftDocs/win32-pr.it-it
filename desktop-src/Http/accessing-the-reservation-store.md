---
title: Accesso all'archivio prenotazioni
description: L'API server HTTP gestisce l'elenco di prenotazioni dello spazio dei nomi per tutti gli utenti nel computer.
ms.assetid: 4b1291fc-cc62-4d4f-9150-18cbb1f6e5c0
keywords:
- Accesso all'HTTP dell'archivio prenotazioni
- HTTP dell'archivio prenotazioni, accesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f9244fd4513517793bf85d205308fc49ac2d8ca0a246c17a68c730d1c76168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015019"
---
# <a name="accessing-the-reservation-store"></a>Accesso all'archivio prenotazioni

L'API server HTTP gestisce l'elenco di prenotazioni dello spazio dei nomi per tutti gli utenti nel computer. Una voce di prenotazione è costituita da [un UrlPrefix](urlprefix-strings.md) e da un ACL corrispondente. Ogni UrlPrefix nell'archivio ha un elenco di controllo di accesso che elenca tutti gli utenti autorizzati a registrarsi per ricevere richieste per lo spazio dei nomi. Gli utenti con privilegi di delega possono delegare sottoalberi dello spazio dei nomi di cui sono proprietari ad altri utenti o eliminare prenotazioni esistenti usando le API di configurazione.

Per aggiungere una prenotazione all'archivio prenotazioni persistente, l'applicazione chiama la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con il parametro ID di configurazione impostato sul **valore HttpServiceConfigUrlAclInfo.** L'API server HTTP verifica la proprietà dello spazio dei nomi e l'ID utente prima di aggiungere una prenotazione all'archivio.

L'API server HTTP fornisce anche funzioni per eseguire query ed eliminare le configurazioni del servizio per gli spazi dei nomi URL. La [**funzione HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) chiamata con il parametro ID di configurazione impostato sulle query valore **HttpServiceConfigUrlAclInfo** e la funzione [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) elimina l'archivio dello spazio dei nomi URL.

 

 




