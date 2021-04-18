---
description: Quando si è pronti per eseguire il debug della funzionalità COM+ nei componenti di Microsoft Visual C++, è possibile configurare Visual C++ progetto o lo strumento di amministrazione Servizi componenti per avviare il debugger.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: Debug di componenti scritti in Visual C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304629"
---
# <a name="debugging-components-written-in-visual-c"></a><span data-ttu-id="d81d1-103">Debug di componenti scritti in Visual C++</span><span class="sxs-lookup"><span data-stu-id="d81d1-103">Debugging Components Written in Visual C++</span></span>

<span data-ttu-id="d81d1-104">Quando si è pronti per eseguire il debug della funzionalità COM+ nei componenti di Microsoft Visual C++, è possibile configurare Visual C++ progetto o lo strumento di amministrazione Servizi componenti per avviare il debugger.</span><span class="sxs-lookup"><span data-stu-id="d81d1-104">When you are ready to debug the COM+ functionality in your Microsoft Visual C++ components, you can configure Visual C++ project or the Component Services administrative tool to launch the debugger.</span></span> <span data-ttu-id="d81d1-105">Se si utilizza Visual C++, è possibile eseguire il debug con un client remoto utilizzando la RPC OLE e il debug JIT (just-in-Time).</span><span class="sxs-lookup"><span data-stu-id="d81d1-105">If you are using Visual C++, you can debug with a remote client using OLE RPC and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="d81d1-106">Se non si riesce a eseguire il client nel debugger o se il client è in esecuzione in un altro computer, è possibile usare l'impostazione **di avvio com+ in debugger** .</span><span class="sxs-lookup"><span data-stu-id="d81d1-106">If you are unable to run your client under the debugger or if the client is running on another machine, you can use the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="d81d1-107">Lo strumento di amministrazione Servizi componenti è presente in come casella di controllo nella scheda **Avanzate** della finestra di dialogo **Proprietà** applicazione com+.</span><span class="sxs-lookup"><span data-stu-id="d81d1-107">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span>

<span data-ttu-id="d81d1-108">Al termine del debug, è necessario arrestare le applicazioni COM+ di cui si esegue il debug.</span><span class="sxs-lookup"><span data-stu-id="d81d1-108">When you are finished debugging, you should shut down the COM+ applications you are debugging.</span></span> <span data-ttu-id="d81d1-109">Se un processo server viene lasciato in esecuzione, è possibile che venga generato un messaggio di errore al successivo tentativo di compilazione di una DLL quando la DLL esistente è ancora caricata in memoria.</span><span class="sxs-lookup"><span data-stu-id="d81d1-109">If a server process is left running, you might get an error message the next time you try to build a DLL when the existing DLL is still loaded in memory.</span></span> <span data-ttu-id="d81d1-110">Per arrestare un'applicazione COM+, fare clic con il pulsante destro del mouse sull'applicazione nell'albero della console e quindi scegliere **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="d81d1-110">To shut down a COM+ application, right-click the application in the console tree and then click **Shut down**.</span></span>

> [!Note]  
> <span data-ttu-id="d81d1-111">Se si utilizzano le transazioni, potrebbe essere necessario aumentare anche il timeout della transazione, il cui valore predefinito è 60 secondi.</span><span class="sxs-lookup"><span data-stu-id="d81d1-111">If you are using transactions, you might also want to increase the transaction time-out, which defaults to 60 seconds.</span></span> <span data-ttu-id="d81d1-112">È anche possibile specificare un valore pari a 0, specificando in modo efficace un periodo di timeout delle transazioni infinito.</span><span class="sxs-lookup"><span data-stu-id="d81d1-112">You can also specify a value of 0, effectively specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="d81d1-113">Utilizzando lo strumento di amministrazione Servizi componenti, modificare l'impostazione di timeout della transazione nella scheda **Opzioni** della finestra **Proprietà computer locale** .</span><span class="sxs-lookup"><span data-stu-id="d81d1-113">Using the Component Services administrative tool, change the transaction time-out setting on the **Options** tab of the **My Computer Properties** window.</span></span>

 

## <a name="debugging-server-application-components-with-visual-c"></a><span data-ttu-id="d81d1-114">Debug dei componenti dell'applicazione server con Visual C++</span><span class="sxs-lookup"><span data-stu-id="d81d1-114">Debugging Server Application Components with Visual C++</span></span>

