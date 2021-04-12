---
description: L'uso di Microsoft Visual Basic Integrated Development Environment (IDE) per il debug offre agli sviluppatori Visual Basic l'accesso a strumenti e semplicità d'uso noti.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Debug nell'IDE di Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401400"
---
# <a name="debugging-in-the-visual-basic-ide"></a><span data-ttu-id="1dc10-103">Debug nell'IDE di Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1dc10-103">Debugging in the Visual Basic IDE</span></span>

<span data-ttu-id="1dc10-104">L'uso di Microsoft Visual Basic Integrated Development Environment (IDE) per il debug offre agli sviluppatori Visual Basic l'accesso a strumenti e semplicità d'uso noti.</span><span class="sxs-lookup"><span data-stu-id="1dc10-104">Using the Microsoft Visual Basic integrated development environment (IDE) for debugging gives Visual Basic developers access to familiar tools and ease-of-use.</span></span> <span data-ttu-id="1dc10-105">Sebbene sia necessario eseguire il debug di molti componenti in modo più completo utilizzando l'ambiente Microsoft Visual C++, una strategia potrebbe consistere nel eseguire prima il debug della maggior parte delle funzionalità possibili con Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1dc10-105">While many components will eventually need to be more fully debugged using the Microsoft Visual C++ environment, one strategy might be to first debug as much functionality as possible with Visual Basic.</span></span> <span data-ttu-id="1dc10-106">Ad esempio, è possibile usare l'IDE di Visual Basic per il debug all'interno di COM+ quando non è ancora in corso il debug del multithreading, il rilevamento dei componenti, le chiamate remote o l'isolamento dei processi.</span><span class="sxs-lookup"><span data-stu-id="1dc10-106">For example, you might want to use the Visual Basic IDE for debugging within COM+ when you aren't yet debugging multithreading, component tracking, remote calls, or process isolation.</span></span>

<span data-ttu-id="1dc10-107">In generale, quando si utilizza l'ambiente Visual Basic per il debug, è necessario innanzitutto compilare il progetto e aggiungere la DLL a un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="1dc10-107">In general, when using the Visual Basic environment for debugging, you first compile the project and add the DLL to a COM+ application.</span></span> <span data-ttu-id="1dc10-108">Si imposta quindi la compatibilità binaria per il progetto, si fa riferimento alla DLL creata e si avvia il progetto per avviare il debug.</span><span class="sxs-lookup"><span data-stu-id="1dc10-108">Then you set binary compatibility for the project, referencing the DLL you made, and start the project to begin debugging.</span></span>

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a><span data-ttu-id="1dc10-109">Linee guida generali per il debug nell'ambiente Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1dc10-109">General Guidelines for Debugging in the Visual Basic Environment</span></span>

-   <span data-ttu-id="1dc10-110">Durante il debug con Visual Basic, COM+ considera i componenti Visual Basic come se appartengano a un'applicazione di libreria, anche se i componenti sono registrati come appartenenti a un'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="1dc10-110">While you are debugging using Visual Basic, COM+ treats the Visual Basic components as if they belong to a library application, even if the components are registered as belonging to a server application.</span></span> <span data-ttu-id="1dc10-111">Poiché viene eseguito come applicazione libreria, le icone dei componenti nello strumento di amministrazione Servizi componenti non vengono spinte durante il debug dei componenti.</span><span class="sxs-lookup"><span data-stu-id="1dc10-111">Because it runs as a library application, the component icons in the Component Services administrative tool do not spin as the components are debugged.</span></span>
-   <span data-ttu-id="1dc10-112">Se si modificano gli attributi delle transazioni in un componente durante il debug o si crea una modifica del codice sorgente che richiede Visual Basic per generare un nuovo CLSID o ProgID, assicurarsi di eliminare e reinstallare l'applicazione COM+ contenente il componente.</span><span class="sxs-lookup"><span data-stu-id="1dc10-112">If you change transaction attributes on a component during debugging or make a source code change that requires Visual Basic to generate a new CLSID or ProgID, be sure to delete and reinstall the COM+ application containing the component.</span></span> <span data-ttu-id="1dc10-113">Se è stata impostata la compatibilità binaria per il componente, si riceverà un avviso per segnalare che si sono verificate modifiche.</span><span class="sxs-lookup"><span data-stu-id="1dc10-113">If you have set binary compatibility for the component, you will be warned that changes have occurred.</span></span>

## <a name="notes-on-debugging-within-a-com-application"></a><span data-ttu-id="1dc10-114">Note sul debug in un'applicazione COM+</span><span class="sxs-lookup"><span data-stu-id="1dc10-114">Notes on Debugging Within a COM+ Application</span></span>

