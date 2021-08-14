---
description: Microsoft Digest esegue un'autenticazione iniziale quando il server riceve la prima risposta di richiesta da un client.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Autenticazione digest Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 135e5374515acb0604ee14a6770b9523e9bf31fd0e2d6c946fec26d2ad789c2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921830"
---
# <a name="microsoft-digest-authentication"></a>Autenticazione digest Microsoft

Microsoft Digest esegue un'autenticazione iniziale quando il server riceve la prima risposta di richiesta da un client. Il server verifica che il client non sia stato autenticato e quindi esegue l'autenticazione iniziale accedendo ai servizi di un controller di dominio. Per una descrizione dettagliata di questa procedura, vedere [Initial Authentication Using Microsoft Digest](initial-authentication-using-microsoft-digest.md).

Quando l'autenticazione iniziale ha esito positivo, il server riceve una chiave [*di sessione digest*](../secgloss/s-gly.md). Il server memorizza nella cache questa chiave e la usa per autenticare le richieste successive di risorse dal client. Questa autenticazione è locale, cio' non richiede l'accesso a un controller di dominio. Per una descrizione dettagliata di questa procedura, vedere [Autenticazione delle richieste successive tramite Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

Quando si usa HTTP, non viene mantenuta alcuna connessione tra client e server. Per ridurre il traffico del controller di dominio e migliorare le prestazioni, Microsoft Digest memorizza nella cache le informazioni ricevute dopo l'autenticazione. Per informazioni su questo processo, vedere [Gestione del contesto di sicurezza tra le connessioni](maintaining-the-security-context-between-connections.md).

 

 
