---
description: Le tecniche di debug per le applicazioni COM+ dipendono dal linguaggio in cui si sceglie di scrivere il componente.
ms.assetid: 781a0b3f-2bd0-435b-b6fe-4469cc02e8b6
title: Debug di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db096ceb525cd988afa55e49cc88fda0ddf52549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748866"
---
# <a name="debugging-com-applications"></a><span data-ttu-id="1dc9c-103">Debug di applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="1dc9c-103">Debugging COM+ Applications</span></span>

<span data-ttu-id="1dc9c-104">Le tecniche di debug per le applicazioni COM+ dipendono dal linguaggio in cui si sceglie di scrivere il componente.</span><span class="sxs-lookup"><span data-stu-id="1dc9c-104">Debugging techniques for COM+ applications depend on the language in which you choose to write your component.</span></span>

<span data-ttu-id="1dc9c-105">Se si esegue il codice in Microsoft Visual C++, è possibile avviare il debugger in C++ o, con un client remoto, è possibile eseguire il debug utilizzando il controllo remoto OLE procedure (RPC) e il debug JIT (just-in-Time).</span><span class="sxs-lookup"><span data-stu-id="1dc9c-105">If you code in Microsoft Visual C++, you can launch the debugger in C++ or, with a remote client, you can debug by using OLE remote procedure control (RPC) and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="1dc9c-106">È sempre possibile usare lo strumento di amministrazione Servizi componenti per eseguire il debug del componente con l'impostazione **avvio com+ in debugger** nella scheda **Avanzate** della finestra di dialogo **proprietà** dell'applicazione com+.</span><span class="sxs-lookup"><span data-stu-id="1dc9c-106">You can always use the Component Services administrative tool to debug your component with the COM+ **Launch in debugger** setting on the **Advanced** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="1dc9c-107">Per ulteriori informazioni sul debug di componenti codificati in C++, vedere [debug di componenti scritti in Visual C++](debugging-components-written-in-visual-c--.md).</span><span class="sxs-lookup"><span data-stu-id="1dc9c-107">For more information on debugging components coded in C++, see [Debugging Components Written in Visual C++](debugging-components-written-in-visual-c--.md).</span></span>

<span data-ttu-id="1dc9c-108">A meno che non si stia attualmente eseguendo il debug di multithreading, rilevamento componenti, chiamate remote o isolamento dei processi, è possibile usare l'ambiente Microsoft Visual Basic a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="1dc9c-108">Unless you are currently debugging multithreading, component tracking, remote calls, or process isolation, you can use the Microsoft Visual Basic environment for debugging purposes.</span></span> <span data-ttu-id="1dc9c-109">Il [debug di componenti scritti in Visual Basic](debugging-components-written-in-visual-basic.md) descrive il processo di debug all'interno di un ambiente Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1dc9c-109">[Debugging Components Written in Visual Basic](debugging-components-written-in-visual-basic.md) describes the debugging process within a Visual Basic environment.</span></span>

<span data-ttu-id="1dc9c-110">Il debug dell'argomento [nell'IDE di Visual Basic](debugging-in-the-visual-basic-ide.md) fornisce una panoramica generale con linee guida, suggerimenti e una procedura per il debug nell'Integrated Development Environment (IDE).</span><span class="sxs-lookup"><span data-stu-id="1dc9c-110">The topic [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md) provides a general overview with guidelines, tips and a procedure on debugging in the integrated development environment (IDE).</span></span>

<span data-ttu-id="1dc9c-111">Per visualizzare altre informazioni sul debug di processi avanzati, vedere [debug di componenti Visual Basic compilati](debugging-compiled-visual-basic-components.md).</span><span class="sxs-lookup"><span data-stu-id="1dc9c-111">To view more information about debugging advanced processes, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

> [!Note]  
> <span data-ttu-id="1dc9c-112">Per COM+ sono state risolte diverse limitazioni associate all'uso dell'ambiente Visual Basic per eseguire il debug dei componenti con MTS.</span><span class="sxs-lookup"><span data-stu-id="1dc9c-112">Several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="1dc9c-113">Per ulteriori informazioni, vedere [COM+ Visual Basic il supporto per il debug in contrapposizione a MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span><span class="sxs-lookup"><span data-stu-id="1dc9c-113">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1dc9c-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1dc9c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dc9c-115">Gestione degli errori in COM+</span><span class="sxs-lookup"><span data-stu-id="1dc9c-115">Handling Errors in COM+</span></span>](handling-errors-in-com-.md)
</dt> </dl>

 

 



