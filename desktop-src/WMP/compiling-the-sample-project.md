---
title: Compilazione del progetto di esempio
description: Compilazione del progetto di esempio
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player Online Stores, compilazione di progetti di esempio
- negozi online, compilazione di progetti di esempio
- digitare 2 archivi online, compilazione di progetti di esempio
- Windows Media Player Online Stores, progetti di esempio
- negozi online, progetti di esempio
- digitare 2 archivi online, progetti di esempio
- Windows Media Player Online Stores, creazione guidata progetto
- negozi online, creazione guidata progetto
- digitare 2 archivi online, creazione guidata progetto
- plug-in, creazione guidata progetto
- Plug-in di Windows Media Player, creazione guidata progetto
- compilazione di progetti di esempio
- esempi, digitare 2 archivi online
- Creazione guidata progetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ea2382e5852965b246f1ef303e5e70d160cb22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298472"
---
# <a name="compiling-the-sample-project"></a><span data-ttu-id="88c88-117">Compilazione del progetto di esempio</span><span class="sxs-lookup"><span data-stu-id="88c88-117">Compiling the Sample Project</span></span>

<span data-ttu-id="88c88-118">La procedura guidata genera tutti i file necessari per compilare il progetto di esempio, pertanto non è necessario modificare le impostazioni predefinite del progetto.</span><span class="sxs-lookup"><span data-stu-id="88c88-118">The wizard generates all the files you need to compile the sample project, so you shouldn't need to change the default project settings.</span></span> <span data-ttu-id="88c88-119">In Visual Studio scegliere **Compila soluzione** dal menu **Compila** per compilare e registrare il componente com.</span><span class="sxs-lookup"><span data-stu-id="88c88-119">In Visual Studio, from the **Build** menu, click **Build Solution** to build and register the COM component.</span></span> <span data-ttu-id="88c88-120">Per impostazione predefinita, la configurazione di debug è attiva.</span><span class="sxs-lookup"><span data-stu-id="88c88-120">By default, the Debug configuration is active.</span></span>

> [!Note]  
> <span data-ttu-id="88c88-121">In Windows Vista e versioni successive il progetto non viene compilato correttamente a meno che non si esegua Visual Studio con un token di accesso amministratore completo.</span><span class="sxs-lookup"><span data-stu-id="88c88-121">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="88c88-122">Fare clic con il pulsante destro del mouse sul nome o sull'icona di Visual Studio e scegliere **Esegui come amministratore**.</span><span class="sxs-lookup"><span data-stu-id="88c88-122">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

 

<span data-ttu-id="88c88-123">Prima di provare a compilare il progetto, assicurarsi di configurare l'ambiente di sviluppo in modo che punti alle cartelle denominate include e lib in cui è stato installato il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="88c88-123">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="88c88-124">Il compilatore e il linker dovranno accedere ad alcuni file in queste cartelle.</span><span class="sxs-lookup"><span data-stu-id="88c88-124">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="88c88-125">Se è stata eseguita l'utilità di registrazione di Visual Studio fornita con Windows Vista SDK, è probabile che l'ambiente di sviluppo sia già stato configurato in modo da puntare all'Windows SDK includere le cartelle e lib.</span><span class="sxs-lookup"><span data-stu-id="88c88-125">If you ran the Visual Studio Registration utility that comes with the Windows Vista SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="88c88-126">In caso contrario, è necessario configurare manualmente l'ambiente di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="88c88-126">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="88c88-127">Per configurare manualmente Visual Studio, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="88c88-127">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="88c88-128">Scegliere **Opzioni** dal menu **Strumenti**.</span><span class="sxs-lookup"><span data-stu-id="88c88-128">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="88c88-129">Fare clic su **progetti e soluzioni** e quindi su **directory di VC + +**.</span><span class="sxs-lookup"><span data-stu-id="88c88-129">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="88c88-130">In **Mostra directory per** fare clic su **Includi file** o **file di libreria**.</span><span class="sxs-lookup"><span data-stu-id="88c88-130">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="88c88-131">Aggiungere le directory per i file necessari.</span><span class="sxs-lookup"><span data-stu-id="88c88-131">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88c88-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="88c88-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88c88-133">Creazione del plug-in per un negozio online di tipo 2</span><span class="sxs-lookup"><span data-stu-id="88c88-133">Building the Plug-in for a Type 2 Online Store</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




