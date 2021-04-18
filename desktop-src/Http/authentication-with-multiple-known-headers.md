---
title: Autenticazione con più intestazioni note
description: La \_ struttura delle \_ intestazioni note multiple http consente alle \_ applicazioni server di inviare più richieste di autenticazione al client.
ms.assetid: d517fd61-9547-4e1c-b0fd-1eb3d0098db2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8afbce3c2a41ea143003723acebc7eb83dc463d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298193"
---
# <a name="authentication-with-multiple-known-headers"></a>Autenticazione con più intestazioni note

La struttura delle [**\_ \_ \_ intestazioni note multiple http**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) consente alle applicazioni server di inviare più richieste di autenticazione al client. Le applicazioni possono richiedere al client un unico schema di autenticazione specificando il tipo di enumerazione **HttpHeaderWwwAuthenticate** nel membro **KnownHeaders** della struttura [**delle \_ \_ intestazioni di risposta http**](/windows/desktop/api/Http/ns-http-http_response_headers) contenuto [**nella \_ risposta http**](http-response.md). Tuttavia, quando il server si verifica con più schemi di autenticazione, l'applicazione usa la struttura di [**\_ \_ \_ intestazioni note multiple http**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) per fornire i tipi di autenticazione.

Quando il flag dell' **ordine di conservazione dei flag delle \_ informazioni di risposta \_ \_ \_ \_ http** è presente, http Invia le intestazioni di autenticazione nell'ordine specificato. Se il flag non è presente, HTTP Ordina gli schemi di autenticazione dal più forte al più vulnerabile come segue:

1.  Negotiate
2.  NTLM
3.  Digest
4.  Basic

Se lo schema di autenticazione non è uno di questi schemi, l'applicazione deve specificare il flag di **ordine di conservazione dei flag delle \_ informazioni di risposta \_ \_ \_ \_ http** .

Il membro **KnownHeader** di [**\_ più \_ \_ intestazioni note http**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) punta a una matrice di strutture di [**\_ \_ intestazione note http**](/windows/desktop/api/Http/ns-http-http_known_header) . Il membro **pRawValue** della struttura **di \_ \_ intestazione nota http** deve puntare a una stringa che specifica il nome dello schema. HTTP analizza la stringa per determinare lo schema ed esegue una delle azioni seguenti:

-   Se la stringa contiene un tipo di autenticazione sconosciuto o se il tipo di autenticazione non è abilitato nel gruppo di configurazione (il gruppo di URL o la sessione del server) associato alla richiesta, l'API del server HTTP aggiunge la stringa in **pRawValue** all'intestazione WWW-Authenticate. Se, ad esempio, l'applicazione specifica uno schema di autenticazione non supportato e **pRawValue** contiene la stringa "CustomAuthString", all'intestazione di autenticazione viene aggiunto il testo seguente:

    WWW-autenticazione: CustomAuthSchemeCRLF

    Se per l'applicazione non è abilitata l'autenticazione di base e **pRawValue** contiene la stringa "Basic realm =" BasicRealm "", l'intestazione Authentication contiene il testo seguente:

    WWW-Authenticate: autenticazione di base = "BasicRealm"

-   Se la stringa contiene un tipo di autenticazione noto ed è presente nel gruppo di configurazione (il gruppo di URL o la sessione del server) associata alla richiesta, l'API del server HTTP genera l'intestazione del WWW-Authenticate. Se, ad esempio, la stringa specificata in **pRawValue** è "digest" e digest è abilitato nella sessione del server, l'API del server http aggiunge il testo seguente all'intestazione di autenticazione:

    WWW-Authenticate: Realm digest = " testrealm@host.com "

Se lo schema nel membro **pRawValue** dell' [**\_ \_ intestazione nota http**](/windows/desktop/api/Http/ns-http-http_known_header) è Negotiate o NTLM, il nome dello schema di autenticazione è sufficiente. Se lo schema specificato è di base, il nome dell'area di autenticazione viene aggiunto al nome dello schema; non è necessario che l'applicazione fornisca il nome dell'area di autenticazione in **pRawValue**. Se lo schema specificato è digest, HTTP chiama [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) per generare la richiesta di verifica aggiunta al nome dello schema. I parametri per lo schema di base (area di autenticazione) e digest (area di autenticazione e nome di dominio) vengono ottenuti dalle informazioni di autenticazione del gruppo di configurazione corrispondente.

Quando l'applicazione invia più richieste di autenticazione al client in intestazioni di richiesta sconosciute, l'API server HTTP le invia al client senza intervento. Questo utilizzo non è tuttavia consigliato.

 

 




