---
title: Prestare attenzione ad altri endpoint RPC in esecuzione nello stesso processo
description: Quando un'applicazione si trova in un processo con altri server RPC, tutte le applicazioni restano in attesa su tutti i protocolli.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00828ddf95fd024069a8a535c95673eb014d84b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711572"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a>Prestare attenzione ad altri endpoint RPC in esecuzione nello stesso processo

Quando un'applicazione si trova in un processo con altri server RPC, tutte le applicazioni restano in attesa su tutti i protocolli. Di conseguenza, se un componente chiama solo [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) \* per LRPC, non è necessariamente accessibile solo su LRPC. Può essere accessibile tramite altri protocolli, dal momento che altri server RPC nel processo potrebbero essere in ascolto su pipe o socket (ad esempio).

Analogamente agli handle di contesto rigorosi, non l'inserimento di un altro endpoint nel processo non significa che un altro endpoint non esiste. Indipendentemente dalla modalità di registrazione del server, non esiste un'associazione speciale tra l'interfaccia e l'endpoint. tutte le interfacce possono essere richiamate su tutti gli endpoint in tale processo. Questo è un altro motivo per cui il modello di sicurezza degli endpoint non è efficace; Se un descrittore di sicurezza viene inserito in un endpoint, gli utenti malintenzionati possono chiamare l'interfaccia su un altro endpoint.

Per assicurarsi che un processo venga chiamato solo su una sequenza di protocollo specifica, registrare una funzione di callback di sicurezza e, in tale funzione, controllare la sequenza di protocollo effettuata dalla chiamata.

 

 




