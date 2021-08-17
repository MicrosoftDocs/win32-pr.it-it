---
title: Informazioni sull'amministrazione del servizio di accesso remoto
description: Windows 2000 e versioni successive offrono un set di funzioni per l'amministrazione delle autorizzazioni utente e delle porte nei server RAS.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- Routing e Accesso remoto RRAS , Amministrazione RAS
- RRAS del servizio routing e accesso remoto, amministrazione RAS, descritto
- RRAS di amministrazione RAS
- Amministrazione RAS RRAS , descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67939d142763f45bc2eb52e959d8448904559c98357544c6c858b46e8f87a917
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792284"
---
# <a name="about-remote-access-service-administration"></a>Informazioni sull'amministrazione del servizio di accesso remoto

Windows 2000 e versioni successive offrono un set di funzioni per l'amministrazione delle autorizzazioni utente e delle porte nei server RAS. Usando queste funzioni, è possibile sviluppare un'applicazione di amministrazione del server RAS per eseguire le attività seguenti:

-   Enumerare gli utenti con un set specificato di autorizzazioni RAS
-   Assegnare o revocare le autorizzazioni RAS per un utente specificato
-   Enumerare le porte configurate in un server RAS
-   Ottenere informazioni e statistiche su una porta specificata in un server RAS
-   Reimpostare i contatori delle statistiche per una porta specificata
-   Disconnettere una porta specificata

È anche possibile installare una DLL di amministrazione del server RAS per controllare le connessioni utente e assegnare indirizzi IP agli utenti con accesso remoto. La DLL esporta un set di funzioni chiamate dal server RAS ogni volta che un utente tenta di connettersi o disconnettersi.

Questa documentazione descrive gli argomenti seguenti:

-   [Confronto tra funzioni: Windows 2000 e RRAS Redistributable](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [Amministrazione utenti RAS](ras-user-administration.md)
-   [Amministrazione di server e porte RAS](ras-server-and-port-administration.md)
-   [DLL di amministrazione RAS](ras-administration-dll.md)
-   [Configurazione del Registro di sistema della DLL di amministrazione RAS](ras-administration-dll-registry-setup.md)

 

 




