---
title: Installazione come applicazione di servizio
description: Installazione come applicazione di servizio
ms.assetid: 0dd4b348-3d12-49ba-8098-4adb9df01a0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54b36b0bb6c853de98e8277e8b64171c6825bf1d9a51f557cbb7308fea546ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919044"
---
# <a name="installing-as-a-service-application"></a>Installazione come applicazione di servizio

Oltre all'esecuzione come eseguibile del server locale (EXE), un oggetto COM può anche creare un pacchetto per l'esecuzione come applicazione di servizio quando viene attivato da un client locale o remoto. I servizi supportano numerose funzionalità amministrative integrate e utili, tra cui avvio locale e remoto, arresto, sospensione e riavvio, nonché la possibilità di stabilire il server per l'esecuzione con un [account](/windows/desktop/Services/service-user-accounts) utente e una stazione finestra [specifici.](/windows/desktop/winstation/window-stations)

Un oggetto scritto come servizio viene installato per l'uso da parte di COM stabilendo un valore [LocalService](localservice.md) nella relativa chiave [AppID](appid-key.md) ed eseguendo un'installazione standard del servizio.

Le classi possono anche essere configurate per l'esecuzione con un account utente specifico quando vengono attivate da un client remoto senza essere scritte come applicazione di servizio. A tale scopo, la classe installa un nome utente e una password da usare quando Gestione controllo servizi avvia il processo del server locale.

Quando una classe viene configurata in questo modo, le chiamate a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con questo CLSID avranno esito negativo a meno che il processo non sia stato avviato da COM per conto di una richiesta di attivazione effettiva. In altre parole, le classi configurate per l'esecuzione come utente specifico potrebbero non essere registrate con altre identità.

Il nome utente deriva dal valore denominato [RunAs](runas.md) nella chiave APPID della classe. Se il nome utente è "Interactive User", il codice della classe viene eseguito nel contesto di sicurezza dell'utente attualmente connesso ed è connesso alla stazione finestra interattiva.

In caso contrario, la password viene recuperata da una parte nascosta del Registro di sistema disponibile solo per gli amministratori del computer e per il sistema. Il nome utente e la password vengono quindi utilizzati per creare una sessione di accesso in cui viene eseguito il codice della classe. Quando viene avviato in questo modo, il codice della classe viene eseguito con il proprio desktop e window-station e non condivide gli handle di finestra, gli Appunti o altri elementi dell'interfaccia utente con l'utente interattivo o altre classi in esecuzione in altri account utente.

Un server registrato con **LocalService** o **RunAs** può registrare un oggetto nella tabella degli oggetti in esecuzione per consentire a qualsiasi client di connettersi a esso. A tale scopo, la chiamata del server a [**IRunningObjectTable::Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) deve impostare il flag ROTFLAGS \_ ALLOWANYCLIENT. Un'impostazione del server per questo bit deve avere il nome eseguibile nella sezione AppID del Registro di sistema che fa riferimento all'AppID per l'eseguibile. Un server "activate as activator" (non registrato come **LocalService** o **RunAs)** potrebbe non registrare un oggetto con questo flag.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di una classe durante l'installazione](registering-a-class-at-installation.md)
</dt> <dt>

[Registrazione di un server EXE in esecuzione](registering-a-running-exe-server.md)
</dt> <dt>

[Registrazione di oggetti nella ROT](registering-objects-in-the-rot.md)
</dt> <dt>

[Registrazione automatica](self-registration.md)
</dt> </dl>

 

 