<span data-ttu-id="d81d1-115">Quando si esegue il debug di applicazioni server COM+, è possibile eseguire il debug delle chiamate remote caricando il client e l'applicazione server nel debugger.</span><span class="sxs-lookup"><span data-stu-id="d81d1-115">When debugging COM+ server applications, you may want to debug remote calls by loading both the client and the server application into the debugger.</span></span> <span data-ttu-id="d81d1-116">Con Visual C++, è possibile eseguire il debug delle chiamate remote ai componenti tramite le impostazioni JIT (just-in-Time) e OLE RPC.</span><span class="sxs-lookup"><span data-stu-id="d81d1-116">With Visual C++, you can debug remote calls to your components through the just-in-time (JIT) and OLE RPC settings.</span></span> <span data-ttu-id="d81d1-117">L'impostazione JIT induce il componente compilato ad avviare il debugger Visual C++ quando si verifica un errore. l'impostazione OLE RPC consente al debugger di eseguire il passaggio da client a componente mentre si esegue il codice un'istruzione alla volta.</span><span class="sxs-lookup"><span data-stu-id="d81d1-117">The JIT setting causes the compiled component to start the Visual C++ debugger when an error occurs; the OLE RPC setting enables the debugger to step from client to component as you step through your code.</span></span>

<span data-ttu-id="d81d1-118">Quando queste funzionalità sono abilitate, è possibile avviare il client nel debugger.</span><span class="sxs-lookup"><span data-stu-id="d81d1-118">When these features are enabled, you can start your client under the debugger.</span></span> <span data-ttu-id="d81d1-119">Quando il client effettua una chiamata al componente, il debugger eseguirà l'istruzione nel codice del componente nel processo server, anche se il server si trova in un computer diverso nella rete.</span><span class="sxs-lookup"><span data-stu-id="d81d1-119">When the client makes a call to your component, the debugger will step into the component's code in the server process, even if the server is on a different computer on the network.</span></span> <span data-ttu-id="d81d1-120">Una sessione di debug viene avviata automaticamente nel computer server, se necessario.</span><span class="sxs-lookup"><span data-stu-id="d81d1-120">A debugging session is automatically started on the server computer if necessary.</span></span> <span data-ttu-id="d81d1-121">Analogamente, il passaggio successivo dell'istruzione return nel codice del componente restituirà il debug all'istruzione successiva nel codice del client.</span><span class="sxs-lookup"><span data-stu-id="d81d1-121">Similarly, single stepping past the return statement in the component's code will return debugging to the next statement in the client's code.</span></span>

> [!Note]  
> <span data-ttu-id="d81d1-122">È possibile salvare alcuni passaggi utilizzando l'impostazione di **avvio com+ in debugger** .</span><span class="sxs-lookup"><span data-stu-id="d81d1-122">You may be able to save a few steps by using the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="d81d1-123">In questo modo è possibile specificare il debugger Visual C++ (o un altro) senza dover effettuare particolari impostazioni di debug nell'ambiente Visual C++.</span><span class="sxs-lookup"><span data-stu-id="d81d1-123">This allows you to specify the Visual C++ (or other) debugger without having to make special debug settings in the Visual C++ environment.</span></span> <span data-ttu-id="d81d1-124">Lo strumento di amministrazione Servizi componenti è presente in come casella di controllo nella scheda **Avanzate** della finestra di dialogo **Proprietà** applicazione com+.</span><span class="sxs-lookup"><span data-stu-id="d81d1-124">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span> <span data-ttu-id="d81d1-125">Per ulteriori informazioni, vedere "debug senza Visual C++" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="d81d1-125">For more information, see "Debugging Without Visual C++" in this topic.</span></span>

 

<span data-ttu-id="d81d1-126">Quando l'applicazione COM+ che contiene il componente è un'applicazione server, è necessario innanzitutto arrestare l'applicazione utilizzando lo strumento di amministrazione Servizi componenti.</span><span class="sxs-lookup"><span data-stu-id="d81d1-126">When the COM+ application containing your component is a server application, you must begin by shutting down the application using the Component Services administrative tool.</span></span> <span data-ttu-id="d81d1-127">A tale scopo, fare clic con il pulsante destro del mouse sull'applicazione COM+ nell'albero della console e quindi scegliere **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="d81d1-127">To do this, right-click the COM+ application in the console tree and then click **Shut down**.</span></span>

<span data-ttu-id="d81d1-128">**Per abilitare il debug RPC in Visual C++**</span><span class="sxs-lookup"><span data-stu-id="d81d1-128">**To enable RPC debugging in Visual C++**</span></span>

1.  <span data-ttu-id="d81d1-129">In Visual C++ scegliere **Opzioni** dal menu **strumenti** .</span><span class="sxs-lookup"><span data-stu-id="d81d1-129">In Visual C++, on the **Tools** menu, click **Options**.</span></span>

