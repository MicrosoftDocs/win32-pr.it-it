---
title: Informazioni di base sulla sicurezza RPC
description: Per completare qualsiasi chiamata di procedura remota, tutte le applicazioni distribuite devono creare un'associazione tra il client e il server.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ed8bce6f97ecfc7bd257d20eebbb35d068624fe017c01a662b47fceb463b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926032"
---
# <a name="rpc-security-essentials"></a>Informazioni di base sulla sicurezza RPC

Per completare qualsiasi chiamata di procedura remota, tutte le applicazioni distribuite devono creare un'associazione tra il client e il server. Per altre informazioni sulle associazioni, vedere [Binding e handle.](binding-and-handles.md) Per completare una chiamata di procedura remota sicura, sono necessari passaggi aggiuntivi. In primo luogo, il server deve scegliere un provider di sicurezza (servizio di autenticazione nella terminologia DCE). Deve quindi decidere il meccanismo di autenticazione. Successivamente, il client ottiene un'associazione al server e richiede una chiamata di procedura remota protetta dal tempo di esecuzione RPC e specifica varie opzioni di sicurezza, ad esempio il provider di sicurezza, le opzioni QOS di sicurezza e così via.

In questa sezione vengono illustrati i concetti fondamentali e le informazioni necessarie per utilizzare le funzioni RPC per creare un client e un server per un'applicazione distribuita autenticata. È organizzato negli argomenti seguenti:

-   [Nomi delle entità](principal-names.md)
-   [Livelli di autenticazione](authentication-levels.md)
-   [Servizi di autenticazione](authentication-services.md)
-   [Credenziali di autenticazione client](client-authentication-credentials.md)
-   [Servizi di autorizzazione](authorization-services.md)
-   [QoS (Quality of Service)](quality-of-service.md)
-   [Funzioni di autorizzazione](authorization-functions.md)
-   [Funzioni di acquisizione delle chiavi](key-acquisition-functions.md)
-   [Rappresentazione client](client-impersonation.md)

 

 




