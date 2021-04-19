---
description: Debug di componenti scritti in Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Debug di componenti scritti in Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305223"
---
# <a name="debugging-components-written-in-visual-basic"></a><span data-ttu-id="2de54-103">Debug di componenti scritti in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2de54-103">Debugging Components Written in Visual Basic</span></span>

<span data-ttu-id="2de54-104">È possibile utilizzare l'ambiente di sviluppo Microsoft Visual Basic 6,0 per il debug in determinati scenari.</span><span class="sxs-lookup"><span data-stu-id="2de54-104">You can use the Microsoft Visual Basic 6.0 development environment for debugging within certain scenarios.</span></span> <span data-ttu-id="2de54-105">L'uso di Visual Basic per il debug consente l'accesso a strumenti familiari con Visual Basic programmatori.</span><span class="sxs-lookup"><span data-stu-id="2de54-105">Using Visual Basic for debugging allows access to tools familiar to Visual Basic programmers.</span></span> <span data-ttu-id="2de54-106">D'altra parte, poiché durante il debug Visual Basic componenti vengono eseguiti nel processo dell'ambiente Visual Basic, potrebbe essere necessario eseguire il debug del componente dopo che è stato compilato tramite l'ambiente di sviluppo di Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="2de54-106">On the other hand, because during debugging Visual Basic components run within the Visual Basic environment's process, it may be necessary to debug your component after it has been compiled by using the Microsoft Visual C++ development environment.</span></span>

<span data-ttu-id="2de54-107">Per ulteriori informazioni sul debug all'interno del Visual Basic Integrated Development Environment (IDE), vedere [debug nell'IDE di Visual Basic](debugging-in-the-visual-basic-ide.md).</span><span class="sxs-lookup"><span data-stu-id="2de54-107">For more information about debugging within the Visual Basic integrated development environment (IDE), see [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md).</span></span> <span data-ttu-id="2de54-108">Per altre informazioni sul debug dei componenti di Visual Basic dopo che sono stati compilati usando l'ambiente di sviluppo Visual C++, vedere [debug di componenti Visual Basic compilati](debugging-compiled-visual-basic-components.md).</span><span class="sxs-lookup"><span data-stu-id="2de54-108">For more on debugging Visual Basic components after they're compiled using the Visual C++ development environment, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

<span data-ttu-id="2de54-109">Inoltre, per COM+ sono state risolte diverse limitazioni associate all'utilizzo dell'ambiente Visual Basic per eseguire il debug dei componenti con MTS.</span><span class="sxs-lookup"><span data-stu-id="2de54-109">Also, several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="2de54-110">Per ulteriori informazioni, vedere [COM+ Visual Basic il supporto per il debug in contrapposizione a MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span><span class="sxs-lookup"><span data-stu-id="2de54-110">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

> [!Note]  
> <span data-ttu-id="2de54-111">Se si è già utilizzato Visual Basic nello stesso computer di COM+, è possibile che sia stato notato il componente aggiuntivo Servizi componenti disponibile nell'ambiente Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2de54-111">If you have already used Visual Basic on the same computer as COM+, you may have noticed the Component Services add-in available in the Visual Basic environment.</span></span> <span data-ttu-id="2de54-112">Originariamente in MTS, questa funzionalità è stata progettata per aggiornare il registro di sistema ogni volta che si ricompila un componente in un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="2de54-112">Originally in MTS, this feature was designed to update the registry each time you recompiled a component in a COM+ application.</span></span> <span data-ttu-id="2de54-113">Tuttavia, data la natura dell'interazione tra il registro di sistema di Microsoft Windows e il database di registrazione COM+, alcune impostazioni potrebbero non essere completamente aggiornate.</span><span class="sxs-lookup"><span data-stu-id="2de54-113">However, given the nature of the interaction of the Microsoft Windows Registry and the COM+ registration database, some settings may not be completely updated.</span></span> <span data-ttu-id="2de54-114">Pertanto, anziché usare i comandi disponibili con questo componente aggiuntivo, è necessario rimuovere e reinstallare i componenti per aggiornare le impostazioni dopo la ricompilazione.</span><span class="sxs-lookup"><span data-stu-id="2de54-114">Therefore, instead of using the commands available with this add-in, you should remove and reinstall your components to update settings after recompiling.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2de54-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2de54-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2de54-116">Debug di componenti scritti in Visual C++</span><span class="sxs-lookup"><span data-stu-id="2de54-116">Debugging Components Written in Visual C++</span></span>](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