2.  <span data-ttu-id="d81d1-130">Nella scheda **debug** della finestra di dialogo **Opzioni** selezionare le caselle di controllo debug **RPC OLE** e **debug JIT** .</span><span class="sxs-lookup"><span data-stu-id="d81d1-130">In the **Options** dialog box, on the **Debug** tab, select the **OLE RPC debugging** and **Just-in time debugging** check boxes.</span></span>

3.  <span data-ttu-id="d81d1-131">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="d81d1-131">Click **OK**.</span></span>

<span data-ttu-id="d81d1-132">Per iniziare il debug, avviare il progetto client nel debugger.</span><span class="sxs-lookup"><span data-stu-id="d81d1-132">To begin debugging, start your client project in the debugger.</span></span>

<span data-ttu-id="d81d1-133">È anche possibile eseguire il debug del componente senza avviare il client nel debugger.</span><span class="sxs-lookup"><span data-stu-id="d81d1-133">You can also debug your component without launching your client in the debugger.</span></span> <span data-ttu-id="d81d1-134">In questo caso, il componente deve avviare il debugger autonomamente.</span><span class="sxs-lookup"><span data-stu-id="d81d1-134">In this case, your component must launch the debugger on its own.</span></span> <span data-ttu-id="d81d1-135">Per eseguire questa operazione, è necessario che il progetto componente specifichi un eseguibile per la sessione di debug, insieme all'ID applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="d81d1-135">To do this, your component project must specify an executable for the debug session, along with the COM+ application ID.</span></span>

<span data-ttu-id="d81d1-136">**Per abilitare un componente dell'applicazione server per avviare il debugger Visual C++**</span><span class="sxs-lookup"><span data-stu-id="d81d1-136">**To enable a server application component to launch the Visual C++ debugger**</span></span>

1.  <span data-ttu-id="d81d1-137">Scegliere **Impostazioni** dal menu **progetto** .</span><span class="sxs-lookup"><span data-stu-id="d81d1-137">On the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="d81d1-138">Nella finestra di dialogo **Impostazioni progetto** , nella casella **impostazioni per** Selezionare **debug Win32**.</span><span class="sxs-lookup"><span data-stu-id="d81d1-138">In the **Project Settings** dialog box, in the **Settings For** box, select **Win32 Debug**.</span></span>

3.  <span data-ttu-id="d81d1-139">Nella scheda **debug** della casella **categoria** Selezionare **generale**.</span><span class="sxs-lookup"><span data-stu-id="d81d1-139">On the **Debug** tab, in the **Category** box, select **General**.</span></span>

4.  <span data-ttu-id="d81d1-140">Nella casella **eseguibile per la sessione di debug** immettere il percorso completo per Dllhost.exe, seguito da un argomento che specifica l'ID applicazione dell'applicazione com+ contenente il componente.</span><span class="sxs-lookup"><span data-stu-id="d81d1-140">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the application ID of the COM+ application containing the component.</span></span>

    > [!Note]  
    > <span data-ttu-id="d81d1-141">Utilizzando lo strumento di amministrazione Servizi componenti, sarà possibile trovare l'ID applicazione nella scheda **generale** della finestra di dialogo **Proprietà** dell'applicazione com+.</span><span class="sxs-lookup"><span data-stu-id="d81d1-141">Using the Component Services administrative tool, you will find the application ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="d81d1-142">Di seguito è illustrato un esempio:</span><span class="sxs-lookup"><span data-stu-id="d81d1-142">Following is an example:</span></span>

     

    > [!Note]  
    > <span data-ttu-id="d81d1-143">C: \\ WinNT \\ system32 \\Dllhost.exe/ProcessId: {applicationID}</span><span class="sxs-lookup"><span data-stu-id="d81d1-143">C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{applicationID}</span></span>

     

5.  <span data-ttu-id="d81d1-144">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="d81d1-144">Click **OK**.</span></span>

<span data-ttu-id="d81d1-145">È ora possibile impostare punti di interruzione, avviare il debugger e iniziare a eseguire chiamate al componente.</span><span class="sxs-lookup"><span data-stu-id="d81d1-145">You can now set breakpoints, start the debugger, and begin making calls to your component.</span></span>

## <a name="debugging-library-application-components-with-visual-c"></a><span data-ttu-id="d81d1-146">Debug dei componenti dell'applicazione libreria con Visual C++</span><span class="sxs-lookup"><span data-stu-id="d81d1-146">Debugging Library Application Components with Visual C++</span></span>

<span data-ttu-id="d81d1-147">Per eseguire il debug dei componenti in un'applicazione di libreria, è necessario configurare il progetto del client perché il processo del client ospiterà l'applicazione della libreria.</span><span class="sxs-lookup"><span data-stu-id="d81d1-147">To debug components in a library application, you must configure the client's project because the client's process will host the library application.</span></span>

