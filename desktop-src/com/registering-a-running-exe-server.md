---
title: Registrazione di un server EXE in esecuzione
description: Registrazione di un server EXE in esecuzione
ms.assetid: 277f44bb-72b7-4409-955d-2cd53bc99467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0c6cae15818e5cdb3931f71f0d4be1ac1baef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331583"
---
# <a name="registering-a-running-exe-server"></a><span data-ttu-id="94340-103">Registrazione di un server EXE in esecuzione</span><span class="sxs-lookup"><span data-stu-id="94340-103">Registering a Running EXE Server</span></span>

<span data-ttu-id="94340-104">Quando viene avviato un server eseguibile (EXE), deve chiamare [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), che registra il CLSID per il server in ciò che viene chiamato tabella della classe (una tabella diversa rispetto alla tabella degli oggetti in esecuzione).</span><span class="sxs-lookup"><span data-stu-id="94340-104">When an executable (EXE) server is launched, it should call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject), which registers the CLSID for the server in what is called the class table (a different table than the running object table).</span></span> <span data-ttu-id="94340-105">Quando un server viene registrato nella tabella della classe, consente a gestione controllo servizi di determinare che non è necessario avviare di nuovo la classe, perché il server è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="94340-105">When a server is registered in the class table, it allows the service control manager (SCM) to determine that it is not necessary to launch the class again, because the server is already running.</span></span> <span data-ttu-id="94340-106">Solo se il server non è elencato nella tabella della classe, SCM verificherà i valori appropriati nel registro di sistema e avvierà il server associato al CLSID specificato.</span><span class="sxs-lookup"><span data-stu-id="94340-106">Only if the server is not listed in the class table will the SCM check the registry for appropriate values and launch the server associated with the given CLSID.</span></span>

<span data-ttu-id="94340-107">Si passa [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) al CLSID per la classe e un puntatore alla relativa interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="94340-107">You pass [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) the CLSID for the class and a pointer to its [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="94340-108">I client che successivamente chiamano [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) con questo CLSID recupereranno un puntatore all'interfaccia richiesta, purché la sicurezza non lo vieti.</span><span class="sxs-lookup"><span data-stu-id="94340-108">Clients who subsequently call [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with this CLSID will retrieve a pointer to their requested interface, as long as security does not forbid it.</span></span> <span data-ttu-id="94340-109">Vedere [funzioni helper](instance-creation-helper-functions.md) per la creazione di istanze per una descrizione di diverse funzioni di creazione e attivazione di istanze.</span><span class="sxs-lookup"><span data-stu-id="94340-109">(See [Instance Creation Helper Functions](instance-creation-helper-functions.md) for a description of several instance creation and activation functions.)</span></span>

<span data-ttu-id="94340-110">Il server per un oggetto classe deve chiamare [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) per revocare l'oggetto classe (rimuovere la registrazione) quando si verificano tutte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="94340-110">The server for a class object should call [**CoRevokeClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject) to revoke the class object (remove its registration) when all of the following are true:</span></span>

-   <span data-ttu-id="94340-111">Nessuna istanza esistente della definizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="94340-111">There are no existing instances of the object definition.</span></span>
-   <span data-ttu-id="94340-112">Non ci sono blocchi sull'oggetto classe.</span><span class="sxs-lookup"><span data-stu-id="94340-112">There are no locks on the class object.</span></span>
-   <span data-ttu-id="94340-113">L'applicazione che fornisce servizi all'oggetto classe non è sotto il controllo utente (non visibile all'utente sullo schermo).</span><span class="sxs-lookup"><span data-stu-id="94340-113">The application providing services to the class object is not under user control (not visible to the user on the display).</span></span>

## <a name="related-topics"></a><span data-ttu-id="94340-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="94340-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94340-115">Installazione come applicazione di servizio</span><span class="sxs-lookup"><span data-stu-id="94340-115">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="94340-116">Registrazione di una classe durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="94340-116">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="94340-117">Registrazione di oggetti nella tabella ROT</span><span class="sxs-lookup"><span data-stu-id="94340-117">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="94340-118">Registrazione automatica</span><span class="sxs-lookup"><span data-stu-id="94340-118">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 




