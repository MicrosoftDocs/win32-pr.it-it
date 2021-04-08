---
title: Introduzione con Windows Media Player SDK
description: Introduzione con Windows Media Player SDK
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player Mobile, plug-in
- Plug-in di Windows Media Player Mobile, interfaccia utente
- Plug-in di Windows Media Player Mobile
- plug-in, interfaccia utente
- plug-in, Windows Media Player Mobile
- plug-in dell'interfaccia utente, Windows Media Player Mobile
- Plug-in dell'interfaccia utente, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739303"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a><span data-ttu-id="5071a-110">Introduzione con Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="5071a-110">Getting Started with the Windows Media Player SDK</span></span>

<span data-ttu-id="5071a-111">Per creare il plug-in, è prima di tutto necessario installare Microsoft eMbedded Visual C++ 4,0 e Visual Studio 2003.</span><span class="sxs-lookup"><span data-stu-id="5071a-111">To create your plug-in, you first need to install Microsoft eMbedded Visual C++ 4.0 and Visual Studio 2003.</span></span> <span data-ttu-id="5071a-112">È inoltre necessario installare Pocket PC 2003 SDK o Smartphone 2003 SDK, che sono download distinti.</span><span class="sxs-lookup"><span data-stu-id="5071a-112">You must also install the Pocket PC 2003 SDK or the Smartphone 2003 SDK, which are separate downloads.</span></span> <span data-ttu-id="5071a-113">Per compilare ed eseguire il progetto, un dispositivo Pocket PC o smartphone che esegue il sistema operativo Windows Mobile 2003 Second Edition deve essere sincronizzato con il computer di sviluppo tramite Microsoft ActiveSync® 3.7.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="5071a-113">To compile and run the project, a Pocket PC or Smartphone device running the Windows Mobile 2003 Second Edition operating system must be synchronized with the development computer by using Microsoft ActiveSync® 3.7.1 or later.</span></span>

<span data-ttu-id="5071a-114">Poiché i plug-in dell'interfaccia utente nei dispositivi Windows Mobile utilizzano lo stesso modello di plug-in delle versioni desktop, è possibile utilizzare la creazione guidata plug-in di Windows Media Player come punto di partenza per la creazione di un plug-in di interfaccia utente in background che funzionerà con Windows Media Player 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="5071a-114">Because UI plug-ins on Windows Mobile devices use the same plug-in model as the desktop versions, you can use the Windows Media Player Plug-in Wizard as a starting point when creating a background UI plug-in that will work with Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="5071a-115">Per creare il codice del plug-in dell'interfaccia utente, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5071a-115">To create UI plug-in code, do the following:</span></span>

1.  <span data-ttu-id="5071a-116">Aprire Visual Studio 2003 e avviare un nuovo progetto in Visual C++.</span><span class="sxs-lookup"><span data-stu-id="5071a-116">Open Visual Studio 2003, and start a new project in Visual C++.</span></span>
2.  <span data-ttu-id="5071a-117">Selezionare **creazione guidata plug-in di Windows Media Player** dal riquadro **modelli** .</span><span class="sxs-lookup"><span data-stu-id="5071a-117">Select **Windows Media Player Plug-in Wizard** from the **Templates** pane.</span></span>
3.  <span data-ttu-id="5071a-118">Assegnare al progetto il nome NetworkPlugin e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="5071a-118">Name your project NetworkPlugin and click **OK**.</span></span>
4.  <span data-ttu-id="5071a-119">Selezionare il **plug-in dell'interfaccia utente** e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="5071a-119">Select **UI Plug-in** and click **Next**.</span></span>
5.  <span data-ttu-id="5071a-120">Selezionare **sfondo** , quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="5071a-120">Select **Background** and click **Next**.</span></span>
6.  <span data-ttu-id="5071a-121">Fare clic su **Avanti** per uscire dalla procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="5071a-121">Click **Next** to finish the wizard.</span></span> <span data-ttu-id="5071a-122">Se si intende monitorare gli eventi con il plug-in, è necessario controllare l' **ascolto degli eventi** prima di completare la procedura guidata ed è necessario leggere la documentazione per l'interfaccia **IWMPEvents** per scoprire quali eventi sono supportati in Windows Media Player 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="5071a-122">If you are going to monitor events with your plug-in, you must check **Listen to events** before finishing the wizard, and you should read the documentation for the **IWMPEvents** interface to find out which events are supported on Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="5071a-123">Ora che è stato creato il codice del plug-in dell'interfaccia utente, è necessario creare un progetto di Windows CE DLL vuoto in eMbedded Visual C++ 4,0.</span><span class="sxs-lookup"><span data-stu-id="5071a-123">Now that you have created your UI plug-in code, you need to create an empty Windows CE DLL project in eMbedded Visual C++ 4.0.</span></span> <span data-ttu-id="5071a-124">Copiare quindi i file di origine generati dalla procedura guidata nel nuovo progetto in modo che vengano compilati con il compilatore ARM4.</span><span class="sxs-lookup"><span data-stu-id="5071a-124">Then copy your wizard-generated source files to that new project so that they will compile with the ARM4 compiler.</span></span>

<span data-ttu-id="5071a-125">Per creare un progetto vuoto</span><span class="sxs-lookup"><span data-stu-id="5071a-125">To create an empty project</span></span>

1.  <span data-ttu-id="5071a-126">Avviare un nuovo progetto in eMbedded Visual C++, quindi selezionare **WCE Dynamic-Link Library** dal riquadro **progetti** .</span><span class="sxs-lookup"><span data-stu-id="5071a-126">Start a new project in eMbedded Visual C++, and then select **WCE Dynamic-Link Library** from the **Projects** pane.</span></span>
2.  <span data-ttu-id="5071a-127">Assegnare un nome al progetto e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="5071a-127">Name your project and click **OK**.</span></span>
3.  <span data-ttu-id="5071a-128">Verificare che sia selezionato **un progetto di Windows CE dll vuoto** , quindi fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="5071a-128">Make sure **An empty Windows CE DLL project** is selected, and then click **Finish**.</span></span>
4.  <span data-ttu-id="5071a-129">Fare clic sulla voce di menu **progetto** .</span><span class="sxs-lookup"><span data-stu-id="5071a-129">Click the **Project** menu item.</span></span>
5.  <span data-ttu-id="5071a-130">Selezionare **Aggiungi al progetto**, quindi fare clic su **file**.</span><span class="sxs-lookup"><span data-stu-id="5071a-130">Select **Add to Project**, and then click **Files**.</span></span>
6.  <span data-ttu-id="5071a-131">Selezionare i file C++ creati con la creazione guidata plug-in, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="5071a-131">Select the C++ files you created with the plug-in wizard, and then click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5071a-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5071a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5071a-133">**Creazione di un plug-in dell'interfaccia utente per Windows Media Player 10 Mobile**</span><span class="sxs-lookup"><span data-stu-id="5071a-133">**Creating a User Interface Plug-in for Windows Media Player 10 Mobile**</span></span>](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[<span data-ttu-id="5071a-134">**Interfaccia IWMPEvents**</span><span class="sxs-lookup"><span data-stu-id="5071a-134">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




