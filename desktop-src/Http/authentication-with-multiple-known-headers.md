---
title: Autenticazione con più intestazioni note
description: La struttura \_ HTTP MULTIPLE KNOWN HEADERS consente alle applicazioni server di \_ \_ inviare più richieste di autenticazione al client.
ms.assetid: d517fd61-9547-4e1c-b0fd-1eb3d0098db2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb8fd2071626d8a12f046ac0c3b6c50fcffc794462d5109a89a974f441879bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950930"
---
# <a name="authentication-with-multiple-known-headers"></a>Autenticazione con più intestazioni note

La [**struttura HTTP MULTIPLE KNOWN \_ \_ \_ HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) consente alle applicazioni server di inviare più richieste di autenticazione al client. Le applicazioni possono eseguire una richiesta al client con un singolo schema di autenticazione fornendo il tipo di enumerazione **HttpHeaderWwwAuthenticate** nel membro **KnownHeaders** della struttura [**HTTP RESPONSE \_ \_ HEADERS**](/windows/desktop/api/Http/ns-http-http_response_headers) contenuta in [**HTTP \_ RESPONSE.**](http-response.md) Tuttavia, quando il server verifica più schemi di autenticazione, l'applicazione usa la [**struttura HTTP MULTIPLE KNOWN \_ \_ \_ HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) per fornire i tipi di autenticazione.

Quando è presente il flag **HTTP RESPONSE INFO FLAGS PRESERVE \_ \_ \_ \_ \_ ORDER,** HTTP invia le intestazioni di autenticazione nell'ordine specificato. Se il flag non è presente, HTTP ordina gli schemi di autenticazione dal più forte al più debole come segue:

1.  Negotiate
2.  NTLM
3.  Digest
4.  Basic

Se lo schema di autenticazione non è uno di questi schemi, l'applicazione deve specificare il flag **HTTP RESPONSE INFO FLAGS PRESERVE \_ \_ \_ \_ \_ ORDER.**

Il **membro KnownHeader** di [**HTTP MULTIPLE KNOWN \_ \_ \_ HEADERS**](/windows/desktop/api/Http/ns-http-http_multiple_known_headers) punta a una matrice di [**strutture HTTP KNOWN \_ \_ HEADER.**](/windows/desktop/api/Http/ns-http-http_known_header) Il **membro pRawValue** della struttura **HTTP KNOWN \_ \_ HEADER** deve puntare a una stringa che specifica il nome dello schema. HTTP analizza la stringa per determinare lo schema ed esegue una delle azioni seguenti:

-   Se la stringa contiene un tipo di autenticazione sconosciuto o se il tipo di autenticazione non è abilitato nel gruppo di configurazione (gruppo di URL o sessione del server) associato alla richiesta, l'API del server HTTP aggiunge la stringa in **pRawValue** all'intestazione WWW-Authenticate. Ad esempio, se l'applicazione specifica uno schema di autenticazione non supportato e **pRawValue** contiene la stringa "CustomAuthString", all'intestazione di autenticazione viene aggiunto il testo seguente:

    WWW-Authenticate: CustomAuthSchemeCRLF

    Se per l'applicazione non è abilitata l'autenticazione di base e **pRawValue** contiene la stringa "Basic realm="BasicRealm"", l'intestazione di autenticazione contiene il testo seguente:

    WWW-Authenticate: Basic realm="BasicRealm"

-   Se la stringa contiene un tipo di autenticazione noto ed è presente nel gruppo di configurazione (gruppo di URL o sessione del server) associato alla richiesta, l'API del server HTTP genera l'intestazione WWW-Authenticate richiesta. Ad esempio, se la stringa specificata in **pRawValue** è "Digest" e digest è abilitato nella sessione del server, l'API del server HTTP aggiunge il testo seguente all'intestazione di autenticazione:

    WWW-Authenticate: Digest realm=" testrealm@host.com "

Se lo schema nel membro **pRawValue** di [**HTTP KNOWN \_ \_ HEADER**](/windows/desktop/api/Http/ns-http-http_known_header) è Negotiate o NTLM, il nome dello schema di autenticazione è sufficiente. Se lo schema specificato è Basic, il nome dell'area di autenticazione viene aggiunto al nome dello schema. L'applicazione non deve specificare il nome dell'area di autenticazione in **pRawValue.** Se lo schema specificato è Digest, HTTP chiama [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) per generare la richiesta di verifica aggiunta al nome dello schema. I parametri per lo schema Di base (area di autenticazione) e Digest (area di autenticazione e nome di dominio) vengono ottenuti dalle informazioni di autenticazione del gruppo di configurazione corrispondenti.

Quando l'applicazione invia più richieste di autenticazione al client in Intestazioni di richiesta sconosciute, l'API del server HTTP li invia al client senza intervento dell'utente. Tuttavia, questo utilizzo non è consigliato.

 

 




