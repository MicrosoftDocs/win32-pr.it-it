---
description: Windows Server 2008 R2 aggiunge il supporto per il riconoscimento della grafia lato server in Windows. Questo argomento descrive come riconoscere la grafia in Windows Server 2008 R2.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Riconoscimento della grafia in Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047559"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a><span data-ttu-id="f84c7-104">Riconoscimento della grafia in Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f84c7-104">Handwriting Recognition in Windows Server 2008 R2</span></span>

<span data-ttu-id="f84c7-105">Windows Server 2008 R2 supporta il riconoscimento della grafia lato server.</span><span class="sxs-lookup"><span data-stu-id="f84c7-105">Windows Server 2008 R2 supports server-side handwriting recognition.</span></span> <span data-ttu-id="f84c7-106">Il riconoscimento lato server consente a un server di riconoscere il contenuto dall'input penna nelle pagine Web.</span><span class="sxs-lookup"><span data-stu-id="f84c7-106">Server-side recognition lets a server recognize content from pen input on Web pages.</span></span> <span data-ttu-id="f84c7-107">Questa operazione è particolarmente utile quando gli utenti in una rete specificano i termini che vengono interpretati utilizzando un dizionario personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f84c7-107">This is particularly useful when users on a network will be specifying terms that are interpreted using a custom dictionary.</span></span> <span data-ttu-id="f84c7-108">Se, ad esempio, si dispone di un'applicazione medica che esegue una query su un database del server per i nomi dei pazienti, questi nomi possono essere aggiunti a un altro database a cui si fa riferimento incrociato quando si eseguono ricerche da un modulo Silverlight scritto a mano.</span><span class="sxs-lookup"><span data-stu-id="f84c7-108">For example, if you had a medical application that queried a server database for patient names, those names could be added to another database that would be cross-referenced when performing searches from a handwritten Silverlight form.</span></span>

## <a name="set-up-your-server-for-server-side-recognition"></a><span data-ttu-id="f84c7-109">Configurare il server per il riconoscimento Server-Side</span><span class="sxs-lookup"><span data-stu-id="f84c7-109">Set up your Server for Server-Side Recognition</span></span>

<span data-ttu-id="f84c7-110">Attenersi alla procedura seguente per configurare il riconoscimento lato server.</span><span class="sxs-lookup"><span data-stu-id="f84c7-110">The following steps should be followed to set up server-side recognition.</span></span>

- <span data-ttu-id="f84c7-111">Installa Servizi di riconoscimento della grafia</span><span class="sxs-lookup"><span data-stu-id="f84c7-111">Install Ink and Handwriting Services</span></span>
- <span data-ttu-id="f84c7-112">Installare il supporto per server Web (IIS) e server applicazioni</span><span class="sxs-lookup"><span data-stu-id="f84c7-112">Install Support for Web Server (IIS) and Application Server</span></span>
- <span data-ttu-id="f84c7-113">Abilitare il ruolo esperienza desktop</span><span class="sxs-lookup"><span data-stu-id="f84c7-113">Enable the Desktop Experience Role</span></span>
- <span data-ttu-id="f84c7-114">Avviare il servizio di input di Tablet PC</span><span class="sxs-lookup"><span data-stu-id="f84c7-114">Start the Tablet PC Input Service</span></span>

### <a name="install-ink-and-handwriting-services"></a><span data-ttu-id="f84c7-115">Installa Servizi di riconoscimento della grafia</span><span class="sxs-lookup"><span data-stu-id="f84c7-115">Install Ink and Handwriting Services</span></span>

<span data-ttu-id="f84c7-116">Per installare i servizi di input penna e grafia, aprire Server Manager facendo clic sull'icona Server Manager nella barra di avvio veloce.</span><span class="sxs-lookup"><span data-stu-id="f84c7-116">To install Ink and Handwriting services, open the server manager by clicking the server manager icon from the Quick Launch tray.</span></span> <span data-ttu-id="f84c7-117">Scegliere **Aggiungi funzionalità** dal menu **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="f84c7-117">From the **Features** menu, click **Add Features**.</span></span> <span data-ttu-id="f84c7-118">Assicurarsi di selezionare la casella di controllo **servizi di riconoscimento della grafia** .</span><span class="sxs-lookup"><span data-stu-id="f84c7-118">Make sure that you select the **Ink and Handwriting Services** check box.</span></span> <span data-ttu-id="f84c7-119">Nella figura seguente è illustrata la finestra di dialogo **Seleziona funzionalità** con **servizi di riconoscimento della grafia** selezionata.</span><span class="sxs-lookup"><span data-stu-id="f84c7-119">The following image shows the **Select Features** dialog box with **Ink and Handwriting Services** selected.</span></span>

