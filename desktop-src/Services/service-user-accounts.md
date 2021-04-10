---
description: Ogni servizio viene eseguito nel contesto di sicurezza di un account utente.
ms.assetid: a0e48918-6957-4288-a188-d65198b38c16
title: Account utente del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c72f332b8eddbc5b5929718b6688f75e226e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884822"
---
# <a name="service-user-accounts"></a>Account utente del servizio

Ogni servizio viene eseguito nel contesto di sicurezza di un account utente. Il nome utente e la password di un account vengono specificati dalla funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) al momento dell'installazione del servizio. Il nome utente e la password possono essere modificati tramite la funzione [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . È possibile usare la funzione [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) per ottenere il nome utente, ma non la password, associato a un oggetto servizio. Gestione controllo servizi carica automaticamente il profilo utente.

Quando si avvia un servizio, SCM esegue l'accesso all'account associato al servizio. Se l'accesso ha esito positivo, il sistema produce un token di accesso e lo collega al nuovo processo del servizio. Questo token identifica il processo del servizio in tutte le interazioni successive con gli oggetti a protezione diretta (oggetti a cui è associato un descrittore di sicurezza). Se, ad esempio, il servizio tenta di aprire un handle per una pipe, il sistema confronta il token di accesso del servizio con il descrittore di sicurezza della pipe prima di concedere l'accesso.

SCM non mantiene le password degli account utente del servizio. Se una password è scaduta, l'accesso ha esito negativo e il servizio non viene avviato. L'amministratore di sistema che assegna gli account ai servizi può creare account con password senza scadenza. L'amministratore può anche gestire gli account con password che scadono usando un [programma di configurazione del servizio](service-configuration-programs.md) per modificare periodicamente le password.

Se un servizio deve riconoscere un altro servizio prima di condividerne le informazioni, il secondo servizio può usare lo stesso account del primo servizio oppure può essere eseguito in un account appartenente a un alias riconosciuto dal primo servizio. I servizi che devono essere eseguiti in modalità distribuita attraverso la rete devono essere eseguiti in account a livello di dominio.

Anziché specificare un account utente per il servizio, è possibile specificare uno degli account speciali seguenti:

-   [LocalService](localservice-account.md)
-   [NetworkService](networkservice-account.md)
-   [LocalSystem](localsystem-account.md)

 

 



