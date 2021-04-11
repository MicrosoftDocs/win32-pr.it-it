---
title: Uso della procedura guidata plug-in con Visual Studio
description: Uso della procedura guidata plug-in con Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Plug-in di Windows Media Player, Visual Studio
- plug-in, Visual Studio
- creazione di plug-in, Visual Studio
- Creazione guidata plug-in di Windows Media Player, Visual Studio
- Visual Studio, creazione guidata plug-in di Windows Media Player
- procedura guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330711"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a><span data-ttu-id="54035-109">Uso della procedura guidata plug-in con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="54035-109">Using the Plug-in Wizard with Visual Studio</span></span>

<span data-ttu-id="54035-110">Dopo aver installato i componenti necessari, è possibile creare rapidamente un plug-in che funge da punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="54035-110">After you have installed the necessary components, you can quickly create a plug-in that will serve as a starting point.</span></span> <span data-ttu-id="54035-111">La procedura seguente illustra come eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="54035-111">The following steps will guide you.</span></span>

1.  <span data-ttu-id="54035-112">Avviare Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="54035-112">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="54035-113">Scegliere **nuovo** dal menu **file** , quindi fare clic su **progetto**.</span><span class="sxs-lookup"><span data-stu-id="54035-113">From the **File** menu, point to **New** and then click **Project**.</span></span>
3.  <span data-ttu-id="54035-114">In **Tipi progetto** selezionare **Visual C++ progetti**.</span><span class="sxs-lookup"><span data-stu-id="54035-114">In **Project Types**, select **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="54035-115">In **modelli** selezionare **creazione guidata plug-in di Windows Media Player**.</span><span class="sxs-lookup"><span data-stu-id="54035-115">In **Templates**, select **Windows Media Player Plug-in Wizard**.</span></span>
5.  <span data-ttu-id="54035-116">Immettere un nome per il progetto.</span><span class="sxs-lookup"><span data-stu-id="54035-116">Enter a name for your project.</span></span>
6.  <span data-ttu-id="54035-117">Immettere un percorso per il progetto.</span><span class="sxs-lookup"><span data-stu-id="54035-117">Enter a location for your project.</span></span> <span data-ttu-id="54035-118">Si tratta della cartella in cui verranno copiati i file di progetto.</span><span class="sxs-lookup"><span data-stu-id="54035-118">This is the folder to which your project files will be copied.</span></span>
7.  <span data-ttu-id="54035-119">Fare clic su **OK** per avviare la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="54035-119">Click **OK** to start the wizard.</span></span>
8.  <span data-ttu-id="54035-120">Selezionare il tipo di plug-in che si desidera creare.</span><span class="sxs-lookup"><span data-stu-id="54035-120">Select the type of plug-in you want to create.</span></span>
9.  <span data-ttu-id="54035-121">Completare tutte le finestre di dialogo rimanenti della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="54035-121">Complete any remaining dialog boxes in the wizard.</span></span>
10. <span data-ttu-id="54035-122">Usare l'ambiente di sviluppo di Visual Studio per compilare il progetto.</span><span class="sxs-lookup"><span data-stu-id="54035-122">Use the Visual Studio development environment to build your project.</span></span>
    > [!Note]  
    > <span data-ttu-id="54035-123">In Windows Vista e versioni successive il progetto non viene compilato correttamente a meno che non si esegua Visual Studio con un token di accesso amministratore completo.</span><span class="sxs-lookup"><span data-stu-id="54035-123">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="54035-124">Fare clic con il pulsante destro del mouse sul nome o sull'icona di Visual Studio e scegliere **Esegui come amministratore**.</span><span class="sxs-lookup"><span data-stu-id="54035-124">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

     

<span data-ttu-id="54035-125">Prima di provare a compilare il progetto, assicurarsi di configurare l'ambiente di sviluppo in modo che punti alle cartelle denominate include e lib in cui è stato installato il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="54035-125">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="54035-126">Il compilatore e il linker dovranno accedere ad alcuni file in queste cartelle.</span><span class="sxs-lookup"><span data-stu-id="54035-126">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="54035-127">Se è stata eseguita l'utilità di registrazione di Visual Studio fornita con la Windows SDK, è probabile che l'ambiente di sviluppo sia già stato configurato in modo da puntare al Windows SDK includere le cartelle e lib.</span><span class="sxs-lookup"><span data-stu-id="54035-127">If you ran the Visual Studio Registration utility that comes with the Windows SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="54035-128">In caso contrario, è necessario configurare manualmente l'ambiente di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="54035-128">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="54035-129">Per configurare manualmente Visual Studio, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="54035-129">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="54035-130">Scegliere **Opzioni** dal menu **Strumenti**.</span><span class="sxs-lookup"><span data-stu-id="54035-130">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="54035-131">Fare clic su **progetti e soluzioni** e quindi su **directory di VC + +**.</span><span class="sxs-lookup"><span data-stu-id="54035-131">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="54035-132">In **Mostra directory per** fare clic su **Includi file** o **file di libreria**.</span><span class="sxs-lookup"><span data-stu-id="54035-132">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="54035-133">Aggiungere le directory per i file necessari.</span><span class="sxs-lookup"><span data-stu-id="54035-133">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54035-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="54035-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54035-135">Creazione di un plug-in</span><span class="sxs-lookup"><span data-stu-id="54035-135">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> </dl>

 

 




