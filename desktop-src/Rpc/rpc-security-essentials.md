---
title: Concetti di base sulla sicurezza RPC
description: Per completare qualsiasi chiamata di procedura remota, tutte le applicazioni distribuite devono creare un'associazione tra il client e il server.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856766"
---
# <a name="rpc-security-essentials"></a>Concetti di base sulla sicurezza RPC

Per completare qualsiasi chiamata di procedura remota, tutte le applicazioni distribuite devono creare un'associazione tra il client e il server. Per ulteriori informazioni sulle associazioni, vedere [Binding e handle](binding-and-handles.md). Per completare una chiamata di procedura remota sicura, sono necessari passaggi aggiuntivi. In primo luogo, il server deve scegliere un provider di sicurezza (servizio di autenticazione nella terminologia DCE). Quindi deve decidere il meccanismo di autenticazione. Successivamente, il client ottiene un'associazione al server e richiede una chiamata di procedura remota sicura dal runtime RPC e specifica varie opzioni di sicurezza, ad esempio il provider di sicurezza, le opzioni QOS di sicurezza e così via.

In questa sezione vengono illustrati i concetti e le informazioni essenziali necessari per utilizzare le funzioni RPC per creare un client e un server per un'applicazione distribuita autenticata. Sono organizzati negli argomenti seguenti:

-   [Nomi principali](principal-names.md)
-   [Livelli di autenticazione](authentication-levels.md)
-   [Servizi di autenticazione](authentication-services.md)
-   [Credenziali di autenticazione client](client-authentication-credentials.md)
-   [Servizi di autorizzazione](authorization-services.md)
-   [QoS (Quality of Service)](quality-of-service.md)
-   [Funzioni di autorizzazione](authorization-functions.md)
-   [Funzioni di acquisizione chiave](key-acquisition-functions.md)
-   [Rappresentazione client](client-impersonation.md)

 

 




