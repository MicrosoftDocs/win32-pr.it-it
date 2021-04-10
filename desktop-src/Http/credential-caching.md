---
title: Memorizzazione delle credenziali nella cache
description: Memorizzazione delle credenziali nella cache
ms.assetid: 6e411333-56fa-455b-a90a-f2b54f3c9545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a139d0cd90495de87f42de08687fd3157acaf6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955659"
---
# <a name="credential-caching"></a>Memorizzazione delle credenziali nella cache

## <a name="credential-caching-on-ntlm-ka-connections"></a>Memorizzazione delle credenziali nella cache per le connessioni NTLM KA

L'API server HTTP memorizza nella cache le credenziali solo per le connessioni Keep-Alive (KA) per l'autenticazione NTLM. Per impostazione predefinita, l'API server HTTP memorizza nella cache le credenziali ottenute alla prima richiesta inviata in una connessione KA. Il client può inviare richieste successive sulle connessioni KA senza un'intestazione di autorizzazione e ottenere l'autenticazione basata sul contesto precedentemente stabilito. In questo caso, l'API server HTTP invia il token in base alle credenziali memorizzate nella cache all'applicazione. Le credenziali per una richiesta inviata da un proxy non vengono memorizzate nella cache. L'applicazione Disabilita la memorizzazione nella cache delle credenziali NTLM impostando il flag **DisableNTLMCredentialCaching** nella struttura delle [**informazioni di \_ \_ autenticazione \_ del server http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) fornita nelle chiamate a HttpSetServerSessionProperty o HttpSetUrlGroupProperty. Quando la memorizzazione delle credenziali nella cache è disabilitata, l'API server HTTP ignora le credenziali memorizzate nella cache ed esegue l'autenticazione per ogni richiesta

## <a name="ntlm-credential-caching-for-specific-urls"></a>Caching delle credenziali NTLM per URL specifici

L'applicazione determina se le credenziali della richiesta restituite dall'API del server HTTP vengono memorizzate nella cache controllando il parametro Flags della \_ struttura di informazioni di autenticazione della richiesta HTTP \_ \_ . Questo parametro indica il \_ \_ \_ \_ token del flag di autenticazione della richiesta HTTP per l' \_ \_ oggetto cred memorizzato nella cache \_ quando il token NTLM restituito è stato recuperato dalla cache. La memorizzazione delle credenziali nella cache viene specificata in un gruppo di URL per tutti gli URL nel gruppo. La memorizzazione delle credenziali nella cache per URL non è supportata. Tuttavia, le applicazioni possono determinare se accettare o rifiutare le credenziali memorizzate nella cache in base all'URL controllando il \_ token del flag di autenticazione della richiesta HTTP \_ \_ \_ \_ per \_ \_ il flag cred memorizzato nella cache nella \_ struttura delle informazioni di autenticazione della richiesta HTTP \_ \_ . L'applicazione rifiuta le credenziali memorizzate nella cache inviando una richiesta di autenticazione 401 al client. Il client invia nuovamente la richiesta con le intestazioni di autorizzazione, attivando un nuovo handshake di autenticazione con l'API del server HTTP.

## <a name="basic-authentication"></a>Autenticazione di base

Quando nella richiesta viene inclusa un'intestazione di autenticazione di base, l'API del server HTTP analizza l'intestazione per ottenere il nome utente e la password. Il nome utente viene quindi analizzato nelle parti utente e dominio. L'API server HTTP memorizza nella cache il token di accesso, ottenuto per l'autenticazione di base, in base al nome utente e alla chiave di dominio. Quando viene ricevuta una nuova richiesta, l'API del server HTTP recupera il token di accesso in base al nome utente e al dominio. La password nella richiesta viene quindi controllata in base alla password memorizzata nella cache. Il token di accesso memorizzato nella cache viene eliminato quando viene raggiunto il limite TTL (time-to-Live).

 

 




