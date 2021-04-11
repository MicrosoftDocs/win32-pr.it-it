---
description: Poiché in molti casi sarà possibile eseguire il debug solo di una parte della funzionalità dei componenti all'interno dell'ambiente Microsoft Visual Basic, in alcune situazioni sarà necessario eseguire il debug dei componenti compilati con Visual Basic dopo che sono stati compilati. Poiché l'ambiente Visual Basic non lo Abilita, è necessario usare invece l'ambiente Microsoft Visual C++.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Debug di componenti Visual Basic compilati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b32a39f0f1c50e1da4c9534b40658838361225
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126711"
---
# <a name="debugging-compiled-visual-basic-components"></a><span data-ttu-id="87050-104">Debug di componenti Visual Basic compilati</span><span class="sxs-lookup"><span data-stu-id="87050-104">Debugging Compiled Visual Basic Components</span></span>

<span data-ttu-id="87050-105">Poiché in molti casi sarà possibile eseguire il debug solo di una parte delle funzionalità del componente all'interno dell'ambiente Microsoft Visual Basic, in alcune situazioni sarà necessario eseguire il debug dei componenti compilati con Visual Basic dopo che sono stati compilati.</span><span class="sxs-lookup"><span data-stu-id="87050-105">Given that in many cases you will be able to debug only a portion of your component's functionality within the Microsoft Visual Basic environment, there will be situations in which you will need to debug components built with Visual Basic after they have been compiled.</span></span> <span data-ttu-id="87050-106">Poiché l'ambiente Visual Basic non lo Abilita, è necessario usare invece l'ambiente Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="87050-106">Since the Visual Basic environment doesn't enable this, you must instead use the Microsoft Visual C++ environment.</span></span>

<span data-ttu-id="87050-107">**Per eseguire il debug di un componente Visual Basic nell'ambiente Visual C++**</span><span class="sxs-lookup"><span data-stu-id="87050-107">**To debug a Visual Basic component in the Visual C++ environment**</span></span>

1.  <span data-ttu-id="87050-108">In Visual Basic 6,0 aprire il progetto Visual Basic di cui si desidera eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="87050-108">In Visual Basic 6.0, open the Visual Basic project that you want to debug.</span></span>

2.  <span data-ttu-id="87050-109">Scegliere **Make YourProject.dll** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="87050-109">On the **File** menu, click **Make YourProject.dll**.</span></span>

3.  <span data-ttu-id="87050-110">Nella finestra di dialogo **Crea progetto** fare clic su **Opzioni**.</span><span class="sxs-lookup"><span data-stu-id="87050-110">In the **Make Project** dialog box, click **Options**.</span></span>

4.  <span data-ttu-id="87050-111">Nella scheda **Compila** della finestra di dialogo **Proprietà progetto** fare clic su **Compila in codice nativo** e **Nessuna ottimizzazione** , quindi selezionare la casella di controllo **Crea informazioni di debug simbolico** .</span><span class="sxs-lookup"><span data-stu-id="87050-111">In the **Project Properties** dialog box, on the **Compile** tab, click **Compile to Native Code** and **No Optimization** and select the **Create Symbolic Debug Info** check box.</span></span>

5.  <span data-ttu-id="87050-112">Fare clic su **OK**, quindi fare di nuovo clic su **OK** per compilare il progetto.</span><span class="sxs-lookup"><span data-stu-id="87050-112">Click **OK**, and then click **OK** again to compile your project.</span></span>

6.  <span data-ttu-id="87050-113">Spostare la DLL compilata nel percorso in cui sono normalmente installate le applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="87050-113">Move the compiled DLL to the location where COM+ applications are normally installed.</span></span>

    > [!Note]  
    > <span data-ttu-id="87050-114">Se la DLL non viene spostata, potrebbe essere presente un messaggio di errore che informa che non è stato possibile trovare le informazioni di debug simboliche per la DLL.</span><span class="sxs-lookup"><span data-stu-id="87050-114">If you don't move the DLL, you may get an error message informing you that symbolic debugging information for the DLL could not be located.</span></span> <span data-ttu-id="87050-115">Se si verificano problemi durante l'arresto del debugger in corrispondenza di punti di interruzione nel componente, verificare che la DLL si trovi nella directory dei pacchetti standard, eliminare il componente dal pacchetto e aggiungere nuovamente il componente.</span><span class="sxs-lookup"><span data-stu-id="87050-115">If you have trouble getting the debugger to stop at breakpoints in your component, confirm that the DLL is in the standard packages directory, delete the component from its package, and re-add the component.</span></span>

     

7.  <span data-ttu-id="87050-116">Avviare Visual C++.</span><span class="sxs-lookup"><span data-stu-id="87050-116">Start Visual C++.</span></span>

8.  <span data-ttu-id="87050-117">Scegliere **Apri area di lavoro** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="87050-117">On the **File** menu, click **Open Workspace**.</span></span>

9.  <span data-ttu-id="87050-118">Nella finestra di dialogo **Apri area di lavoro** impostare **file di tipo** su **tutti i file ( \* . \* )**, selezionare il componente compilato e fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="87050-118">In the **Open Workspace** dialog box, set **Files of Type** to **All files(\*.\*)**, select your compiled component, and click **Open**.</span></span>

10. <span data-ttu-id="87050-119">Dal menu **file** , fare clic su **Apri** (non **aprire area di lavoro**) e aprire il modulo Visual Basic (. Bas), il form (. frm) o la classe (. CLS) di cui si desidera eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="87050-119">From the **File** menu, click **Open** (not **Open Workspace**) and open the Visual Basic module (.bas), form (.frm), or class (.cls) that you want to debug.</span></span>

11. <span data-ttu-id="87050-120">Scegliere **Impostazioni** dal menu **progetto** .</span><span class="sxs-lookup"><span data-stu-id="87050-120">On the **Project** menu, click **Settings**.</span></span>

12. <span data-ttu-id="87050-121">Nella scheda **debug** della finestra di dialogo **Impostazioni progetto** selezionare **generale** nella casella **categoria** .</span><span class="sxs-lookup"><span data-stu-id="87050-121">In the **Project Settings** dialog box, on the **Debug** tab, select **General** in the **Category** box.</span></span>

13. <span data-ttu-id="87050-122">Nella casella **eseguibile per la sessione di debug** immettere il percorso completo per Dllhost.exe, seguito da un argomento che specifica l'ID di processo dell'applicazione com+ contenente il componente.</span><span class="sxs-lookup"><span data-stu-id="87050-122">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the process ID of the COM+ application containing the component.</span></span> <span data-ttu-id="87050-123">L'ID del processo è presente nella scheda **generale** della finestra di dialogo **Proprietà** dell'applicazione com+.</span><span class="sxs-lookup"><span data-stu-id="87050-123">You will find the process ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="87050-124">Di seguito è riportato un esempio: C: \\ WinNT \\ system32 \\Dllhost.exe/ProcessId: { <processID> }.</span><span class="sxs-lookup"><span data-stu-id="87050-124">Following is an example: C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{<processID>}.</span></span>

14. <span data-ttu-id="87050-125">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="87050-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87050-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87050-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87050-127">Supporto per il debug di Visual Basic COM+ a differenza di MTS</span><span class="sxs-lookup"><span data-stu-id="87050-127">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="87050-128">Debug nell'IDE di Visual Basic</span><span class="sxs-lookup"><span data-stu-id="87050-128">Debugging in the Visual Basic IDE</span></span>](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