-   <span data-ttu-id="1dc10-115">Se si apportano modifiche nell'IDE di Visual Basic nelle interfacce del componente, nomi di classi, nomi di progetti, supporto transazionale o altre impostazioni, potrebbe esserci una mancata corrispondenza tra i dati di configurazione in Esplora servizi componenti e la configurazione effettiva in esecuzione nel debugger di Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1dc10-115">If you make changes in the Visual Basic IDE in your component's interfaces, class names, project names, transactional support or other settings, there may be mismatches between the configuration data in the Component Services explorer and the actual configuration running in the Visual Basic debugger.</span></span>
-   <span data-ttu-id="1dc10-116">Non esportare un'applicazione COM+ durante il debug di un componente nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1dc10-116">Do not export a COM+ application while you are debugging a component in the application.</span></span> <span data-ttu-id="1dc10-117">COM+ considererà l'ambiente di sviluppo Visual Basic come componente.</span><span class="sxs-lookup"><span data-stu-id="1dc10-117">COM+ will treat the Visual Basic development environment as the component.</span></span>
-   <span data-ttu-id="1dc10-118">Se si esegue un componente all'esterno del debugger e si decide di avviare il debug, un'istanza del componente potrebbe essere ancora in esecuzione in COM+ quando viene avviata nel debugger.</span><span class="sxs-lookup"><span data-stu-id="1dc10-118">If you are running a component outside the debugger and then decide to begin debugging, an instance of the component may still be running in COM+ when you start it in the debugger.</span></span> <span data-ttu-id="1dc10-119">COM+ rileverà questa condizione e tenterà di arrestare automaticamente l'istanza che controlla.</span><span class="sxs-lookup"><span data-stu-id="1dc10-119">COM+ will detect this condition and attempt to silently shut down the instance it controls.</span></span> <span data-ttu-id="1dc10-120">Per evitare questo problema, rimuovere il componente dallo strumento di amministrazione Servizi componenti prima di avviare il debug.</span><span class="sxs-lookup"><span data-stu-id="1dc10-120">To avoid this problem, remove the component from the Component Services administrative tool before you begin debugging.</span></span>

<span data-ttu-id="1dc10-121">**Per eseguire il debug con l'ambiente Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="1dc10-121">**To debug using the Visual Basic environment**</span></span>

1.  <span data-ttu-id="1dc10-122">Aprire il progetto componente in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1dc10-122">Open the component project in Visual Basic.</span></span>

2.  <span data-ttu-id="1dc10-123">Compilare il componente, quindi impostare la compatibilità binaria nel progetto sul componente compilato.</span><span class="sxs-lookup"><span data-stu-id="1dc10-123">Compile your component, and then set binary compatibility in your project to the compiled component.</span></span>

3.  <span data-ttu-id="1dc10-124">Impostare la proprietà MTSTransactionMode su un valore diverso da 0-NotAnMTSObject.</span><span class="sxs-lookup"><span data-stu-id="1dc10-124">Set the MTSTransactionMode property to a value other than 0 - NotAnMTSObject.</span></span> <span data-ttu-id="1dc10-125">Quando si avvia il progetto, questa impostazione richiede Visual Basic per attivare il componente all'interno di COM+.</span><span class="sxs-lookup"><span data-stu-id="1dc10-125">When you start the project, this setting prompts Visual Basic to activate your component within COM+.</span></span>

4.  <span data-ttu-id="1dc10-126">Scegliere **Proprietà** dal menu **progetto** , quindi immettere il programma avvia nella scheda **debug** . Il programma di avvio è l'eseguibile del client che chiama il componente.</span><span class="sxs-lookup"><span data-stu-id="1dc10-126">From the **Project** menu, click **Properties**, and then enter the start program on the **Debugging** tab. The start program is the client executable that calls this component.</span></span>

    > [!Note]  
    > <span data-ttu-id="1dc10-127">Il programma di avvio deve essere locale per il componente di cui si esegue il debug.</span><span class="sxs-lookup"><span data-stu-id="1dc10-127">The start program must be local to the component you are debugging.</span></span>

     

5.  <span data-ttu-id="1dc10-128">Premere il tasto F5 per avviare il debug del componente.</span><span class="sxs-lookup"><span data-stu-id="1dc10-128">Press the F5 key to begin debugging the component.</span></span>

<span data-ttu-id="1dc10-129">Dopo aver premuto F5, Visual Basic avvia l'applicazione client ed esegue il componente in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="1dc10-129">After you press F5, Visual Basic launches the client application and runs the component in debug mode.</span></span> <span data-ttu-id="1dc10-130">È possibile inserire punti di interruzione nel codice del componente e impostare gli orologi sulle variabili.</span><span class="sxs-lookup"><span data-stu-id="1dc10-130">You can place breakpoints in the component's code and set watches on variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dc10-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1dc10-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dc10-132">Supporto per il debug di Visual Basic COM+ a differenza di MTS</span><span class="sxs-lookup"><span data-stu-id="1dc10-132">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="1dc10-133">Debug di componenti Visual Basic compilati</span><span class="sxs-lookup"><span data-stu-id="1dc10-133">Debugging Compiled Visual Basic Components</span></span>](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



