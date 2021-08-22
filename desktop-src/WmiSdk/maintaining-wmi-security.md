---
description: La sicurezza WMI è incentrata sulla protezione dell'accesso ai dati dello spazio dei nomi. WMI concede innanzitutto l'accesso a gruppi di utenti come specificato dalle impostazioni di Controllo WMI e DCOM e quindi i provider determinano se l'utente deve avere accesso ai dati dello spazio dei nomi.
ms.assetid: 88a2538a-ae30-4a1a-9d16-f0cd9419b2ed
ms.tgt_platform: multiple
title: Gestione della sicurezza WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79467b3baffd030cae1022f65bc0b8a97242c5e8bbe2f870753a3d3794b8705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118818419"
---
# <a name="maintaining-wmi-security"></a>Gestione della sicurezza WMI

La sicurezza WMI è incentrata sulla protezione dell'accesso ai dati dello spazio dei nomi. WMI concede innanzitutto l'accesso a gruppi di utenti come specificato dalle impostazioni di Controllo [*WMI*](gloss-w.md) e DCOM e quindi i provider determinano se l'utente deve avere accesso ai dati dello spazio dei nomi.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Sicurezza dello spazio dei nomi](#namespace-security)
-   [Distributed Component Object Model (DCOM) Security Impostazioni.](#distributed-component-object-model-dcom-security-settings)
-   [WMI, host del servizio condiviso e autenticazione](#wmi-shared-service-hosts-and-authentication)
-   [Sicurezza per applicazioni e script client WMI](#security-for-wmi-client-scripts-and-applications)
-   [Argomenti correlati](#related-topics)

## <a name="namespace-security"></a>Sicurezza dello spazio dei nomi

La sicurezza dello spazio dei nomi dipende Windows id di sicurezza [*utente (SID)*](gloss-s.md) e dal descrittore di sicurezza [*per*](gloss-s.md) lo spazio dei nomi WMI.

È possibile impostare la sicurezza dello spazio dei nomi eseguendo le azioni seguenti:

-   Concedere o negare diritti di accesso agli spazi dei nomi per gli utenti che usano il controllo WMI o quando viene creato lo spazio dei nomi. Per altre informazioni, vedere [Impostazione della sicurezza dello spazio dei](setting-namespace-security-with-the-wmi-control.md) nomi con il controllo WMI e Impostazione della sicurezza dello spazio dei nomi quando viene creato lo spazio dei [nomi](setting-namespace-security-when-the-namespace-is-created.md).
-   Usare il controllo WMI scheda Sicurezza per stabilire il controllo di sicurezza. Il controllo di sicurezza comporta voci del registro eventi quando un utente ha esito negativo o ha esito positivo in un'azione di controllo, ad esempio la scrittura di dati in un oggetto WMI o la lettura del descrittore di sicurezza. Per altre informazioni, vedere [Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md).
-   Usare il file MOF che definisce lo spazio dei nomi per richiedere a un utente di stabilire una connessione crittografata. Per altre informazioni, vedere [Richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="distributed-component-object-model-dcom-security-settings"></a>Distributed Component Object Model (DCOM) Security Impostazioni.

La sicurezza DCOM richiede un'impostazione di autenticazione e un'impostazione di rappresentazione. L'autenticazione significa che un processo si identifica con un altro. La rappresentazione identifica l'autorità che un client concede a un server per chiamare processi diversi. Durante un controllo di sicurezza, il server rappresenta il client. Per altre informazioni, vedere [Protezione di client e provider C++](securing-c---clients-and-providers.md) o Protezione dei client di [scripting](securing-scripting-clients.md).

Gli script e le applicazioni C/C++/C# stabiliscono livelli di autenticazione e rappresentazione quando si connettono a uno spazio dei nomi WMI o usano le impostazioni predefinite. Le connessioni ai computer remoti richiedono impostazioni diverse rispetto agli spazi dei nomi WMI nel computer locale. Per altre informazioni, vedere [Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

## <a name="wmi-shared-service-hosts-and-authentication"></a>WMI, host del servizio condiviso e autenticazione

WMI si trova in un host del servizio condiviso con diversi altri servizi in esecuzione con l'account NetworkService. In un processo Svchost WMI condivide la stessa autenticazione degli altri processi nell'host.

Le DLL del provider vengono caricate in processi host del servizio separati da WMI. La **proprietà HostingModel** nella [**\_ \_ classe di sistema Win32Provider**](--win32provider.md) che rappresenta un provider specifica l'account di sistema con cui viene eseguito il provider. L'impostazione di questa proprietà determina il caricamento del provider in un processo host condiviso con un livello di privilegi specificato. Per altre informazioni, vedere [Provider Hosting and Security](provider-hosting-and-security.md).

## <a name="security-for-wmi-client-scripts-and-applications"></a>Sicurezza per applicazioni e script client WMI

Gli script e le applicazioni devono stabilire la sicurezza corretta per connettersi agli spazi dei nomi WMI nei computer locali e remoti. Per altre informazioni, vedere [Protezione di client e provider C++,](securing-c---clients-and-providers.md)Protezione dei client di [scripting](securing-scripting-clients.md)e Protezione di [eventi WMI.](securing-wmi-events.md)

Nella tabella seguente sono elencati gli argomenti relativi alla gestione della sicurezza WMI.



| Argomento                                                                                              | Descrizione                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md)                                             | È possibile limitare l'accesso ai dati dello spazio dei nomi agli utenti autorizzati tramite il controllo WMI.                                                                                      |
| [Protezione del provider](securing-your-provider.md)                                               | Informazioni sulla scrittura di provider sicuri.                                                                                                                           |
| [Protezione di client e provider C++](securing-c---clients-and-providers.md)                       | Sia i provider C++ che le applicazioni client devono eseguire molte delle stesse operazioni per mantenere la sicurezza WMI.                                                         |
| [Protezione dei client di scripting](securing-scripting-clients.md)                                       | Gli script e Visual Basic applicazioni (client di automazione) devono impostare la sicurezza appropriata per ottenere l'accesso a dati ed eventi WMI.                                        |
| [Protezione degli eventi WMI](securing-wmi-events.md)                                                     | Gli eventi WMI vengono recapitati dal provider di eventi a un consumer temporaneo o permanente. Gli eventi vengono recapitati sotto forma di un'istanza di una classe di evento.               |
| [Modifica della sicurezza degli accessi per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md) | Con le autorizzazioni appropriate, è possibile chiamare metodi sugli oggetti WMI che rappresentano oggetti a protezione diretta che leggono o modificano i descrittori di sicurezza sugli oggetti a protezione diretta. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di WMI](using-wmi.md)
</dt> </dl>

 

 



