---
title: Registrazione di applicazioni COM
description: Registrazione di applicazioni COM
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331807"
---
# <a name="registering-com-applications"></a><span data-ttu-id="4b7bd-103">Registrazione di applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="4b7bd-103">Registering COM Applications</span></span>

<span data-ttu-id="4b7bd-104">Il registro di sistema è un database di sistema che contiene informazioni sulla configurazione dell'hardware e del software del sistema, nonché sugli utenti del sistema.</span><span class="sxs-lookup"><span data-stu-id="4b7bd-104">The registry is a system database that contains information about the configuration of system hardware and software as well as about users of the system.</span></span> <span data-ttu-id="4b7bd-105">Qualsiasi programma basato su Windows può aggiungere informazioni al registro di sistema e leggere le informazioni dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4b7bd-105">Any Windows-based program can add information to the registry and read information back from the registry.</span></span> <span data-ttu-id="4b7bd-106">I client cercano i componenti interessanti da usare nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4b7bd-106">Clients search the registry for interesting components to use.</span></span>

<span data-ttu-id="4b7bd-107">Il registro di sistema mantiene le informazioni su tutti gli oggetti COM installati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4b7bd-107">The registry maintains information about all the COM objects installed in the system.</span></span> <span data-ttu-id="4b7bd-108">Ogni volta che un'applicazione crea un'istanza di un componente COM, viene consultato il registro di sistema per risolvere il CLSID o il ProgID del componente nel percorso della DLL del server o del file EXE che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="4b7bd-108">Whenever an application creates an instance of a COM component, the registry is consulted to resolve either the CLSID or ProgID of the component into the pathname of the server DLL or EXE that contains it.</span></span> <span data-ttu-id="4b7bd-109">Dopo aver determinato il server del componente, Windows carica il server nello spazio di processo dell'applicazione client (componenti in-process) o avvia il server nello spazio di processo (server locali e remoti).</span><span class="sxs-lookup"><span data-stu-id="4b7bd-109">After determining the component's server, Windows either loads the server into the process space of the client application (in-process components) or starts the server in its own process space (local and remote servers).</span></span> <span data-ttu-id="4b7bd-110">Il server crea un'istanza del componente e restituisce al client un riferimento a una delle interfacce del componente.</span><span class="sxs-lookup"><span data-stu-id="4b7bd-110">The server creates an instance of the component and returns to the client a reference to one of the component's interfaces.</span></span>

<span data-ttu-id="4b7bd-111">Per ulteriori informazioni sul Registro di sistema di Windows, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b7bd-111">For more information about the Windows registry, see the following topics:</span></span>

-   [<span data-ttu-id="4b7bd-112">Gerarchia del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="4b7bd-112">Registry Hierarchy</span></span>](registry-hierarchy.md)
-   [<span data-ttu-id="4b7bd-113">Classi e server</span><span class="sxs-lookup"><span data-stu-id="4b7bd-113">Classes and Servers</span></span>](classes-and-servers.md)
-   [<span data-ttu-id="4b7bd-114">Classificazione di componenti</span><span class="sxs-lookup"><span data-stu-id="4b7bd-114">Classifying Components</span></span>](classifying-components.md)
-   [<span data-ttu-id="4b7bd-115">Uso di OleView</span><span class="sxs-lookup"><span data-stu-id="4b7bd-115">Using OleView</span></span>](using-oleview.md)
-   [<span data-ttu-id="4b7bd-116">Registrazione di componenti</span><span class="sxs-lookup"><span data-stu-id="4b7bd-116">Registering Components</span></span>](registering-components.md)
-   [<span data-ttu-id="4b7bd-117">Verifica della registrazione</span><span class="sxs-lookup"><span data-stu-id="4b7bd-117">Checking Registration</span></span>](checking-registration.md)
-   [<span data-ttu-id="4b7bd-118">Tipi di utente sconosciuti</span><span class="sxs-lookup"><span data-stu-id="4b7bd-118">Unknown User Types</span></span>](unknown-user-types.md)
-   [<span data-ttu-id="4b7bd-119">Chiavi del registro di sistema COM</span><span class="sxs-lookup"><span data-stu-id="4b7bd-119">COM Registry Keys</span></span>](com-registry-keys.md)

 

 




