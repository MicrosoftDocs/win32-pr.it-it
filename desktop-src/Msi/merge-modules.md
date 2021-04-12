---
description: I moduli merge forniscono un metodo standard mediante il quale gli sviluppatori distribuiscono i componenti Windows Installer condivisi e la logica di configurazione alle applicazioni.
ms.assetid: 673de3ff-e58c-4153-9c8d-c3baebba5eb1
title: Unisci moduli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3499368b309909bcb06da45476d43d8cac28e205
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233848"
---
# <a name="merge-modules"></a><span data-ttu-id="c26b1-103">Unisci moduli</span><span class="sxs-lookup"><span data-stu-id="c26b1-103">Merge Modules</span></span>

<span data-ttu-id="c26b1-104">I moduli merge forniscono un metodo standard mediante il quale gli sviluppatori distribuiscono i [*componenti*](c-gly.md) Windows Installer condivisi e la logica di configurazione alle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c26b1-104">Merge modules provide a standard method by which developers deliver shared Windows Installer [*components*](c-gly.md) and setup logic to their applications.</span></span> <span data-ttu-id="c26b1-105">I moduli merge vengono utilizzati per fornire codice condiviso, file, risorse, voci del registro di sistema e la logica di installazione alle applicazioni come un unico file composto.</span><span class="sxs-lookup"><span data-stu-id="c26b1-105">Merge modules are used to deliver shared code, files, resources, registry entries, and setup logic to applications as a single compound file.</span></span> <span data-ttu-id="c26b1-106">Gli sviluppatori che creano nuovi modelli merge o utilizzano i moduli merge esistenti devono seguire lo standard descritto in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="c26b1-106">Developers authoring new merge modules or using existing merge modules should follow the standard outlined in this section.</span></span>

<span data-ttu-id="c26b1-107">Un modulo merge è simile alla struttura di un file Windows Installer [*. msi*](m-gly.md)semplificato.</span><span class="sxs-lookup"><span data-stu-id="c26b1-107">A merge module is similar in structure to a simplified Windows Installer [*.msi file*](m-gly.md).</span></span> <span data-ttu-id="c26b1-108">Un modulo merge, tuttavia, non può essere installato da solo, ma deve essere unito in un pacchetto di installazione utilizzando uno strumento di merge.</span><span class="sxs-lookup"><span data-stu-id="c26b1-108">However, a merge module cannot be installed alone, it must be merged into an installation package using a merge tool.</span></span> <span data-ttu-id="c26b1-109">Gli sviluppatori che desiderano utilizzare i moduli unione devono ottenere uno degli strumenti di merge distribuiti liberamente, ad esempio Mergemod.dll, oppure acquistare uno strumento di merge da un fornitore di software indipendente.</span><span class="sxs-lookup"><span data-stu-id="c26b1-109">Developers wanting to use merge modules must obtain one of the freely distributed merge tools, such as Mergemod.dll, or purchase a merge tool from an independent software vendor.</span></span> <span data-ttu-id="c26b1-110">Gli sviluppatori possono creare nuovi moduli unione usando molti degli stessi strumenti software usati per creare un pacchetto di installazione di Windows Installer, ad esempio l'editor di tabelle di database Orca fornito con Windows Installer SDK.</span><span class="sxs-lookup"><span data-stu-id="c26b1-110">Developers can create new merge modules by using many of the same software tools used to create a Windows Installer installation package, such as the database table editor Orca provided with the Windows Installer SDK.</span></span>

<span data-ttu-id="c26b1-111">Quando un modulo merge viene unito nel file con estensione msi di un'applicazione, tutte le informazioni e le risorse necessarie per installare i componenti forniti dal modulo merge vengono incorporate nel file con estensione msi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c26b1-111">When a merge module is merged into the .msi file of an application, all the information and resources required to install the components delivered by the merge module are incorporated into the application's .msi file.</span></span> <span data-ttu-id="c26b1-112">Il modulo merge non è più necessario per installare questi componenti e non è necessario che il modulo merge sia accessibile a un utente.</span><span class="sxs-lookup"><span data-stu-id="c26b1-112">The merge module is then no longer required to install these components and the merge module does not need to be accessible to a user.</span></span> <span data-ttu-id="c26b1-113">Poiché tutte le informazioni necessarie per installare i componenti vengono recapitate come un singolo file, l'utilizzo di modelli Unione può eliminare molte istanze di conflitti di versione, voci del registro di sistema mancanti e file installati in modo errato.</span><span class="sxs-lookup"><span data-stu-id="c26b1-113">Because all the information needed to install the components is delivered as a single file, the use of merge modules can eliminate many instances of version conflicts, missing registry entries, and improperly installed files.</span></span>

<span data-ttu-id="c26b1-114">Per ulteriori informazioni sui moduli merge, vedere:</span><span class="sxs-lookup"><span data-stu-id="c26b1-114">For more information about merge modules, see:</span></span>

-   [<span data-ttu-id="c26b1-115">Informazioni sui moduli merge</span><span class="sxs-lookup"><span data-stu-id="c26b1-115">About Merge Modules</span></span>](about-merge-modules.md)
-   [<span data-ttu-id="c26b1-116">Uso di moduli merge</span><span class="sxs-lookup"><span data-stu-id="c26b1-116">Using Merge Modules</span></span>](using-merge-modules.md)
-   [<span data-ttu-id="c26b1-117">Riferimento al modulo merge</span><span class="sxs-lookup"><span data-stu-id="c26b1-117">Merge Module Reference</span></span>](merge-module-reference.md)

 

 



