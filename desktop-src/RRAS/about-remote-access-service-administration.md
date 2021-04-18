---
title: Informazioni sull'amministrazione del servizio di accesso remoto
description: I sistemi operativi Windows 2000 e versioni successive forniscono un set di funzioni per l'amministrazione delle autorizzazioni e delle porte utente nei server RAS.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- Servizio Routing e accesso remoto RRAS, amministrazione RAS
- Servizio Routing e accesso remoto RRAS, amministrazione RAS, descrizione
- RRAS amministrazione RAS
- Amministrazione RAS RRAS, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298295"
---
# <a name="about-remote-access-service-administration"></a>Informazioni sull'amministrazione del servizio di accesso remoto

I sistemi operativi Windows 2000 e versioni successive forniscono un set di funzioni per l'amministrazione delle autorizzazioni e delle porte utente nei server RAS. Utilizzando queste funzioni, è possibile sviluppare un'applicazione di amministrazione del server RAS per eseguire le attività seguenti:

-   Enumerare gli utenti che dispongono di un set specificato di autorizzazioni RAS
-   Assegnare o revocare le autorizzazioni RAS per un utente specificato
-   Enumerare le porte configurate in un server RAS
-   Ottenere informazioni e statistiche su una porta specificata in un server RAS
-   Reimposta i contatori delle statistiche per una porta specificata
-   Disconnettere una porta specificata

È anche possibile installare una DLL di amministrazione del server RAS per controllare le connessioni utente e assegnare gli indirizzi IP agli utenti con connessione remota. La DLL esporta un set di funzioni che il server RAS chiama ogni volta che un utente tenta di connettersi o disconnettersi.

In questa documentazione vengono descritti gli argomenti seguenti:

-   [Confronto tra le funzioni: Windows 2000 e RRAS ridistribuibile](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [Amministrazione utenti RAS](ras-user-administration.md)
-   [Amministrazione di server e porte RAS](ras-server-and-port-administration.md)
-   [DLL di amministrazione RAS](ras-administration-dll.md)
-   [Configurazione del registro di sistema della DLL di amministrazione RAS](ras-administration-dll-registry-setup.md)

 

 