<span data-ttu-id="d81d1-148">**Per abilitare il debug dell'applicazione libreria con Visual C++**</span><span class="sxs-lookup"><span data-stu-id="d81d1-148">**To enable library application debugging with Visual C++**</span></span>

1.  <span data-ttu-id="d81d1-149">In Visual C++ scegliere **Impostazioni** dal menu **progetto** .</span><span class="sxs-lookup"><span data-stu-id="d81d1-149">In Visual C++, on the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="d81d1-150">Nella finestra di dialogo **Impostazioni progetto** , nella casella **impostazioni per** , fare clic su **debug Win32**.</span><span class="sxs-lookup"><span data-stu-id="d81d1-150">In the **Project Settings** dialog box, in the **Settings For** box, click **Win32 Debug**.</span></span>

3.  <span data-ttu-id="d81d1-151">Nella scheda **debug** della casella **categoria** fare clic su **DLL aggiuntive**.</span><span class="sxs-lookup"><span data-stu-id="d81d1-151">On the **Debug** tab, in the **Category** box, click **Additional DLLs**.</span></span>

4.  <span data-ttu-id="d81d1-152">Nell'elenco **moduli** aggiungere le dll del componente nell'applicazione libreria.</span><span class="sxs-lookup"><span data-stu-id="d81d1-152">In the **Modules** list, add the component DLLs in your library application.</span></span> <span data-ttu-id="d81d1-153">In questo modo è possibile impostare punti di interruzione prima che la DLL venga effettivamente caricata.</span><span class="sxs-lookup"><span data-stu-id="d81d1-153">This allows you to set breakpoints before your DLL is actually loaded.</span></span>

5.  <span data-ttu-id="d81d1-154">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="d81d1-154">Click **OK**.</span></span>

## <a name="debugging-without-visual-c"></a><span data-ttu-id="d81d1-155">Debug senza Visual C++</span><span class="sxs-lookup"><span data-stu-id="d81d1-155">Debugging Without Visual C++</span></span>

<span data-ttu-id="d81d1-156">Indipendentemente dall'utilizzo Visual C++ per il debug, è possibile utilizzare l'impostazione **avvia in debugger** per specificare il debugger in cui devono essere eseguiti i componenti.</span><span class="sxs-lookup"><span data-stu-id="d81d1-156">Whether or not you are using Visual C++ for debugging, you can use the **Launch in debugger** setting to specify the debugger in which your components should run.</span></span>

<span data-ttu-id="d81d1-157">**Per specificare un debugger dallo strumento di amministrazione Servizi componenti**</span><span class="sxs-lookup"><span data-stu-id="d81d1-157">**To specify a debugger from the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="d81d1-158">Nell'albero della console selezionare l'applicazione libreria COM+ contenente i componenti di cui si desidera eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="d81d1-158">In the console tree, select the COM+ library application containing the components you wish to debug.</span></span>

2.  <span data-ttu-id="d81d1-159">Fare clic con il pulsante destro del mouse sull'applicazione, quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="d81d1-159">Right-click the application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="d81d1-160">Nella finestra di dialogo **Proprietà** dell'applicazione fare clic sulla scheda **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="d81d1-160">In the application's **Properties** dialog box, click the **Advanced** tab.</span></span>

4.  <span data-ttu-id="d81d1-161">In **debug** selezionare la casella **di controllo avvia nel debugger** .</span><span class="sxs-lookup"><span data-stu-id="d81d1-161">Under **Debugging**, select the **Launch in debugger** check box.</span></span>

5.  <span data-ttu-id="d81d1-162">Nella casella **percorso debugger** immettere il percorso del debugger che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="d81d1-162">In the **Debugger path** box, enter path to the debugger you want to use.</span></span> <span data-ttu-id="d81d1-163">È anche possibile fare clic su **Sfoglia** per individuare il debugger.</span><span class="sxs-lookup"><span data-stu-id="d81d1-163">You can also click **Browse** to locate the debugger.</span></span> <span data-ttu-id="d81d1-164">Di seguito è riportato un esempio: C: \\ WinNT \\ system32 \\Ntsd.exe.</span><span class="sxs-lookup"><span data-stu-id="d81d1-164">Following is an example: C:\\Winnt\\System32\\Ntsd.exe.</span></span>

6.  <span data-ttu-id="d81d1-165">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="d81d1-165">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d81d1-166">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d81d1-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d81d1-167">Debug di componenti scritti in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="d81d1-167">Debugging Components Written in Visual Basic</span></span>](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



