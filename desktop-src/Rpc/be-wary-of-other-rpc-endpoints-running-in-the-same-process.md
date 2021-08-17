---
title: Diffidato da altri endpoint RPC in esecuzione nello stesso processo
description: Quando un'applicazione risiede in un processo con altri server RPC, tutte le applicazioni sono in ascolto su tutti i protocolli.
ms.assetid: edb20108-e0c3-4b9b-b57d-45a96d9472ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e2044b83de96a352546d90c45cd54879fc87923786b7852133ffeb28dbf9cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932352"
---
# <a name="be-wary-of-other-rpc-endpoints-running-in-the-same-process"></a>Diffidato da altri endpoint RPC in esecuzione nello stesso processo

Quando un'applicazione risiede in un processo con altri server RPC, tutte le applicazioni sono in ascolto su tutti i protocolli. Di conseguenza, se un componente chiama [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) solo per LRPC, non è necessariamente \* accessibile solo tramite LRPC. Può essere accessibile tramite altri protocolli, poiché altri server RPC nel processo possono essere in ascolto su pipe o socket (ad esempio).

Analogamente agli handle di contesto rigorosi, non inserire un altro endpoint nel processo non significa che non esista un altro endpoint. Indipendentemente dalla modalità di registrazione del server, non esiste alcuna associazione speciale tra l'interfaccia e l'endpoint. tutte le interfacce sono richiamabili su tutti gli endpoint del processo. Questo è un altro motivo per cui il modello di sicurezza degli endpoint è inefficace; se un descrittore di sicurezza viene inserito in un endpoint, gli utenti malintenzionati possono chiamare l'interfaccia su un altro endpoint.

Per assicurarsi che un processo sia chiamato solo in una sequenza di protocollo specifica, registrare una funzione di callback di sicurezza e in tale funzione controllare la sequenza di protocollo in cui viene effettuata la chiamata.

 

 




