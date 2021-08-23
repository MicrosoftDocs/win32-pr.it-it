---
description: Ogni servizio viene eseguito nel contesto di sicurezza di un account utente.
ms.assetid: a0e48918-6957-4288-a188-d65198b38c16
title: Account utente del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6053a4f870b2a49923d802f7cb5f2a45b786d63314d1010773c3e8f58627bec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888548"
---
# <a name="service-user-accounts"></a>Account utente del servizio

Ogni servizio viene eseguito nel contesto di sicurezza di un account utente. Il nome utente e la password di un account vengono specificati dalla [**funzione CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) al momento dell'installazione del servizio. Il nome utente e la password possono essere modificati usando la [**funzione ChangeServiceConfig.**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) È possibile usare la [**funzione QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) per ottenere il nome utente (ma non la password) associato a un oggetto servizio. Gestione controllo servizi carica automaticamente il profilo utente.

Quando si avvia un servizio, Gestione controllo servizi accede all'account associato al servizio. Se l'accesso ha esito positivo, il sistema produce un token di accesso e lo collega al nuovo processo del servizio. Questo token identifica il processo del servizio in tutte le interazioni successive con oggetti a protezione diretta (oggetti a cui è associato un descrittore di sicurezza). Ad esempio, se il servizio tenta di aprire un handle a una pipe, il sistema confronta il token di accesso del servizio con il descrittore di sicurezza della pipe prima di concedere l'accesso.

Gestione controllo servizi non gestisce le password degli account utente del servizio. Se una password è scaduta, l'accesso ha esito negativo e l'avvio del servizio non riesce. L'amministratore di sistema che assegna gli account ai servizi può creare account con password che non scadono mai. L'amministratore può anche gestire gli account con password che scadono usando un programma di [configurazione del servizio](service-configuration-programs.md) per modificare periodicamente le password.

Se un servizio deve riconoscere un altro servizio prima di condividere le informazioni, il secondo servizio può usare lo stesso account del primo servizio oppure può essere eseguito in un account appartenente a un alias riconosciuto dal primo servizio. I servizi che devono essere eseguiti in modo distribuito nella rete devono essere eseguiti in account a livello di dominio.

È possibile specificare uno degli account speciali seguenti invece di specificare un account utente per il servizio:

-   [LocalService](localservice-account.md)
-   [NetworkService](networkservice-account.md)
-   [LocalSystem](localsystem-account.md)

 

 



