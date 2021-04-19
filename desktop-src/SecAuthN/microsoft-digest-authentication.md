---
description: Microsoft Digest esegue un'autenticazione iniziale quando il server riceve la prima risposta di richiesta di verifica da un client.
ms.assetid: c65bb134-d480-4a71-872c-30e2884237a6
title: Autenticazione digest Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d5eb9c2d114bae70c28d07ed9fef64f9d0514
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315867"
---
# <a name="microsoft-digest-authentication"></a>Autenticazione digest Microsoft

Microsoft Digest esegue un'autenticazione iniziale quando il server riceve la prima risposta di richiesta di verifica da un client. Il server verifica che il client non sia stato autenticato, quindi esegue l'autenticazione iniziale accedendo ai servizi di un controller di dominio. Per una descrizione dettagliata di questa procedura, vedere [autenticazione iniziale con Microsoft Digest](initial-authentication-using-microsoft-digest.md).

Quando l'autenticazione iniziale ha esito positivo, il server riceve una [*chiave di sessione*](../secgloss/s-gly.md)digest. Il server memorizza nella cache la chiave e la usa per autenticare le richieste successive di risorse dal client. Questa autenticazione è locale, ovvero non richiede l'accesso a un controller di dominio. Per una descrizione dettagliata di questa procedura, vedere [autenticazione delle richieste successive con Microsoft Digest](authenticating-subsequent-requests-using-microsoft-digest.md).

Quando si usa HTTP, non viene mantenuta alcuna connessione tra il client e il server. Per ridurre il traffico del controller di dominio e migliorare le prestazioni, Microsoft Digest memorizza nella cache le informazioni ricevute dopo il completamento dell'autenticazione. Per informazioni su questo processo, vedere [gestione del contesto di sicurezza tra le connessioni](maintaining-the-security-context-between-connections.md).

 

 
