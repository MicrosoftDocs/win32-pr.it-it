---
description: In questo argomento viene illustrato come eseguire il debug di dll di estensione dello spazio dei nomi e Shell
title: Debug con la shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ca6e30809565408454976e1b07ff37dcc8f8f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525380"
---
# <a name="debugging-with-the-shell"></a><span data-ttu-id="aa81c-103">Debug con la shell</span><span class="sxs-lookup"><span data-stu-id="aa81c-103">Debugging with the Shell</span></span>

<span data-ttu-id="aa81c-104">In questo argomento viene illustrato come eseguire il debug di dll di estensione dello spazio dei nomi e Shell</span><span class="sxs-lookup"><span data-stu-id="aa81c-104">This topic explains how to debug Shell and namespace extension DLLs.</span></span>

-   [<span data-ttu-id="aa81c-105">Esecuzione della shell in un debugger</span><span class="sxs-lookup"><span data-stu-id="aa81c-105">Running the Shell Under a Debugger</span></span>](#running-the-shell-under-a-debugger)
-   [<span data-ttu-id="aa81c-106">Esecuzione e test delle estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="aa81c-106">Running and Testing Shell Extensions</span></span>](#running-and-testing-shell-extensions)
-   [<span data-ttu-id="aa81c-107">Scaricamento della DLL</span><span class="sxs-lookup"><span data-stu-id="aa81c-107">Unloading the DLL</span></span>](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a><span data-ttu-id="aa81c-108">Esecuzione della shell in un debugger</span><span class="sxs-lookup"><span data-stu-id="aa81c-108">Running the Shell Under a Debugger</span></span>

<span data-ttu-id="aa81c-109">Per eseguire il debug dell'estensione, è necessario eseguire la shell dal debugger.</span><span class="sxs-lookup"><span data-stu-id="aa81c-109">To debug your extension, you need to run the Shell from the debugger.</span></span> <span data-ttu-id="aa81c-110">A tale scopo, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="aa81c-110">Follow these steps:</span></span>

1.  <span data-ttu-id="aa81c-111">Caricare il progetto dell'estensione nel debugger, ma non eseguirlo.</span><span class="sxs-lookup"><span data-stu-id="aa81c-111">Load the extension's project into the debugger, but do not run it.</span></span>
2.  <span data-ttu-id="aa81c-112">Arrestare la Shell.</span><span class="sxs-lookup"><span data-stu-id="aa81c-112">Shut down the Shell.</span></span>

    -   <span data-ttu-id="aa81c-113">Per Windows Vista e versioni successive:</span><span class="sxs-lookup"><span data-stu-id="aa81c-113">For Windows Vista and later:</span></span>
        1.  <span data-ttu-id="aa81c-114">Visualizzare il menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="aa81c-114">Display the **Start** menu.</span></span>
        2.  <span data-ttu-id="aa81c-115">Premere CTRL + MAIUSC e fare clic con il pulsante destro del mouse sullo sfondo della metà destra del menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="aa81c-115">Press CTRL+SHIFT and right-click on the background of the right half of the **Start** menu.</span></span>
        3.  <span data-ttu-id="aa81c-116">Dal menu visualizzato scegliere **Esci da Esplora risorse**.</span><span class="sxs-lookup"><span data-stu-id="aa81c-116">From the menu that appears, choose **Exit Explorer**.</span></span>
    -   <span data-ttu-id="aa81c-117">Per Windows XP:</span><span class="sxs-lookup"><span data-stu-id="aa81c-117">For Windows XP:</span></span>
        1.  <span data-ttu-id="aa81c-118">Dal menu **Start** scegliere **Arresta**.</span><span class="sxs-lookup"><span data-stu-id="aa81c-118">From the **Start** menu, choose **Shut down**.</span></span>
        2.  <span data-ttu-id="aa81c-119">Premere CTRL + ALT + MAIUSC e fare clic su **No** nella finestra di dialogo **arresta Windows** .</span><span class="sxs-lookup"><span data-stu-id="aa81c-119">Press CTRL+ALT+SHIFT, and click **No** in the **Shut Down Windows** dialog box.</span></span>

    <span data-ttu-id="aa81c-120">La shell viene ora arrestata, ma tutte le altre applicazioni sono ancora in esecuzione, incluso il debugger.</span><span class="sxs-lookup"><span data-stu-id="aa81c-120">The Shell is now shut down, but all other applications are still running, including the debugger.</span></span>

3.  <span data-ttu-id="aa81c-121">Impostare il debugger per eseguire la DLL di estensione con Explorer.exe dalla directory **Windows** .</span><span class="sxs-lookup"><span data-stu-id="aa81c-121">Set the debugger to run the extension DLL with Explorer.exe from the **Windows** directory.</span></span>
4.  <span data-ttu-id="aa81c-122">Eseguire il progetto dal debugger.</span><span class="sxs-lookup"><span data-stu-id="aa81c-122">Run the project from the debugger.</span></span> <span data-ttu-id="aa81c-123">La shell verrà avviata come di consueto, ma il debugger verrà collegato al processo della shell.</span><span class="sxs-lookup"><span data-stu-id="aa81c-123">The Shell will launch as usual, but the debugger will be attached to the Shell's process.</span></span>

## <a name="running-and-testing-shell-extensions"></a><span data-ttu-id="aa81c-124">Esecuzione e test delle estensioni della shell</span><span class="sxs-lookup"><span data-stu-id="aa81c-124">Running and Testing Shell Extensions</span></span>

<span data-ttu-id="aa81c-125">È possibile eseguire e testare le estensioni in un processo separato di Esplora risorse per evitare di arrestare e riavviare il desktop e la barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="aa81c-125">You can run and test your extensions in a separate Windows Explorer process to avoid stopping and restarting the desktop and taskbar.</span></span> <span data-ttu-id="aa81c-126">Il desktop e la barra delle applicazioni possono essere ancora usati durante l'esecuzione e il test delle estensioni.</span><span class="sxs-lookup"><span data-stu-id="aa81c-126">Your desktop and taskbar can still be used while you run and test the extensions.</span></span>

<span data-ttu-id="aa81c-127">Per abilitare questa funzionalità, aggiungere la seguente \_ voce reg DWORD al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="aa81c-127">To enable this feature, add the following REG\_DWORD entry to the registry.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

<span data-ttu-id="aa81c-128">Per rendere effettive queste voci, è necessario disconnettersi e accedere di nuovo.</span><span class="sxs-lookup"><span data-stu-id="aa81c-128">For this entry to take effect, you must log off and log on again.</span></span> <span data-ttu-id="aa81c-129">Questa impostazione consente di creare le finestre del desktop e della barra delle applicazioni in un processo di Explorer.exe e tutte le altre finestre di esplorazione e cartella da aprire in un processo di Explorer.exe diverso.</span><span class="sxs-lookup"><span data-stu-id="aa81c-129">This setting causes the desktop and taskbar windows to be created in one Explorer.exe process and all other Explorer and folder windows to be opened in a different Explorer.exe process.</span></span>

<span data-ttu-id="aa81c-130">Oltre a rendere più semplice l'esecuzione e il test delle estensioni, questa impostazione rende il desktop più affidabile in quanto si riferisce alle estensioni della shell.</span><span class="sxs-lookup"><span data-stu-id="aa81c-130">In addition to making the running and testing of your extensions more convenient, this setting also makes the desktop more robust as it relates to Shell extensions.</span></span> <span data-ttu-id="aa81c-131">Molte estensioni di questo tipo (ad esempio, le estensioni del menu di scelta rapida) verranno caricate nel processo di Explorer.exe non desktop.</span><span class="sxs-lookup"><span data-stu-id="aa81c-131">Many such extensions (shortcut menu extensions, for example) will be loaded into the nondesktop Explorer.exe process.</span></span> <span data-ttu-id="aa81c-132">Se questo processo termina, il desktop e la barra delle applicazioni non saranno interessati e la finestra Esplora o cartella successiva creerà nuovamente il processo terminato.</span><span class="sxs-lookup"><span data-stu-id="aa81c-132">If this process terminates, the desktop and taskbar will be unaffected, and the next Explorer or folder window will re-create the terminated process.</span></span>

## <a name="unloading-the-dll"></a><span data-ttu-id="aa81c-133">Scaricamento della DLL</span><span class="sxs-lookup"><span data-stu-id="aa81c-133">Unloading the DLL</span></span>

<span data-ttu-id="aa81c-134">La shell Scarica automaticamente qualsiasi DLL quando il conteggio di utilizzo è pari a zero, ma solo dopo che la DLL non è stata utilizzata per un certo periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="aa81c-134">The Shell automatically unloads any DLL when its usage count is zero, but only after the DLL has not been used for a period of time.</span></span> <span data-ttu-id="aa81c-135">Questo periodo di tempo inattivo potrebbe essere inaccettabile a volte, soprattutto quando viene eseguito il debug di una DLL di estensione della shell.</span><span class="sxs-lookup"><span data-stu-id="aa81c-135">This inactive period might be unacceptably long at times, especially when a Shell extension DLL is being debugged.</span></span> <span data-ttu-id="aa81c-136">È possibile abbreviare il periodo di inattività aggiungendo le informazioni seguenti al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="aa81c-136">You can shorten the inactive period by adding the following information to the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



