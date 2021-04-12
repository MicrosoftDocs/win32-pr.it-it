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
# <a name="accessing-the-reservation-store"></a><span data-ttu-id="1afa5-105">Accesso all'archivio prenotazioni</span><span class="sxs-lookup"><span data-stu-id="1afa5-105">Accessing the Reservation Store</span></span>

<span data-ttu-id="1afa5-106">L'API server HTTP gestisce l'elenco delle prenotazioni degli spazi dei nomi per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="1afa5-106">The HTTP Server API maintains the namespace reservation list for all users on the computer.</span></span> <span data-ttu-id="1afa5-107">Una voce di prenotazione è costituita da un [URLPrefix](urlprefix-strings.md) e da un ACL corrispondente.</span><span class="sxs-lookup"><span data-stu-id="1afa5-107">A reservation entry consists of a [UrlPrefix](urlprefix-strings.md) and corresponding ACL.</span></span> <span data-ttu-id="1afa5-108">Ogni UrlPrefix nell'archivio dispone di un ACL che elenca tutti gli utenti autorizzati a eseguire la registrazione per ricevere le richieste per lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="1afa5-108">Each UrlPrefix in the store has an ACL that lists all the users that are permitted to register to receive requests for the namespace.</span></span> <span data-ttu-id="1afa5-109">Gli utenti con privilegi di delega possono delegare i sottoalberi dello spazio dei nomi che possiedono ad altri utenti o eliminare le prenotazioni esistenti usando le API di configurazione.</span><span class="sxs-lookup"><span data-stu-id="1afa5-109">Users with delegation privileges can delegate subtrees of the namespace that they own to other users or delete existing reservations using the configuration APIs.</span></span>

<span data-ttu-id="1afa5-110">Per aggiungere una prenotazione all'archivio prenotazioni persistente, l'applicazione chiama la funzione [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con il parametro Configuration ID impostato sul valore **HttpServiceConfigUrlAclInfo** .</span><span class="sxs-lookup"><span data-stu-id="1afa5-110">To add a reservation to the persistent reservation store, the application calls the [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value.</span></span> <span data-ttu-id="1afa5-111">L'API server HTTP verifica la proprietà dello spazio dei nomi e l'ID utente prima di aggiungere una prenotazione all'archivio.</span><span class="sxs-lookup"><span data-stu-id="1afa5-111">The HTTP Server API verifies the ownership of the namespace and the user ID before adding a reservation to the store.</span></span>

<span data-ttu-id="1afa5-112">L'API server HTTP fornisce anche funzioni per eseguire query ed eliminare le configurazioni del servizio per gli spazi dei nomi URL.</span><span class="sxs-lookup"><span data-stu-id="1afa5-112">The HTTP Server API also supplies functions to query and delete the Service configurations for URL namespaces.</span></span> <span data-ttu-id="1afa5-113">La funzione [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) chiamata con il parametro ID configurazione è impostata sulle query del valore **HttpServiceConfigUrlAclInfo** e la funzione [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) Elimina nell'archivio dello spazio dei nomi dell'URL.</span><span class="sxs-lookup"><span data-stu-id="1afa5-113">The [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) function called with the configuration ID parameter set to the **HttpServiceConfigUrlAclInfo** value queries, and the [**HttpDeleteServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) function deletes on the URL namespace store.</span></span>

 

 




