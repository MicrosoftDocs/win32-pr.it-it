---
description: La protezione WMI è incentrata sulla protezione dell'accesso ai dati dello spazio dei nomi. WMI innanzitutto concede l'accesso ai gruppi di utenti come specificato dal controllo WMI e dalle impostazioni DCOM, quindi i provider determinano se l'utente deve avere accesso ai dati dello spazio dei nomi.
ms.assetid: 88a2538a-ae30-4a1a-9d16-f0cd9419b2ed
ms.tgt_platform: multiple
title: Gestione della sicurezza WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25cbf4a29567b263d6bd279aac9e2e6e21c523e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315198"
---
# <a name="maintaining-wmi-security"></a>Gestione della sicurezza WMI

La protezione WMI è incentrata sulla protezione dell'accesso ai dati dello spazio dei nomi. WMI innanzitutto concede l'accesso ai gruppi di utenti come specificato dal [*controllo WMI*](gloss-w.md) e dalle impostazioni DCOM, quindi i provider determinano se l'utente deve avere accesso ai dati dello spazio dei nomi.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Sicurezza dello spazio dei nomi](#namespace-security)
-   [Impostazioni di sicurezza DCOM (Distributed Component Object Model).](#distributed-component-object-model-dcom-security-settings)
-   [WMI, host di servizi condivisi e autenticazione](#wmi-shared-service-hosts-and-authentication)
-   [Sicurezza per le applicazioni e gli script client WMI](#security-for-wmi-client-scripts-and-applications)
-   [Argomenti correlati](#related-topics)

## <a name="namespace-security"></a>Sicurezza dello spazio dei nomi

La sicurezza dello spazio dei nomi dipende dagli [*identificatori di sicurezza utente (SID)*](gloss-s.md) di Windows standard e dal [*descrittore di sicurezza*](gloss-s.md) per lo spazio dei nomi WMI.

È possibile impostare la sicurezza dello spazio dei nomi eseguendo le azioni seguenti:

-   Concedere o negare i diritti di accesso agli spazi dei nomi per gli utenti che utilizzano il controllo WMI o quando viene creato lo spazio dei nomi. Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md) e [impostazione della sicurezza dello spazio dei nomi quando viene creato lo spazio dei](setting-namespace-security-when-the-namespace-is-created.md)nomi.
-   Utilizzare la scheda sicurezza del controllo WMI per stabilire il controllo della sicurezza. Il controllo di sicurezza genera voci del registro eventi quando un utente ha esito negativo o ha esito positivo in un'azione controllata, ad esempio la scrittura di dati in un oggetto WMI o la lettura del descrittore di sicurezza. Per ulteriori informazioni, vedere [accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md).
-   Utilizzare il file MOF che definisce lo spazio dei nomi per richiedere a un utente di effettuare una connessione crittografata. Per ulteriori informazioni, vedere la pagina relativa [alla richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="distributed-component-object-model-dcom-security-settings"></a>Impostazioni di sicurezza DCOM (Distributed Component Object Model).

Per la sicurezza DCOM è necessaria un'impostazione di autenticazione e un'impostazione di rappresentazione. L'autenticazione indica che un processo viene identificato a un altro. La rappresentazione identifica l'autorità a cui un client concede un server per chiamare processi diversi. Durante un controllo di sicurezza, il server rappresenta il client. Per ulteriori informazioni, vedere [protezione di client e provider C++](securing-c---clients-and-providers.md) o [protezione dei client di scripting](securing-scripting-clients.md).

Gli script e le applicazioni C/C++/C # stabiliscono i livelli di autenticazione e di rappresentazione quando si connettono a uno spazio dei nomi WMI o usano le impostazioni predefinite. Le connessioni ai computer remoti richiedono impostazioni diverse rispetto agli spazi dei nomi WMI nel computer locale. Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

## <a name="wmi-shared-service-hosts-and-authentication"></a>WMI, host di servizi condivisi e autenticazione

WMI risiede in un host del servizio condiviso con diversi altri servizi in esecuzione con l'account NetworkService. In un processo Svchost, WMI condivide la stessa autenticazione degli altri processi nell'host.

Le dll del provider vengono caricate in processi host del servizio distinti da WMI. La proprietà **HostingModel** nella classe di sistema [**\_ \_ Win32Provider**](--win32provider.md) che rappresenta un provider specifica l'account di sistema utilizzato per l'esecuzione del provider. L'impostazione di questa proprietà determina il caricamento del provider in un processo host condiviso con un livello di privilegio specificato. Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).

## <a name="security-for-wmi-client-scripts-and-applications"></a>Sicurezza per le applicazioni e gli script client WMI

Gli script e le applicazioni devono stabilire la corretta sicurezza per connettersi agli spazi dei nomi WMI nei computer locali e remoti. Per ulteriori informazioni, vedere [protezione di client e provider C++](securing-c---clients-and-providers.md), [protezione dei client di scripting](securing-scripting-clients.md)e [protezione degli eventi WMI](securing-wmi-events.md).

Nella tabella seguente sono elencati gli argomenti relativi alla gestione della sicurezza WMI.



| Argomento                                                                                              | Descrizione                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sicurezza degli spazi dei nomi WMI](securing-wmi-namespaces.md)                                             | È possibile limitare l'accesso ai dati dello spazio dei nomi agli utenti autorizzati tramite il controllo WMI.                                                                                      |
| [Sicurezza del provider](securing-your-provider.md)                                               | Informazioni sulla scrittura di provider protetti.                                                                                                                           |
| [Protezione di client e provider C++](securing-c---clients-and-providers.md)                       | Sia i provider C++ che le applicazioni client devono eseguire molte delle stesse operazioni per gestire la sicurezza di WMI.                                                         |
| [Protezione dei client di scripting](securing-scripting-clients.md)                                       | Per gli script e le applicazioni Visual Basic (client di automazione) è necessario impostare la sicurezza appropriata per ottenere l'accesso ai dati e agli eventi WMI.                                        |
| [Protezione degli eventi WMI](securing-wmi-events.md)                                                     | Gli eventi WMI vengono recapitati dal provider di eventi a un consumer temporaneo o permanente. Gli eventi vengono recapitati sotto forma di istanza di una classe di evento.               |
| [Modifica della sicurezza di accesso per gli oggetti a protezione diretta](changing-access-security-on-securable-objects.md) | Con le autorizzazioni appropriate, è possibile chiamare metodi sugli oggetti WMI che rappresentano gli oggetti a protezione diretta che leggono o modificano i descrittori di sicurezza per gli oggetti a protezione diretta. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di WMI](using-wmi.md)
</dt> </dl>

 

 



