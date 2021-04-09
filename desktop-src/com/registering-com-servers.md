---
title: Registrazione di server COM
description: Registrazione di server COM
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118487"
---
# <a name="registering-com-servers"></a><span data-ttu-id="81f5a-103">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="81f5a-103">Registering COM Servers</span></span>

<span data-ttu-id="81f5a-104">Dopo aver definito una classe nel codice (garantendo che implementi [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) o [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) e avergli assegnato un CLSID, è necessario inserire nel registro di sistema le informazioni che consentiranno a com, su richiesta di un client con il CLSID, di creare istanze dei relativi oggetti.</span><span class="sxs-lookup"><span data-stu-id="81f5a-104">After you have defined a class in code (ensuring that it implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) and assigned it a CLSID, you need to put information in the registry that will allow COM, on request of a client with the CLSID, to create instances of its objects.</span></span> <span data-ttu-id="81f5a-105">Queste informazioni indicano al sistema, per un determinato CLSID, dove si trova il codice DLL o EXE per la classe e come deve essere avviato.</span><span class="sxs-lookup"><span data-stu-id="81f5a-105">This information tells the system, for a given CLSID, where the DLL or EXE code for that class is located and how it is to be launched.</span></span>

<span data-ttu-id="81f5a-106">Esiste più di un modo per registrare una classe nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="81f5a-106">There is more than one way of registering a class in the registry.</span></span> <span data-ttu-id="81f5a-107">Inoltre, esistono altri modi per "registrare" una classe con il sistema durante l'esecuzione, in modo che il sistema sia in grado di riconoscere che un oggetto in esecuzione è attualmente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="81f5a-107">In addition, there are other ways of "registering" a class with the system when it is running, so that the system is aware that a running object is currently in the system.</span></span>

<span data-ttu-id="81f5a-108">Per ulteriori informazioni sulla registrazione, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="81f5a-108">See the following topics for more information about registering:</span></span>

-   [<span data-ttu-id="81f5a-109">Registrazione di una classe durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="81f5a-109">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
-   [<span data-ttu-id="81f5a-110">Registrazione di un server EXE in esecuzione</span><span class="sxs-lookup"><span data-stu-id="81f5a-110">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
-   [<span data-ttu-id="81f5a-111">Registrazione di oggetti nella tabella ROT</span><span class="sxs-lookup"><span data-stu-id="81f5a-111">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
-   [<span data-ttu-id="81f5a-112">Registrazione automatica</span><span class="sxs-lookup"><span data-stu-id="81f5a-112">Self-Registration</span></span>](self-registration.md)
-   [<span data-ttu-id="81f5a-113">Installazione come applicazione di servizio</span><span class="sxs-lookup"><span data-stu-id="81f5a-113">Installing as a Service Application</span></span>](installing-as-a-service-application.md)

## <a name="related-topics"></a><span data-ttu-id="81f5a-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81f5a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81f5a-115">Responsabilità server COM</span><span class="sxs-lookup"><span data-stu-id="81f5a-115">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 