<span data-ttu-id="f84c7-120">![Finestra di dialogo Seleziona funzionalità con servizi di input penna e grafia selezionati casella di controllo](images/setup-server-1-ink-and-handwriting.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-120">![Select features dialog box with ink and handwriting services check box selected](images/setup-server-1-ink-and-handwriting.png)</span></span><br/>
<span data-ttu-id="f84c7-121">*Finestra di dialogo Seleziona funzionalità con servizi di input penna e grafia selezionati casella di controllo*</span><span class="sxs-lookup"><span data-stu-id="f84c7-121">*Select features dialog box with ink and handwriting services check box selected*</span></span>

### <a name="installation-support-for-web-server-iis-and-application-server"></a><span data-ttu-id="f84c7-122">Supporto dell'installazione per server Web (IIS) e server applicazioni</span><span class="sxs-lookup"><span data-stu-id="f84c7-122">Installation Support for Web Server (IIS) and Application Server</span></span>

<span data-ttu-id="f84c7-123">Aprire Server Manager come per il primo passaggio.</span><span class="sxs-lookup"><span data-stu-id="f84c7-123">Open the server manager as you did for the first step.</span></span> <span data-ttu-id="f84c7-124">Successivamente, sarà necessario aggiungere i ruoli server Web (IIS) e server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f84c7-124">Next, you will need to add the Web Server (IIS) and Application Server roles.</span></span> <span data-ttu-id="f84c7-125">Dal menu **ruoli** fare clic su **Aggiungi ruoli**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-125">From the **Roles** menu, click **Add Roles**.</span></span> <span data-ttu-id="f84c7-126">Verrà visualizzata l'aggiunta guidata ruoli.</span><span class="sxs-lookup"><span data-stu-id="f84c7-126">The Add Roles wizard appears.</span></span> <span data-ttu-id="f84c7-127">Fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-127">Click **Next**.</span></span> <span data-ttu-id="f84c7-128">Verificare che il **server applicazioni** e il **server Web (IIS)** siano selezionati.</span><span class="sxs-lookup"><span data-stu-id="f84c7-128">Make sure **Application Server** and **Web Server (IIS)** are selected.</span></span> <span data-ttu-id="f84c7-129">Nella figura seguente è illustrata la finestra di dialogo **Selezione ruoli server** con i ruoli server **Web (IIS)** e **server applicazioni** selezionati.</span><span class="sxs-lookup"><span data-stu-id="f84c7-129">The following image shows the **Select Server Roles** dialog box with the **Web Server (IIS)** and **Application Server** roles selected.</span></span>

<span data-ttu-id="f84c7-130">![Finestra di dialogo Selezione ruoli server con i ruoli server Web (IIS) e server applicazioni selezionati](images/setup-server-2-select-server-roles.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-130">![Select server roles dialog box with web server (iis) and application server roles selected](images/setup-server-2-select-server-roles.png)</span></span><br/>
<span data-ttu-id="f84c7-131">*Finestra di dialogo Selezione ruoli server con i ruoli server Web (IIS) e server applicazioni selezionati*</span><span class="sxs-lookup"><span data-stu-id="f84c7-131">*Select server roles dialog box with web server (iis) and application server roles selected*</span></span>

<span data-ttu-id="f84c7-132">Quando si seleziona **server applicazioni**, verrà richiesto di installare ASP.NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f84c7-132">When you select **Application Server**, you will be asked to install the ASP.NET framework.</span></span> <span data-ttu-id="f84c7-133">Fare clic sul pulsante **Aggiungi funzionalità necessarie** .</span><span class="sxs-lookup"><span data-stu-id="f84c7-133">Click the **Add the Required Features** button.</span></span> <span data-ttu-id="f84c7-134">Dopo aver fatto clic su **Avanti**, verrà visualizzata una finestra di dialogo panoramica. fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-134">After you click **Next**, you will be presented with an overview dialog box; click **Next**.</span></span> <span data-ttu-id="f84c7-135">A questo punto la finestra di dialogo **Selezione servizi ruolo** dovrebbe essere disponibile.</span><span class="sxs-lookup"><span data-stu-id="f84c7-135">The **Select Role Services** dialog box should now be available.</span></span> <span data-ttu-id="f84c7-136">Verificare che il **server Web (IIS)** sia selezionato.</span><span class="sxs-lookup"><span data-stu-id="f84c7-136">Make sure that **Web Server (IIS)** is selected.</span></span> <span data-ttu-id="f84c7-137">Nella figura seguente viene illustrata la finestra di dialogo **Selezione servizi ruolo** con server Web (IIS) abilitato.</span><span class="sxs-lookup"><span data-stu-id="f84c7-137">The following image shows the **Select Role Services** dialog box with Web Server (IIS) enabled.</span></span>

<span data-ttu-id="f84c7-138">![Finestra di dialogo Selezione servizi ruolo con server Web (IIS) abilitato](images/setup-server-3-select-role-services.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-138">![Select role services dialog box with web server (iis) enabled](images/setup-server-3-select-role-services.png)</span></span><br/>
<span data-ttu-id="f84c7-139">*Finestra di dialogo Selezione servizi ruolo con server Web (IIS) abilitato*</span><span class="sxs-lookup"><span data-stu-id="f84c7-139">*Select role services dialog box with web server (iis) enabled*</span></span>

<span data-ttu-id="f84c7-140">Fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-140">Click **Next**.</span></span> <span data-ttu-id="f84c7-141">Verrà visualizzata una finestra di dialogo Panoramica; fare di nuovo clic su **Avanti** .</span><span class="sxs-lookup"><span data-stu-id="f84c7-141">An overview dialog box appears; click **Next** again.</span></span> <span data-ttu-id="f84c7-142">A questo punto verrà visualizzata una pagina che offre le opzioni per i ruoli per il server Web (IIS).</span><span class="sxs-lookup"><span data-stu-id="f84c7-142">You will now be presented with a page offering you options for roles for Web Server (IIS).</span></span> <span data-ttu-id="f84c7-143">Fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-143">Click **Next**.</span></span> <span data-ttu-id="f84c7-144">Nella pagina successiva il pulsante **Installa** diventerà attivo.</span><span class="sxs-lookup"><span data-stu-id="f84c7-144">On the next page, the **Install** button will become active.</span></span> <span data-ttu-id="f84c7-145">Fare clic su **Installa** per installare il supporto per server Web (IIS) e server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f84c7-145">Click **Install** and you will install support for Web Server (IIS) and Application Server.</span></span>

### <a name="enable-the-desktop-experience-role"></a><span data-ttu-id="f84c7-146">Abilitare il ruolo esperienza desktop</span><span class="sxs-lookup"><span data-stu-id="f84c7-146">Enable the Desktop Experience Role</span></span>

<span data-ttu-id="f84c7-147">Per abilitare l'esperienza desktop, fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione** e quindi fare clic su **Server Manager**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-147">To enable the desktop experience, click **Start**, click **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="f84c7-148">Selezionare **Aggiungi servizi** e quindi selezionare il servizio **esperienza desktop** .</span><span class="sxs-lookup"><span data-stu-id="f84c7-148">Select **Add Services** and then select the **Desktop Experience** service.</span></span> <span data-ttu-id="f84c7-149">Nella figura seguente viene illustrata la finestra di dialogo **Seleziona funzionalità** con l'elemento esperienza desktop installato.</span><span class="sxs-lookup"><span data-stu-id="f84c7-149">The following image shows the **Select Features** dialog box with the Desktop Experience item installed.</span></span>

<span data-ttu-id="f84c7-150">![Finestra di dialogo Seleziona funzionalità con servizio esperienza desktop selezionato](images/setup-server-4-desktop-experience.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-150">![Select features dialog box with desktop experience service selected](images/setup-server-4-desktop-experience.png)</span></span><br/>
<span data-ttu-id="f84c7-151">*Finestra di dialogo Seleziona funzionalità con servizio esperienza desktop selezionato*</span><span class="sxs-lookup"><span data-stu-id="f84c7-151">*Select features dialog box with desktop experience service selected*</span></span>

<span data-ttu-id="f84c7-152">Fare clic su **Avanti** per installare l'esperienza desktop.</span><span class="sxs-lookup"><span data-stu-id="f84c7-152">Click **Next** to install the Desktop Experience.</span></span>

### <a name="start-the-tablet-service"></a><span data-ttu-id="f84c7-153">Avviare il servizio Tablet</span><span class="sxs-lookup"><span data-stu-id="f84c7-153">Start the Tablet Service</span></span>

<span data-ttu-id="f84c7-154">Dopo aver installato il servizio esperienza desktop, il servizio di input di Tablet PC verrà visualizzato nel menu **Servizi** .</span><span class="sxs-lookup"><span data-stu-id="f84c7-154">After you have installed the Desktop Experience service, the Tablet PC Input service will appear in the **Services** menu.</span></span> <span data-ttu-id="f84c7-155">Per accedere al menu **Servizi** , fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione**, quindi fare clic su **Servizi**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-155">To access the **Services** menu, click **Start**, click **Administrative Tools**, and then click **Services**.</span></span> <span data-ttu-id="f84c7-156">Per avviare il servizio, fare clic con il pulsante destro del mouse su **servizio di input di Tablet PC** e quindi scegliere **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-156">To start the service, right-click **Tablet PC Input Service** and then click **Start**.</span></span> <span data-ttu-id="f84c7-157">La figura seguente mostra il menu **Servizi** con il servizio di input di Tablet PC avviato.</span><span class="sxs-lookup"><span data-stu-id="f84c7-157">The following image shows the **Services** menu with the Tablet PC Input Service started.</span></span>

<span data-ttu-id="f84c7-158">![Menu dei servizi con il servizio di input di Tablet PC avviato](images/setup-server-5-tablet-pc-input-service.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-158">![Services menu with the tablet pc input service started](images/setup-server-5-tablet-pc-input-service.png)</span></span><br/>
<span data-ttu-id="f84c7-159">*Menu dei servizi con il servizio di input di Tablet PC avviato*</span><span class="sxs-lookup"><span data-stu-id="f84c7-159">*Services menu with the tablet pc input service started*</span></span>

## <a name="performing-server-side-recognition-using-silverlight"></a><span data-ttu-id="f84c7-160">Esecuzione del riconoscimento Server-Side tramite Silverlight</span><span class="sxs-lookup"><span data-stu-id="f84c7-160">Performing Server-Side Recognition Using Silverlight</span></span>

<span data-ttu-id="f84c7-161">In questa sezione viene illustrato come creare un'applicazione Web che utilizza Silverlight per acquisire l'input della grafia.</span><span class="sxs-lookup"><span data-stu-id="f84c7-161">This section shows how to create a Web application that uses Silverlight to capture handwriting input.</span></span> <span data-ttu-id="f84c7-162">Usare la procedura seguente per programmare il riconoscimento in Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="f84c7-162">Use the following steps to program the recognizer in Visual Studio 2008.</span></span>

- <span data-ttu-id="f84c7-163">Installare e aggiornare Visual Studio 2008 per aggiungere il supporto per Silverlight.</span><span class="sxs-lookup"><span data-stu-id="f84c7-163">Install and update Visual Studio 2008 to add support for Silverlight.</span></span>
- <span data-ttu-id="f84c7-164">Creare un nuovo progetto Silverlight in Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="f84c7-164">Create a new Silverlight project in Visual Studio 2008.</span></span>
- <span data-ttu-id="f84c7-165">Aggiungere i riferimenti al servizio necessari per il progetto.</span><span class="sxs-lookup"><span data-stu-id="f84c7-165">Add the necessary service references to your project.</span></span>
- <span data-ttu-id="f84c7-166">Creare un servizio WCF Silverlight per il riconoscimento dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="f84c7-166">Create a Silverlight WCF Service for ink recognition.</span></span>
- <span data-ttu-id="f84c7-167">Aggiungere il riferimento al servizio al progetto client.</span><span class="sxs-lookup"><span data-stu-id="f84c7-167">Add the service reference to your client project.</span></span>
- <span data-ttu-id="f84c7-168">Aggiungere la classe InkCollector al progetto InkRecognition.</span><span class="sxs-lookup"><span data-stu-id="f84c7-168">Add the InkCollector class to the InkRecognition project.</span></span>
- <span data-ttu-id="f84c7-169">Rimuovere le direttive del trasporto protetto dalla configurazione client</span><span class="sxs-lookup"><span data-stu-id="f84c7-169">Remove secure transport directives from the client configuration</span></span>

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a><span data-ttu-id="f84c7-170">Installare e aggiornare Visual Studio 2008 per aggiungere il supporto per Silverlight</span><span class="sxs-lookup"><span data-stu-id="f84c7-170">Install and Update Visual Studio 2008 to Add Support for Silverlight</span></span>

<span data-ttu-id="f84c7-171">Prima di iniziare, è necessario eseguire i passaggi seguenti nel server Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="f84c7-171">Before you begin, you must perform the following steps on your Windows Server 2008 R2 server.</span></span>

- <span data-ttu-id="f84c7-172">Installare Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="f84c7-172">Install Visual Studio 2008.</span></span>
- <span data-ttu-id="f84c7-173">Installare [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).</span><span class="sxs-lookup"><span data-stu-id="f84c7-173">Install [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).</span></span>
- <span data-ttu-id="f84c7-174">Installare [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/).</span><span class="sxs-lookup"><span data-stu-id="f84c7-174">Install [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/).</span></span>

<span data-ttu-id="f84c7-175">Al termine dell'installazione di queste applicazioni e degli aggiornamenti, è possibile creare un'applicazione Web di riconoscimento lato server.</span><span class="sxs-lookup"><span data-stu-id="f84c7-175">After you have installed these applications and updates, you are ready to create your server-side recognition Web application.</span></span>

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a><span data-ttu-id="f84c7-176">Creare un nuovo progetto Web Silverlight in Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="f84c7-176">Create a new Silverlight Web Project in Visual Studio 2008</span></span>

<span data-ttu-id="f84c7-177">Scegliere **Nuovo progetto** dal menu **File**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-177">From the **File** menu, click **New Project**.</span></span> <span data-ttu-id="f84c7-178">Selezionare il modello applicazione Silverlight dall'elenco di progetti Visual C \# .</span><span class="sxs-lookup"><span data-stu-id="f84c7-178">Select the Silverlight Application template from the Visual C\# project list.</span></span> <span data-ttu-id="f84c7-179">Assegnare al progetto il nome InkRecognition e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-179">Name your project InkRecognition and click **OK**.</span></span> <span data-ttu-id="f84c7-180">La figura seguente mostra il \# progetto Silverlight C selezionato e denominato InkRecognition.</span><span class="sxs-lookup"><span data-stu-id="f84c7-180">The following image shows the C\# Silverlight project selected and named InkRecognition.</span></span>

<span data-ttu-id="f84c7-181">![\#progetto Silverlight c selezionato con il nome InkRecognition](images/project-1-new-project.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-181">![c\# silverlight project selected, with the name inkrecognition](images/project-1-new-project.png)</span></span><br/>
<span data-ttu-id="f84c7-182">*\#progetto Silverlight c selezionato con il nome InkRecognition*</span><span class="sxs-lookup"><span data-stu-id="f84c7-182">*c\# silverlight project selected, with the name inkrecognition*</span></span>

<span data-ttu-id="f84c7-183">Dopo aver fatto clic su **OK**, viene visualizzata una finestra di dialogo in cui viene richiesto di aggiungere un'applicazione Silverlight al progetto.</span><span class="sxs-lookup"><span data-stu-id="f84c7-183">After you click **OK**, a dialog box prompts you to add a Silverlight application to your project.</span></span> <span data-ttu-id="f84c7-184">Selezionare **Aggiungi un nuovo progetto Web ASP.NET alla soluzione per ospitare Silverlight** e fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-184">Select **Add a new ASP.NET Web project to the solution to host Silverlight** and click **OK**.</span></span> <span data-ttu-id="f84c7-185">Nell'immagine seguente viene illustrato come configurare il progetto di esempio prima di fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-185">The following image shows how to set up the example project before you click **OK**.</span></span>

<span data-ttu-id="f84c7-186">![Finestra di dialogo con la richiesta per l'aggiunta di un'applicazione Silverlight a un progetto](images/project-2-add-a-new-aspnetproject.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-186">![Dialog box with prompt for adding a silverlight application to a project](images/project-2-add-a-new-aspnetproject.png)</span></span><br/>
<span data-ttu-id="f84c7-187">*Finestra di dialogo con la richiesta per l'aggiunta di un'applicazione Silverlight a un progetto*</span><span class="sxs-lookup"><span data-stu-id="f84c7-187">*Dialog box with prompt for adding a silverlight application to a project*</span></span>

### <a name="add-the-necessary-service-references-to-your-project"></a><span data-ttu-id="f84c7-188">Aggiungere i riferimenti al servizio necessari al progetto</span><span class="sxs-lookup"><span data-stu-id="f84c7-188">Add the Necessary Service References to your Project</span></span>

<span data-ttu-id="f84c7-189">A questo punto è disponibile un progetto client Silverlight generico (InkRecognition) con un progetto Web (InkRecognition. Web) configurato nella soluzione.</span><span class="sxs-lookup"><span data-stu-id="f84c7-189">Now you have your generic Silverlight client project (InkRecognition) with a Web project (InkRecognition.Web) set up in your solution.</span></span> <span data-ttu-id="f84c7-190">Il progetto viene aperto con Page. XAML e default. aspx aperti.</span><span class="sxs-lookup"><span data-stu-id="f84c7-190">The project will open with Page.xaml and Default.aspx open.</span></span> <span data-ttu-id="f84c7-191">Chiudere le finestre e aggiungere i riferimenti System. Runtime. Serialization e System. ServiceModel al progetto InkRecognition facendo clic con il pulsante destro del mouse sulla cartella riferimenti nel progetto InkRecognition e scegliendo **Aggiungi riferimento**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-191">Close these windows and add the System.Runtime.Serialization and System.ServiceModel references to the InkRecognition project by right-clicking on the references folder in the InkRecognition project and selecting **Add Reference**.</span></span> <span data-ttu-id="f84c7-192">Nella figura seguente viene illustrata la finestra di dialogo con i riferimenti necessari selezionati.</span><span class="sxs-lookup"><span data-stu-id="f84c7-192">The following image shows the dialog box with the requisite references selected.</span></span>

<span data-ttu-id="f84c7-193">![Finestra di dialogo Aggiungi riferimenti con System. Runtime. Serialization e System. ServiceModel selezionati](images/project-3a-add-references-to-inkreco.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-193">![Add references dialog box with system.runtime.serialization and system.servicemodel selected](images/project-3a-add-references-to-inkreco.png)</span></span><br/>
<span data-ttu-id="f84c7-194">*Finestra di dialogo Aggiungi riferimenti con System. Runtime. Serialization e System. ServiceModel selezionati*</span><span class="sxs-lookup"><span data-stu-id="f84c7-194">*Add references dialog box with system.runtime.serialization and system.servicemodel selected*</span></span>

<span data-ttu-id="f84c7-195">Successivamente, è necessario aggiungere i riferimenti System. ServiceModel e Microsoft. Ink al progetto InkRecognition. Web.</span><span class="sxs-lookup"><span data-stu-id="f84c7-195">Next, you need to add the System.ServiceModel and Microsoft.Ink references to the InkRecognition.Web project.</span></span> <span data-ttu-id="f84c7-196">Per impostazione predefinita, il riferimento a Microsoft. Ink non verrà visualizzato nei riferimenti .NET, quindi cercare Microsoft.Ink.dll nella cartella Windows.</span><span class="sxs-lookup"><span data-stu-id="f84c7-196">The Microsoft.Ink reference will not appear in the .NET references by default, so search your Windows folder for Microsoft.Ink.dll.</span></span> <span data-ttu-id="f84c7-197">Dopo aver individuato la DLL, aggiungere l'assembly ai riferimenti del progetto: selezionare la scheda **Sfoglia** , passare alla cartella contenente Microsoft.Ink.dll, selezionare Microsoft.Ink.dll, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-197">After you have located the DLL, add the assembly to the project references: select the **Browse** tab, change to the folder containing Microsoft.Ink.dll, select Microsoft.Ink.dll, and then click **OK**.</span></span> <span data-ttu-id="f84c7-198">Nell'immagine seguente viene illustrata la soluzione del progetto in Esplora risorse con tutti gli assembly di riferimento aggiunti.</span><span class="sxs-lookup"><span data-stu-id="f84c7-198">The following image shows the project's solution in Windows Explorer with all of the reference assemblies added.</span></span>

<span data-ttu-id="f84c7-199">![progetto InkRecognition in Esplora risorse con tutti gli assembly di riferimento aggiunti](images/project-3b-with-reference-assemblies.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-199">![inkrecognition project in windows explorer with all reference assemblies added](images/project-3b-with-reference-assemblies.png)</span></span><br/>
<span data-ttu-id="f84c7-200">*progetto InkRecognition in Esplora risorse con tutti gli assembly di riferimento aggiunti*</span><span class="sxs-lookup"><span data-stu-id="f84c7-200">*inkrecognition project in windows explorer with all reference assemblies added*</span></span>

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a><span data-ttu-id="f84c7-201">Creare un servizio WCF Silverlight per il riconoscimento dell'input penna</span><span class="sxs-lookup"><span data-stu-id="f84c7-201">Create a Silverlight WCF Service for Ink Recognition</span></span>

<span data-ttu-id="f84c7-202">Successivamente, verrà aggiunto un servizio WCF per il riconoscimento dell'input penna al progetto.</span><span class="sxs-lookup"><span data-stu-id="f84c7-202">Next, you will add a WCF service for ink recognition to the project.</span></span> <span data-ttu-id="f84c7-203">Fare clic con il pulsante destro del mouse sul progetto InkRecognition. Web, scegliere **Aggiungi**, quindi fare clic su **nuovo elemento**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-203">Right-click your InkRecognition.Web project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="f84c7-204">Selezionare il modello di servizio WCF Silverlight, modificare il nome in InkRecogitionService, quindi fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-204">Select the WCF Silverlight Service template, change the name to InkRecogitionService, and then click **Add**.</span></span> <span data-ttu-id="f84c7-205">Nella figura seguente viene illustrata la finestra di dialogo **Aggiungi nuovo elemento** con il servizio WCF Silverlight selezionato e denominato.</span><span class="sxs-lookup"><span data-stu-id="f84c7-205">The following image shows the **Add New Item** dialog box with the Silverlight WCF service selected and named.</span></span>

<span data-ttu-id="f84c7-206">![Finestra di dialogo Aggiungi nuovo elemento con servizio WCF Silverlight selezionato e denominato](images/project-4-add-wcf-service.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-206">![Add new item dialog box with silverlight wcf service selected and named](images/project-4-add-wcf-service.png)</span></span><br/>
<span data-ttu-id="f84c7-207&quot;>*Finestra di dialogo Aggiungi nuovo elemento con servizio WCF Silverlight selezionato e denominato*</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f84c7-207&quot;>*Add new item dialog box with silverlight wcf service selected and named*</span></span>

<span data-ttu-id=&quot;f84c7-208&quot;>Dopo aver aggiunto il servizio WCF Silverlight, si aprirà il code-behind del servizio, InkRecognitionService. cs.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f84c7-208&quot;>After you add the WCF Silverlight service, the service code behind, InkRecognitionService.cs, will open.</span></span> <span data-ttu-id=&quot;f84c7-209&quot;>Sostituire il codice del servizio con il codice seguente.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;f84c7-209&quot;>Replace the service code with the following code.</span></span>

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = &quot;")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a><span data-ttu-id="f84c7-210">Aggiungere il riferimento al servizio al progetto client</span><span class="sxs-lookup"><span data-stu-id="f84c7-210">Add the Service Reference to your Client Project</span></span>

<span data-ttu-id="f84c7-211">Ora che è disponibile il servizio WCF Silverlight per InkRecognition, si utilizzerà il servizio dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="f84c7-211">Now that you have your Silverlight WCF service for InkRecognition, you will consume the service from your client application.</span></span> <span data-ttu-id="f84c7-212">Fare clic con il pulsante destro del mouse sul progetto InkRecognition e selezionare **Aggiungi riferimento al servizio**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-212">Right-click the InkRecognition project and select **Add Service Reference**.</span></span> <span data-ttu-id="f84c7-213">Nella finestra di dialogo **Aggiungi riferimento al servizio** visualizzata selezionare **individua** per individuare i servizi dalla soluzione corrente.</span><span class="sxs-lookup"><span data-stu-id="f84c7-213">From the **Add Service Reference** dialog box that appears, select **Discover** to discover services from the current solution.</span></span> <span data-ttu-id="f84c7-214">InkRecognitionService verrà visualizzato nel riquadro servizi.</span><span class="sxs-lookup"><span data-stu-id="f84c7-214">InkRecognitionService will appear in the Services pane.</span></span> <span data-ttu-id="f84c7-215">Fare doppio clic su InkRecognitionService nel riquadro servizi, impostare lo spazio dei nomi su InkRecognitionServiceReference e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-215">Double-click InkRecognitionService from the Services pane, change the namespace to InkRecognitionServiceReference, and then click **OK**.</span></span> <span data-ttu-id="f84c7-216">Nella figura seguente viene illustrata la finestra di dialogo **Aggiungi riferimento al servizio** con InkRecognitionService selezionato e lo spazio dei nomi modificato.</span><span class="sxs-lookup"><span data-stu-id="f84c7-216">The following image shows the **Add Service Reference** dialog box with InkRecognitionService selected and the namespace changed.</span></span>

<span data-ttu-id="f84c7-217">![Finestra di dialogo Aggiungi riferimento al servizio con inkrecognitionservice selezionato e spazio dei nomi modificato](images/project-5-discover-service-reference.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-217">![Add service reference dialog box with inkrecognitionservice selected and namespace changed](images/project-5-discover-service-reference.png)</span></span><br/>
<span data-ttu-id="f84c7-218">*Finestra di dialogo Aggiungi riferimento al servizio con inkrecognitionservice selezionato e spazio dei nomi modificato*</span><span class="sxs-lookup"><span data-stu-id="f84c7-218">*Add service reference dialog box with inkrecognitionservice selected and namespace changed*</span></span>

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a><span data-ttu-id="f84c7-219">Aggiungere la classe InkCollector al progetto InkRecognition</span><span class="sxs-lookup"><span data-stu-id="f84c7-219">Add the InkCollector Class to the InkRecognition Project</span></span>

<span data-ttu-id="f84c7-220">Fare clic con il pulsante destro del mouse sul progetto InkRecognition, scegliere **Aggiungi** e quindi fare clic su **nuovo elemento**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-220">Right-click the InkRecognition project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="f84c7-221">Dal menu **Visual C \#** Selezionare **\# classe c**.</span><span class="sxs-lookup"><span data-stu-id="f84c7-221">From the **Visual C\#** menu, select **C\# class**.</span></span> <span data-ttu-id="f84c7-222">Denominare la classe InkCollector.</span><span class="sxs-lookup"><span data-stu-id="f84c7-222">Name the class InkCollector.</span></span> <span data-ttu-id="f84c7-223">Nella figura seguente viene illustrata la finestra di dialogo con la \# classe C selezionata e denominata.</span><span class="sxs-lookup"><span data-stu-id="f84c7-223">The following image shows the dialog box with the C\# class selected and named.</span></span>

<span data-ttu-id="f84c7-224">![Finestra di dialogo Aggiungi nuovo elemento con \# classe c selezionata e denominata](images/project-6-add-ink-collector.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-224">![Add new item dialog box with c\# class selected and named](images/project-6-add-ink-collector.png)</span></span><br/>
<span data-ttu-id="f84c7-225">*Finestra di dialogo Aggiungi nuovo elemento con \# classe c selezionata e denominata*</span><span class="sxs-lookup"><span data-stu-id="f84c7-225">*Add new item dialog box with c\# class selected and named*</span></span>

<span data-ttu-id="f84c7-226">Dopo aver aggiunto la classe InkCollector, viene aperta la definizione della classe.</span><span class="sxs-lookup"><span data-stu-id="f84c7-226">After you add the InkCollector class, the class definition will open.</span></span> <span data-ttu-id="f84c7-227">Sostituire il codice nell'agente di raccolta input penna con il codice seguente.</span><span class="sxs-lookup"><span data-stu-id="f84c7-227">Replace the code in the Ink Collector with the following code.</span></span>

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a><span data-ttu-id="f84c7-228">Aggiornare XAML per la pagina predefinita e aggiungere un code-behind per il riconoscimento della grafia</span><span class="sxs-lookup"><span data-stu-id="f84c7-228">Update the XAML for the Default Page and Add a Code Behind for Handwriting Recognition</span></span>

<span data-ttu-id="f84c7-229">Ora che è disponibile una classe che raccoglie l'input penna, sarà necessario aggiornare il codice XAML in page. XAML con il codice XAML seguente.</span><span class="sxs-lookup"><span data-stu-id="f84c7-229">Now that you have a class that collects ink, you will need to update the XAML in page.xaml with the following XAML.</span></span> <span data-ttu-id="f84c7-230">Il codice seguente aggiunge una sfumatura gialla all'area di input, un controllo InkCanvas e un pulsante che attiverà il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="f84c7-230">The following code adds a yellow gradient to the input area, an InkCanvas control, and a button that will trigger recognition.</span></span>

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

<span data-ttu-id="f84c7-231">Sostituire la pagina code-behind, Page. XAML. cs, con il codice seguente che aggiungerà un gestore dell'evento per il pulsante **Recognize** .</span><span class="sxs-lookup"><span data-stu-id="f84c7-231">Replace the code behind page, Page.xaml.cs, with the following code that will add an event handler for the **Recognize** button.</span></span>

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a><span data-ttu-id="f84c7-232">Rimuovere le direttive del trasporto protetto dalla configurazione client</span><span class="sxs-lookup"><span data-stu-id="f84c7-232">Remove Secure Transport Directives from the Client Configuration</span></span>

<span data-ttu-id="f84c7-233">Prima di poter utilizzare il servizio WCF, è necessario rimuovere tutte le opzioni di trasporto protette dalla configurazione del servizio perché i trasporti protetti non sono attualmente supportati nei servizi WCF di Silverlight 2,0.</span><span class="sxs-lookup"><span data-stu-id="f84c7-233">Before you can consume the WCF service, you must remove all secure transport options from the service configuration because secure transports are not currently supported in Silverlight 2.0 WCF services.</span></span> <span data-ttu-id="f84c7-234">Dal progetto InkRecognition aggiornare le impostazioni di sicurezza in ServiceReferences. ClientConfig.</span><span class="sxs-lookup"><span data-stu-id="f84c7-234">From the InkRecognition project, update the security settings in ServiceReferences.ClientConfig.</span></span> <span data-ttu-id="f84c7-235">Modificare il codice XML di sicurezza da</span><span class="sxs-lookup"><span data-stu-id="f84c7-235">Change the security XML from</span></span>

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

<span data-ttu-id="f84c7-236">in</span><span class="sxs-lookup"><span data-stu-id="f84c7-236">to</span></span>

```XML
       <security mode="None"/>
```

<span data-ttu-id="f84c7-237">A questo punto, l'applicazione deve essere eseguita.</span><span class="sxs-lookup"><span data-stu-id="f84c7-237">Now, your application should run.</span></span> <span data-ttu-id="f84c7-238">Nell'immagine seguente viene illustrato il modo in cui l'applicazione esamina awebpagewith parte della grafia immessa nella casella di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="f84c7-238">The following image shows how the application looks within awebpagewith some handwriting entered into the recognition box.</span></span>

<span data-ttu-id="f84c7-239">![Applicazione all'interno di awebpagewith di una grafia immessa nella casella di riconoscimento](images/demo-1.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-239">![Application within awebpagewith some handwriting entered into recognition box](images/demo-1.png)</span></span><br/>
<span data-ttu-id="f84c7-240">*Applicazione all'interno di awebpagewith di una grafia immessa nella casella di riconoscimento*</span><span class="sxs-lookup"><span data-stu-id="f84c7-240">*Application within awebpagewith some handwriting entered into recognition box*</span></span>

<span data-ttu-id="f84c7-241">Nell'immagine seguente viene illustrato il testo riconosciuto nell'elenco a discesa **risultato** .</span><span class="sxs-lookup"><span data-stu-id="f84c7-241">The following image shows the recognized text in the **Result** drop-down list.</span></span>

<span data-ttu-id="f84c7-242">![Applicazione all'interno del testo riconosciuto awebpagewith nell'elenco a discesa risultato](images/demo-2.png)</span><span class="sxs-lookup"><span data-stu-id="f84c7-242">![Application within awebpagewith recognized text in result drop-down list](images/demo-2.png)</span></span><br/>
<span data-ttu-id="f84c7-243">*Applicazione all'interno del testo riconosciuto awebpagewith nell'elenco a discesa risultato*</span><span class="sxs-lookup"><span data-stu-id="f84c7-243">*Application within awebpagewith recognized text in result drop-down list*</span></span>

 

 



