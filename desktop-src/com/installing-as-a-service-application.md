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
# <a name="installing-as-a-service-application"></a><span data-ttu-id="b16c9-103">Installazione come applicazione di servizio</span><span class="sxs-lookup"><span data-stu-id="b16c9-103">Installing as a Service Application</span></span>

<span data-ttu-id="b16c9-104">Oltre a essere eseguito come file eseguibile del server locale (EXE), un oggetto COM può anche creare un pacchetto per l'esecuzione come applicazione di servizio quando viene attivato da un client locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="b16c9-104">In addition to running as a local server executable (EXE), a COM object may also package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="b16c9-105">I servizi supportano numerose funzionalità amministrative integrate e interfaceâ di utenti, tra cui l'avvio, l'arresto, la sospensione e il riavvio locali e remoti, nonché la possibilità di stabilire il server per l'esecuzione con un [account utente](/windows/desktop/Services/service-user-accounts) specifico e una [stazione di finestra](/windows/desktop/winstation/window-stations).</span><span class="sxs-lookup"><span data-stu-id="b16c9-105">Services support numerous useful and user interfaceâ€“integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific [user account](/windows/desktop/Services/service-user-accounts) and [window station](/windows/desktop/winstation/window-stations).</span></span>

<span data-ttu-id="b16c9-106">Un oggetto scritto come servizio viene installato per l'uso da COM mediante la definizione di un valore [LocalService](localservice.md) nella relativa chiave [AppID](appid-key.md) e l'esecuzione di un'installazione del servizio standard.</span><span class="sxs-lookup"><span data-stu-id="b16c9-106">An object written as a service is installed for use by COM by establishing a [LocalService](localservice.md) value under its [AppID](appid-key.md) key and performing a standard service installation.</span></span>

<span data-ttu-id="b16c9-107">Le classi possono anche essere configurate per l'esecuzione con un account utente specifico quando vengono attivate da un client remoto senza essere scritte come applicazione di servizio.</span><span class="sxs-lookup"><span data-stu-id="b16c9-107">Classes may also be configured to run under a specific user account when activated by a remote client without being written as a service application.</span></span> <span data-ttu-id="b16c9-108">A tale scopo, la classe installa un nome utente e una password da usare quando SCM avvia il processo del server locale.</span><span class="sxs-lookup"><span data-stu-id="b16c9-108">To do this, the class installs a user name and a password to be used when the SCM launches its local server process.</span></span>

<span data-ttu-id="b16c9-109">Quando una classe è configurata in questo modo, le chiamate a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con questo CLSID avranno esito negativo a meno che il processo non sia stato avviato da com per conto di una richiesta di attivazione effettiva.</span><span class="sxs-lookup"><span data-stu-id="b16c9-109">When a class is configured in this fashion, calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID will fail unless the process was launched by COM on behalf of an actual activation request.</span></span> <span data-ttu-id="b16c9-110">In altre parole, le classi configurate per l'esecuzione come un utente specifico potrebbero non essere registrate con altre identità.</span><span class="sxs-lookup"><span data-stu-id="b16c9-110">In other words, classes configured to run as a particular user may not be registered under any other identity.</span></span>

<span data-ttu-id="b16c9-111">Il nome utente viene tratto da [RunAs](runas.md) denominato-value sotto la chiave AppID della classe.</span><span class="sxs-lookup"><span data-stu-id="b16c9-111">The user name is taken from the [RunAs](runas.md) named-value under the class's APPID key.</span></span> <span data-ttu-id="b16c9-112">Se il nome utente è "utente interattivo", il codice della classe viene eseguito nel contesto di sicurezza dell'utente attualmente connesso ed è connesso alla stazione di finestra interattiva.</span><span class="sxs-lookup"><span data-stu-id="b16c9-112">If the user name is "Interactive User", the class code is run in the security context of the currently logged on user and is connected to the interactive window station.</span></span>

<span data-ttu-id="b16c9-113">In caso contrario, la password viene recuperata da una parte nascosta del registro di sistema disponibile solo per gli amministratori del computer e del sistema.</span><span class="sxs-lookup"><span data-stu-id="b16c9-113">Otherwise, the password is retrieved from a hidden portion of the registry available only to administrators of the machine and to the system.</span></span> <span data-ttu-id="b16c9-114">Il nome utente e la password vengono quindi utilizzati per creare una sessione di accesso in cui viene eseguito il codice della classe.</span><span class="sxs-lookup"><span data-stu-id="b16c9-114">The user name and password are then used to create a logon session in which the class code is run.</span></span> <span data-ttu-id="b16c9-115">Quando viene avviato in questo modo, il codice della classe viene eseguito con il proprio desktop e la stazione di Windows e non condivide gli handle di finestra, gli Appunti o altri elementi dell'interfaccia utente con l'utente interattivo o altre classi in esecuzione in altri account utente.</span><span class="sxs-lookup"><span data-stu-id="b16c9-115">When launched in this way, the class code runs with its own desktop and window-station and does not share window handles, the clipboard, or other user interface elements with the interactive user or other classes running in other user accounts.</span></span>

<span data-ttu-id="b16c9-116">Un server registrato tramite **LocalService** o **RunAs** può registrare un oggetto nella tabella degli oggetti in esecuzione per consentire a qualsiasi client di connettersi a tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="b16c9-116">A server registered either with **LocalService** or **RunAs** can register an object in the running object table to allow any client to connect to it.</span></span> <span data-ttu-id="b16c9-117">A tale scopo, la chiamata del server a [**IRunningObjectTable:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) deve impostare il \_ flag ROTFLAGS ALLOWANYCLIENT.</span><span class="sxs-lookup"><span data-stu-id="b16c9-117">To do so, the server's call to [**IRunningObjectTable::Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) must set the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="b16c9-118">Un'impostazione del server questo bit deve avere il nome dell'eseguibile nella sezione AppID del registro di sistema che fa riferimento all'AppID per il file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="b16c9-118">A server setting this bit must have its executable name in the AppID section of the registry that refers to the AppID for the executable.</span></span> <span data-ttu-id="b16c9-119">Un server "Activate As Activator" (non registrato come **LocalService** o **RunAs**) non può registrare un oggetto con questo flag.</span><span class="sxs-lookup"><span data-stu-id="b16c9-119">An "activate as activator" server (not registered as either **LocalService** or **RunAs**) may not register an object with this flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b16c9-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b16c9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b16c9-121">Registrazione di una classe durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="b16c9-121">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="b16c9-122">Registrazione di un server EXE in esecuzione</span><span class="sxs-lookup"><span data-stu-id="b16c9-122">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="b16c9-123">Registrazione di oggetti nella tabella ROT</span><span class="sxs-lookup"><span data-stu-id="b16c9-123">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="b16c9-124">Registrazione automatica</span><span class="sxs-lookup"><span data-stu-id="b16c9-124">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 