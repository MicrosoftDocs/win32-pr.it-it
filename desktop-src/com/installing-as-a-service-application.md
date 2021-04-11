---
title: Installazione come applicazione di servizio
description: Installazione come applicazione di servizio
ms.assetid: 0dd4b348-3d12-49ba-8098-4adb9df01a0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed5c474d73c74b3be40bae773c3d51eadf6c69a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047408"
---
# <a name="installing-as-a-service-application"></a>Installazione come applicazione di servizio

Oltre a essere eseguito come file eseguibile del server locale (EXE), un oggetto COM può anche creare un pacchetto per l'esecuzione come applicazione di servizio quando viene attivato da un client locale o remoto. I servizi supportano numerose funzionalità amministrative integrate e interfaceâ di utenti, tra cui l'avvio, l'arresto, la sospensione e il riavvio locali e remoti, nonché la possibilità di stabilire il server per l'esecuzione con un [account utente](/windows/desktop/Services/service-user-accounts) specifico e una [stazione di finestra](/windows/desktop/winstation/window-stations).

Un oggetto scritto come servizio viene installato per l'uso da COM mediante la definizione di un valore [LocalService](localservice.md) nella relativa chiave [AppID](appid-key.md) e l'esecuzione di un'installazione del servizio standard.

Le classi possono anche essere configurate per l'esecuzione con un account utente specifico quando vengono attivate da un client remoto senza essere scritte come applicazione di servizio. A tale scopo, la classe installa un nome utente e una password da usare quando SCM avvia il processo del server locale.

Quando una classe è configurata in questo modo, le chiamate a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con questo CLSID avranno esito negativo a meno che il processo non sia stato avviato da com per conto di una richiesta di attivazione effettiva. In altre parole, le classi configurate per l'esecuzione come un utente specifico potrebbero non essere registrate con altre identità.

Il nome utente viene tratto da [RunAs](runas.md) denominato-value sotto la chiave AppID della classe. Se il nome utente è "utente interattivo", il codice della classe viene eseguito nel contesto di sicurezza dell'utente attualmente connesso ed è connesso alla stazione di finestra interattiva.

In caso contrario, la password viene recuperata da una parte nascosta del registro di sistema disponibile solo per gli amministratori del computer e del sistema. Il nome utente e la password vengono quindi utilizzati per creare una sessione di accesso in cui viene eseguito il codice della classe. Quando viene avviato in questo modo, il codice della classe viene eseguito con il proprio desktop e la stazione di Windows e non condivide gli handle di finestra, gli Appunti o altri elementi dell'interfaccia utente con l'utente interattivo o altre classi in esecuzione in altri account utente.

Un server registrato tramite **LocalService** o **RunAs** può registrare un oggetto nella tabella degli oggetti in esecuzione per consentire a qualsiasi client di connettersi a tale oggetto. A tale scopo, la chiamata del server a [**IRunningObjectTable:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) deve impostare il \_ flag ROTFLAGS ALLOWANYCLIENT. Un'impostazione del server questo bit deve avere il nome dell'eseguibile nella sezione AppID del registro di sistema che fa riferimento all'AppID per il file eseguibile. Un server "Activate As Activator" (non registrato come **LocalService** o **RunAs**) non può registrare un oggetto con questo flag.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di una classe durante l'installazione](registering-a-class-at-installation.md)
</dt> <dt>

[Registrazione di un server EXE in esecuzione](registering-a-running-exe-server.md)
</dt> <dt>

[Registrazione di oggetti nella tabella ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Registrazione automatica](self-registration.md)
</dt> </dl>

 

 