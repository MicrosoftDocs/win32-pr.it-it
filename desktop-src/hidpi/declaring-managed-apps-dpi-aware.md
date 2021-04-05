---
title: Sviluppo di un'applicazione WPF sensibile ai valori DPI del monitor
description: Nota Questa pagina illustra lo sviluppo WPF legacy per Windows 8.1. Per lo sviluppo di applicazioni WPF per Windows 10, vedere la documentazione più recente su GitHub..
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Interfaccia utente di Windows, applicazioni compatibili con DPI
- Interfaccia utente di Windows, DPI superiore
- Applicazioni compatibili con DPI
- DPI alto
- scrittura di applicazioni Win32 compatibili con DPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a32bfaf76271e61d0dc3791d5aaae9609be6d8c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117750"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a><span data-ttu-id="105d2-110">Sviluppo di un'applicazione WPF sensibile ai valori DPI del monitor</span><span class="sxs-lookup"><span data-stu-id="105d2-110">Developing a Per-Monitor DPI-Aware WPF Application</span></span>

<span data-ttu-id="105d2-111">**API importanti**</span><span class="sxs-lookup"><span data-stu-id="105d2-111">**Important APIs**</span></span>

-   [<span data-ttu-id="105d2-112">**SetProcessDpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="105d2-112">**SetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [<span data-ttu-id="105d2-113">**GetProcessDpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="105d2-113">**GetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [<span data-ttu-id="105d2-114">**GetDpiForMonitor**</span><span class="sxs-lookup"><span data-stu-id="105d2-114">**GetDpiForMonitor**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> <span data-ttu-id="105d2-115">**Questa pagina illustra lo sviluppo WPF legacy per Windows 8.1.**</span><span class="sxs-lookup"><span data-stu-id="105d2-115">**This page covers legacy WPF development for Windows 8.1.**</span></span> <span data-ttu-id="105d2-116">Per lo sviluppo di applicazioni WPF per Windows 10, vedere la <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">documentazione più recente su GitHub.</a></span><span class="sxs-lookup"><span data-stu-id="105d2-116">If you are developing WPF applications for Windows 10, please see the <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">latest documentation on GitHub.</a></span></span>

 

<span data-ttu-id="105d2-117">Windows 8.1 offre agli sviluppatori nuove funzionalità per la creazione di applicazioni desktop con compatibilità DPI per monitor.</span><span class="sxs-lookup"><span data-stu-id="105d2-117">Windows 8.1 gives developers new functionality to create desktop applications that are per-monitor DPI-aware.</span></span> <span data-ttu-id="105d2-118">Per sfruttare i vantaggi di questa funzionalità, un'applicazione con riconoscimento DPI per monitor deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="105d2-118">In order to take advantage of this functionality, a per monitor DPI-aware application must do the following:</span></span>

-   <span data-ttu-id="105d2-119">Modificare le dimensioni della finestra per mantenere una dimensione fisica che risulti coerente in qualsiasi visualizzazione</span><span class="sxs-lookup"><span data-stu-id="105d2-119">Change window dimensions to maintain a physical size that appears consistent on any display</span></span>
-   <span data-ttu-id="105d2-120">Ricreare il layout e rieseguire il rendering della grafica per le nuove dimensioni della finestra</span><span class="sxs-lookup"><span data-stu-id="105d2-120">Re-layout and re-render graphics for the new window size</span></span>
-   <span data-ttu-id="105d2-121">Selezione dei tipi di carattere ridimensionati in modo appropriato per il livello DPI</span><span class="sxs-lookup"><span data-stu-id="105d2-121">Select fonts that are scaled appropriately for the DPI level</span></span>
-   <span data-ttu-id="105d2-122">Selezionare e caricare asset bitmap personalizzati per il livello DPI</span><span class="sxs-lookup"><span data-stu-id="105d2-122">Select and load bitmap assets that are tailored for the DPI level</span></span>

<span data-ttu-id="105d2-123">Per semplificare la creazione di un'applicazione compatibile con DPI per il monitoraggio, Windows 8.1 fornisce le seguenti Win32APIs Microsoft:</span><span class="sxs-lookup"><span data-stu-id="105d2-123">To facilitate making a per-monitor DPI-aware application, Windows 8.1 provides the following Microsoft Win32APIs:</span></span>

-   <span data-ttu-id="105d2-124">[**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (o voce del manifesto dpi) imposta il processo su un livello di riconoscimento dpi specificato, che quindi determina il modo in cui Windows ridimensiona l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="105d2-124">[**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (or DPI manifest entry) sets the process to a specified DPI awareness level, which then determines how Windows scales the UI.</span></span> <span data-ttu-id="105d2-125">Questa operazione sostituisce [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span><span class="sxs-lookup"><span data-stu-id="105d2-125">This supersedes [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span></span>
-   <span data-ttu-id="105d2-126">[**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) restituisce il livello di riconoscimento dpi.</span><span class="sxs-lookup"><span data-stu-id="105d2-126">[**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) returns the DPI awareness level.</span></span> <span data-ttu-id="105d2-127">Questa operazione sostituisce [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).</span><span class="sxs-lookup"><span data-stu-id="105d2-127">This supersedes [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).</span></span>
-   <span data-ttu-id="105d2-128">[**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) restituisce il valore dpi per un monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="105d2-128">[**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) returns the DPI for a monitor.</span></span>
-   <span data-ttu-id="105d2-129">La notifica della finestra [**WM \_ DPICHANGED**](wm-dpichanged.md) viene inviata a applicazioni compatibili con DPI per monitor quando la posizione di una finestra viene modificata in modo che la maggior parte dell'area interseca un monitor con un valore DPI diverso da dpi prima della modifica della posizione o quando l'utente sposta il dispositivo di scorrimento della visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="105d2-129">The [**WM\_DPICHANGED**](wm-dpichanged.md) window notification is sent to per-monitor DPI-aware applications when a window’s position changes such that most of its area intersects a monitor with a DPI that is different from the DPI before the position change or when the user moves the display slider.</span></span> <span data-ttu-id="105d2-130">Per creare un'applicazione che esegue il ridimensionamento e il nuovo rendering quando un utente lo sposta in una visualizzazione diversa, usare questa notifica.</span><span class="sxs-lookup"><span data-stu-id="105d2-130">To create an application that resizes and re-renders itself when a user moves it to a different display, use this notification.</span></span>

<span data-ttu-id="105d2-131">Per ulteriori informazioni sui vari livelli di riconoscimento DPI supportati per le applicazioni desktop in Windows 8.1 vedere l'argomento relativo alla [scrittura di applicazioni desktop e Win32 DPI-Aware](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="105d2-131">For more details on various DPI awareness levels supported for desktop applications in Windows 8.1 see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

## <a name="dpi-scaling-and-wpf"></a><span data-ttu-id="105d2-132">Ridimensionamento DPI e WPF</span><span class="sxs-lookup"><span data-stu-id="105d2-132">DPI Scaling and WPF</span></span>

<span data-ttu-id="105d2-133">Per impostazione predefinita, le applicazioni Windows Presentation Foundation (WPF) sono compatibili con DPI di sistema.</span><span class="sxs-lookup"><span data-stu-id="105d2-133">Windows Presentation Foundation (WPF) applications are by default system DPI-aware.</span></span> <span data-ttu-id="105d2-134">Per le definizioni dei diversi livelli di riconoscimento DPI, vedere l'argomento relativo alla [scrittura DPI-Aware applicazioni desktop e Win32](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="105d2-134">For definitions of the different DPI awareness levels see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span> <span data-ttu-id="105d2-135">Il sistema grafico WPF USA unità indipendenti dal dispositivo per abilitare la risoluzione e l'indipendenza del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="105d2-135">The WPF graphics system uses device-independent units to enable resolution and device independence.</span></span> <span data-ttu-id="105d2-136">WPF ridimensiona ogni Device Independent Pixel automaticamente in base al valore DPI corrente del sistema.</span><span class="sxs-lookup"><span data-stu-id="105d2-136">WPF scales each device independent pixel automatically based on current system DPI.</span></span> <span data-ttu-id="105d2-137">Questo consente la scalabilità automatica delle applicazioni WPF quando il DPI del monitoraggio su cui si trova la finestra è lo stesso valore DPI del sistema.</span><span class="sxs-lookup"><span data-stu-id="105d2-137">This allows WPF applications to scale automatically when the DPI of the monitor the window is on is same system DPI.</span></span> <span data-ttu-id="105d2-138">Tuttavia, poiché le applicazioni WPF sono compatibili con i dpi di sistema, l'applicazione verrà ridimensionata dal sistema operativo quando l'applicazione viene spostata in un monitor con un valore DPI diverso o quando il dispositivo di scorrimento nel pannello di controllo viene usato per modificare il valore DPI.</span><span class="sxs-lookup"><span data-stu-id="105d2-138">However, since WPF applications are system dpi-aware, the application will be scaled by the OS when the application is moved to a monitor with a different DPI or when the slider in the control panel is used to change the DPI.</span></span> <span data-ttu-id="105d2-139">Il ridimensionamento del sistema operativo può comportare la visualizzazione sfocatura delle applicazioni WPF, soprattutto quando il ridimensionamento non è integrale.</span><span class="sxs-lookup"><span data-stu-id="105d2-139">Scaling in the OS may result in WPF applications to appear blurry especially when the scaling is non-integral.</span></span> <span data-ttu-id="105d2-140">Per evitare il ridimensionamento di applicazioni WPF, è necessario aggiornarle in modo che siano compatibili con i valori DPI per monitor.</span><span class="sxs-lookup"><span data-stu-id="105d2-140">In order to avoid scaling WPF applications, they need to be updated to be per-monitor DPI-aware.</span></span>

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a><span data-ttu-id="105d2-141">Procedura dettagliata per l'esempio WPF compatibile con monitoraggio</span><span class="sxs-lookup"><span data-stu-id="105d2-141">Per Monitor Aware WPF Sample Walkthrough</span></span>

<span data-ttu-id="105d2-142">L' [esempio WPF per monitoraggio](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) con rilevamento è un'applicazione WPF di esempio aggiornata per essere compatibile con i valori dpi per monitor.</span><span class="sxs-lookup"><span data-stu-id="105d2-142">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) is a sample WPF application updated to be per-monitor DPI-aware.</span></span> <span data-ttu-id="105d2-143">L'esempio è costituito da due progetti:</span><span class="sxs-lookup"><span data-stu-id="105d2-143">The sample consists of two projects:</span></span>

-   <span data-ttu-id="105d2-144">NativeHelpers. vcxproj: si tratta di un progetto Helper nativo che implementa la funzionalità di base per fare in modo che un'applicazione WPF sia compatibile con DPI per il monitoraggio usando il Win32APIs precedente.</span><span class="sxs-lookup"><span data-stu-id="105d2-144">NativeHelpers.vcxproj: This is a native helper project that implements the core functionality to make a WPF application as per-monitor DPI-aware utilizing the Win32APIs above.</span></span> <span data-ttu-id="105d2-145">Il progetto contiene due classi:</span><span class="sxs-lookup"><span data-stu-id="105d2-145">The project contains two classes:</span></span>
    -   <span data-ttu-id="105d2-146">PerMonDPIHelpers: classe che fornisce funzioni di supporto per le operazioni correlate a DPI come il recupero del valore DPI corrente del monitoraggio attivo, l'impostazione di un processo in modo che sia compatibile con DPI per il monitoraggio e così via.</span><span class="sxs-lookup"><span data-stu-id="105d2-146">PerMonDPIHelpers: A class that provides helper functions for DPI related operations like retrieving the current DPI of the active monitor, setting a process to be per-monitor DPI-aware, etc.</span></span>
    -   <span data-ttu-id="105d2-147">PerMonitorDPIWindow: classe di base derivata da **System. Windows. Window** che implementa la funzionalità per fare in modo che una finestra dell'applicazione WPF sia compatibile con DPI per il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="105d2-147">PerMonitorDPIWindow: A base class derived from **System.Windows.Window** that implements functionality to make a WPF application window to be per-monitor dpi-aware.</span></span> <span data-ttu-id="105d2-148">Regola le dimensioni della finestra, le dimensioni del rendering della grafica e le dimensioni del carattere in base al valore DPI del monitoraggio anziché al valore DPI del sistema.</span><span class="sxs-lookup"><span data-stu-id="105d2-148">Adjusts window size, graphics rendering size and font size based on the DPI of the monitor rather than the system DPI.</span></span>
-   <span data-ttu-id="105d2-149">WPFApplication. csproj: applicazione WPF di esempio che usa PerMonitorDPIWindow (PerMonitorDPIWindow) e Mostra come la finestra dell'applicazione e il rendering vengono ridimensionati quando la finestra viene spostata in un monitor con un valore DPI diverso o quando il dispositivo di scorrimento nel pannello di controllo dello schermo viene usato per modificare il valore DPI.</span><span class="sxs-lookup"><span data-stu-id="105d2-149">WPFApplication.csproj: Sample WPF application that consumes the PerMonitorDPIWindow (PerMonitorDPIWindow), and showcases how the application window and rendering resizes when the window is moved to a monitor with a different DPI or when the slider in the Display control panel is used to change the DPI.</span></span>

<span data-ttu-id="105d2-150">Per eseguire l'esempio, attenersi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="105d2-150">To run the sample follow the steps below:</span></span>

1.  <span data-ttu-id="105d2-151">Scaricare e decomprimere l' [esempio WPF per monitoraggio](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) con rilevamento</span><span class="sxs-lookup"><span data-stu-id="105d2-151">Download and unzip the [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)</span></span>
2.  <span data-ttu-id="105d2-152">Avviare Microsoft Visual Studio e selezionare **File > apri > progetto/soluzione**</span><span class="sxs-lookup"><span data-stu-id="105d2-152">Start Microsoft Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="105d2-153">Passare alla directory che contiene l'esempio decompresso.</span><span class="sxs-lookup"><span data-stu-id="105d2-153">Browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="105d2-154">Passare alla directory denominata per l'esempio e fare doppio clic sul file della soluzione Visual Studio (. sln).</span><span class="sxs-lookup"><span data-stu-id="105d2-154">Go to the directory named for the sample, and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="105d2-155">Premere F7 o utilizzare **compila > Compila soluzione** per compilare l'esempio</span><span class="sxs-lookup"><span data-stu-id="105d2-155">Press F7 or use **Build > Build Solution** to build the sample</span></span>
5.  <span data-ttu-id="105d2-156">Premere CTRL + F5 o utilizzare **debug > avvia senza eseguire debug** per eseguire l'esempio</span><span class="sxs-lookup"><span data-stu-id="105d2-156">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="105d2-157">Per vedere l'effetto della modifica del valore DPI in un'applicazione WPF aggiornata in modo da essere compatibile con DPI per il monitoraggio utilizzando la classe di base nell'esempio, spostare la finestra dell'applicazione da e verso le visualizzazioni con DPI diversi.</span><span class="sxs-lookup"><span data-stu-id="105d2-157">To see the impact of changing DPI on a WPF application that is updated to be per-monitor DPI-aware using the base class in the sample, move the application window to and from displays that have different DPIs.</span></span> <span data-ttu-id="105d2-158">Quando la finestra viene spostata tra i monitoraggi, le dimensioni della finestra e la scalabilità dell'interfaccia utente vengono aggiornate in base al valore DPI della visualizzazione utilizzando il sistema grafico scalabile di WPF, anziché essere ridimensionato dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="105d2-158">As the window is moved between monitors, the window size and the UI scale is updated based on the DPI of the display by using WPF’s scalable graphics system, rather than being scaled by the OS.</span></span> <span data-ttu-id="105d2-159">L'interfaccia utente dell'applicazione viene sottoposta a rendering in modo nativo e non appare sfocata.</span><span class="sxs-lookup"><span data-stu-id="105d2-159">The application’s UI is rendered natively and does not appear blurry.</span></span> <span data-ttu-id="105d2-160">Se non sono presenti due schermi con DPI diversi, modificare il valore DPI cambiando il dispositivo di scorrimento nel pannello di controllo dello schermo.</span><span class="sxs-lookup"><span data-stu-id="105d2-160">If you don’t have two displays with different DPI, change the DPI by changing the slider in the Display control panel.</span></span> <span data-ttu-id="105d2-161">Se si modifica il dispositivo di scorrimento e si fa clic su **applica** , la finestra dell'applicazione verrà ridimensionata e verrà aggiornata automaticamente.</span><span class="sxs-lookup"><span data-stu-id="105d2-161">Changing the slider and clicking **Apply** will resize the application’s window and update the UI scale automatically.</span></span>

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a><span data-ttu-id="105d2-162">Aggiornamento di un'applicazione WPF esistente in modo che sia in grado di riconoscere DPI per monitoraggio usando un progetto Helper nell'esempio WPF</span><span class="sxs-lookup"><span data-stu-id="105d2-162">Updating an existing WPF Application to be per-monitor dpi-aware using helper project in the WPF Sample</span></span>

<span data-ttu-id="105d2-163">Se si dispone di un'applicazione WPF esistente e si desidera utilizzare il progetto Helper DPI dall'esempio per renderla compatibile con DPI, attenersi alla seguente procedura.</span><span class="sxs-lookup"><span data-stu-id="105d2-163">If you have an existing WPF application and wish to leverage the DPI helper project from the sample to make it DPI aware, follow these steps.</span></span>

1.  <span data-ttu-id="105d2-164">Scaricare e decomprimere l'esempio WPF per monitoraggio con rilevamento</span><span class="sxs-lookup"><span data-stu-id="105d2-164">Download and unzip the Per Monitor Aware WPF sample</span></span>
2.  <span data-ttu-id="105d2-165">Avviare Visual Studio e selezionare **File > aprire > progetto/soluzione**</span><span class="sxs-lookup"><span data-stu-id="105d2-165">Start Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="105d2-166">Passare alla directory che contiene un'applicazione WPF esistente e fare doppio clic sul file della soluzione Visual Studio (. sln).</span><span class="sxs-lookup"><span data-stu-id="105d2-166">Browse to the directory which contains an existing WPF application and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="105d2-167">Fare clic con il pulsante destro del mouse su **soluzione > aggiungi > progetto esistente** ![ una schermata che illustra la selezione del menu Aggiungi: progetto esistente](images/scrvs-image1.png)</span><span class="sxs-lookup"><span data-stu-id="105d2-167">Right click on **Solution > Add > Existing Project**![a screenshot that illustrates the add: existing project menu selection](images/scrvs-image1.png)</span></span>
5.  <span data-ttu-id="105d2-168">Nella finestra di dialogo selezione file passare alla directory che contiene l'esempio decompresso.</span><span class="sxs-lookup"><span data-stu-id="105d2-168">In the file selection dialogue browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="105d2-169">Aprire la directory denominata per l'esempio, passare alla cartella "NativeHelpers", selezionare il file di progetto Visual C++ "NativeHelpers. vcxproj" e fare clic su **OK** .</span><span class="sxs-lookup"><span data-stu-id="105d2-169">Open to the directory named for the sample, browse to the folder "NativeHelpers", select the Visual C++ project file "NativeHelpers.vcxproj” and click **OK**</span></span>
6.  <span data-ttu-id="105d2-170">Fare clic con il pulsante destro del mouse sul progetto NativeHelpers e selezionare **Compila**.</span><span class="sxs-lookup"><span data-stu-id="105d2-170">Right click on the project NativeHelpers and select **Build**.</span></span> <span data-ttu-id="105d2-171">Questa operazione genererà NativeHelpers.dll che verrà aggiunta come riferimento all'applicazione WPF nel passaggio successivo ![ una schermata che illustra la selezione del menu Compila](images/scrvs-image2.png)</span><span class="sxs-lookup"><span data-stu-id="105d2-171">This will generate NativeHelpers.dll that will be added as a reference to the WPF Application in the next step![a screen shot illustrating the build menu selection](images/scrvs-image2.png)</span></span>
7.  <span data-ttu-id="105d2-172">Aggiungere un riferimento a NativeHelpers.dll dall'applicazione WPF.</span><span class="sxs-lookup"><span data-stu-id="105d2-172">Add a reference to NativeHelpers.dll from your WPF Application.</span></span> <span data-ttu-id="105d2-173">Espandere il progetto di applicazione WPF, fare clic con il pulsante destro del mouse su **riferimenti** e scegliere **Aggiungi riferimento.**</span><span class="sxs-lookup"><span data-stu-id="105d2-173">Expand your WPF application project, right click on **References** and click on **Add Reference...**</span></span>
8.  <span data-ttu-id="105d2-174">Nella finestra di dialogo risultante espandere la sezione **soluzione** .</span><span class="sxs-lookup"><span data-stu-id="105d2-174">In the resulting dialogue, expand the **Solution** section.</span></span> <span data-ttu-id="105d2-175">In **progetti**, selezionare NativeHelpers e fare clic su **OK** per ![ scattare una schermata che illustra la finestra di dialogo Resource Manager](images/scrvs-image3.png)</span><span class="sxs-lookup"><span data-stu-id="105d2-175">Under **Projects**, select NativeHelpers, and click **OK**![a screen shot illustrating the resource manager dialog](images/scrvs-image3.png)</span></span>
9.  <span data-ttu-id="105d2-176">Espandere il progetto di applicazione WPF, espandere **Proprietà** e aprire **AssemblyInfo. cs**.</span><span class="sxs-lookup"><span data-stu-id="105d2-176">Expand your WPF application project, expand **Properties**, and open **AssemblyInfo.cs**.</span></span> <span data-ttu-id="105d2-177">Apportare le aggiunte seguenti a AssemblyInfo. cs</span><span class="sxs-lookup"><span data-stu-id="105d2-177">Make the following additions to AssemblyInfo.cs</span></span>
    -   <span data-ttu-id="105d2-178">Aggiungere un riferimento a System. Windows. Media nella sezione di riferimento (mediante System. Windows. Media;)</span><span class="sxs-lookup"><span data-stu-id="105d2-178">Add reference to System.Windows.Media in the reference section (using System.Windows.Media;)</span></span>
    -   <span data-ttu-id="105d2-179">Aggiungere l'attributo DisableDpiAwareness ( `[assembly: DisableDpiAwareness]` )</span><span class="sxs-lookup"><span data-stu-id="105d2-179">Add the DisableDpiAwareness attribute (`[assembly: DisableDpiAwareness]`)</span></span>

    ![screenshot che illustra le proprietà aggiuntive](images/scrvs-image4.png)
10. <span data-ttu-id="105d2-181">Ereditare la classe principale della finestra WPF dalla classe base PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="105d2-181">Inherit the main WPF window class from PerMonitorDPIWindow base class</span></span>
    -   <span data-ttu-id="105d2-182">Aggiornare il file con estensione CS della finestra principale di WPF per ereditare dalla classe di base PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="105d2-182">Update the .cs file of the main WPF window to inherit from the PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="105d2-183">Aggiungere un riferimento a NativeHelpers nella sezione di riferimento aggiungendo la riga `using NativeHelpers;`</span><span class="sxs-lookup"><span data-stu-id="105d2-183">Add a reference to NativeHelpers in the reference section by adding the line `using NativeHelpers;`</span></span>
        -   <span data-ttu-id="105d2-184">Ereditare la classe della finestra principale dalla classe PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="105d2-184">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![screenshot che illustra il riferimento c++](images/scrvs-image5.png)
    -   <span data-ttu-id="105d2-186">Aggiornare il file con estensione XAML della finestra principale di WPF per ereditare dalla classe di base PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="105d2-186">Update the .xaml file of the main WPF window to inherit from PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="105d2-187">Aggiungere un riferimento a NativeHelpers nella sezione di riferimento aggiungendo la riga `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span><span class="sxs-lookup"><span data-stu-id="105d2-187">Add a reference to NativeHelpers in the reference section by adding the line `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span></span>
        -   <span data-ttu-id="105d2-188">Ereditare la classe della finestra principale dalla classe PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="105d2-188">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![screenshot che illustra l'aggiunta del riferimento. XAML](images/scrvs-image6.png)
11. <span data-ttu-id="105d2-190">Premere F7 o utilizzare **compila > Compila soluzione** per compilare l'esempio</span><span class="sxs-lookup"><span data-stu-id="105d2-190">Press F7 or use **Build > Build Solution** to build the sample</span></span>
12. <span data-ttu-id="105d2-191">Premere CTRL + F5 o utilizzare **debug > avvia senza eseguire debug** per eseguire l'esempio</span><span class="sxs-lookup"><span data-stu-id="105d2-191">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="105d2-192">L'applicazione di [esempio WPF compatibile con monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) illustra come un'applicazione WPF può essere aggiornata in modo che sia compatibile con DPI per il monitoraggio rispondendo alla notifica della finestra [**\_ DPICHANGED di WM**](wm-dpichanged.md) .</span><span class="sxs-lookup"><span data-stu-id="105d2-192">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) application illustrates how a WPF application can be updated to be per-monitor DPI-aware by responding to the [**WM\_DPICHANGED**](wm-dpichanged.md) window notification.</span></span> <span data-ttu-id="105d2-193">In risposta alla notifica della finestra, l'esempio aggiorna la trasformazione di scala utilizzata da WPF in base al valore DPI corrente del monitoraggio su cui si trova la finestra.</span><span class="sxs-lookup"><span data-stu-id="105d2-193">In response to the window notification, the sample updates the scale transform used by WPF based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="105d2-194">Il *wParam* della notifica della finestra contiene il nuovo valore dpi in *wParam*.</span><span class="sxs-lookup"><span data-stu-id="105d2-194">The *wParam* of the window notification contains the new DPI in the *wParam*.</span></span> <span data-ttu-id="105d2-195">*LParam* contiene un rettangolo con le dimensioni e la posizione della nuova finestra suggerita, ridimensionata per il nuovo valore dpi.</span><span class="sxs-lookup"><span data-stu-id="105d2-195">The *lParam* contains a rectangle that has the size and position of the new suggested window, scaled for the new DPI.</span></span>

<span data-ttu-id="105d2-196">Nota:</span><span class="sxs-lookup"><span data-stu-id="105d2-196">Note:</span></span>

> [!Note]  
> <span data-ttu-id="105d2-197">Poiché questo esempio sovrascrive le dimensioni della finestra e la trasformazione di ridimensionamento del nodo radice della finestra WPF, è possibile che lo sviluppatore di applicazioni possa richiedere ulteriore lavoro se:</span><span class="sxs-lookup"><span data-stu-id="105d2-197">Since this sample overwrites the window size and the scale transform of the root node of the WPF window, further work may be required by application developer if:</span></span>
>
> -   <span data-ttu-id="105d2-198">Le dimensioni della finestra influiscano su altre parti dell'applicazione come questa finestra WPF ospitata all'interno di un'altra applicazione.</span><span class="sxs-lookup"><span data-stu-id="105d2-198">The size of the window impacts other portions of the application like this WPF Window being hosted inside another application.</span></span>
> -   <span data-ttu-id="105d2-199">L'applicazione WPF che estende questa classe sta impostando altre trasformazioni sull'oggetto visivo radice. Nell'esempio è possibile sovrascrivere un'altra trasformazione applicata dall'applicazione WPF stessa.</span><span class="sxs-lookup"><span data-stu-id="105d2-199">The WPF application that is extending this class is setting some other transform on the root visual; the sample may overwrite some other transform that is being applied by the WPF application itself.</span></span>

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a><span data-ttu-id="105d2-200">Cenni preliminari sul progetto Helper nell'esempio WPF</span><span class="sxs-lookup"><span data-stu-id="105d2-200">Overview of the helper project in the WPF sample</span></span>

<span data-ttu-id="105d2-201">Per rendere un'applicazione WPF esistente compatibile con DPI per il monitoraggio, la libreria NativeHelpers offre le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="105d2-201">In order to make an existing WPF application per-monitor DPI-aware the NativeHelpers library provides following functionality:</span></span>

-   <span data-ttu-id="105d2-202">**Contrassegna l'applicazione WPF come compatibile con DPI per ponitor:** L'applicazione WPF è contrassegnata come compatibile con DPI per monitoraggio chiamando [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) per il processo corrente.</span><span class="sxs-lookup"><span data-stu-id="105d2-202">**Marks the WPF application as per-ponitor DPI-aware:** The WPF application is marked as per-monitor DPI-aware by calling [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) for the current process.</span></span> <span data-ttu-id="105d2-203">Contrassegnare l'applicazione come compatibile con DPI per il monitoraggio garantisce che</span><span class="sxs-lookup"><span data-stu-id="105d2-203">Marking the application as per-monitor DPI-aware will ensure that</span></span>

    -   <span data-ttu-id="105d2-204">Il sistema operativo non ridimensiona l'applicazione quando il valore DPI del sistema non corrisponde al valore DPI corrente del monitoraggio in cui si trova la finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="105d2-204">The OS does not scale the application when the system DPI does not match the current DPI of the monitor the application window is on</span></span>
    -   <span data-ttu-id="105d2-205">Il messaggio [**WM \_ DPICHANGED**](wm-dpichanged.md) viene inviato ogni volta che viene modificato il valore dpi della finestra</span><span class="sxs-lookup"><span data-stu-id="105d2-205">The [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent whenever the DPI of the window changes</span></span>

-   <span data-ttu-id="105d2-206">Consente **di regolare la dimensione della finestra, di ricreare il layout e di eseguire nuovamente il rendering del contenuto grafico e di selezionare i tipi di carattere basati sul valore dpi iniziale del monitoraggio su cui si trova la finestra:** Una volta che l'applicazione è contrassegnata come compatibile con DPI per monitor, WPF continuerà a ridimensionare le dimensioni della finestra, la grafica e le dimensioni del carattere in base al valore DPI del sistema.</span><span class="sxs-lookup"><span data-stu-id="105d2-206">**Adjusts the window dimension, re-layout and re-render graphics content and select fonts based on initial DPI of the monitor the window is on:** Once the application is marked as per-monitor DPI-aware, WPF will still scale the window size, graphics and font size based on the system DPI.</span></span> <span data-ttu-id="105d2-207">Poiché, all'avvio dell'app, non è garantito che il valore DPI del sistema corrisponda a quello del monitor su cui è stata avviata la finestra, la libreria regola questi valori una volta caricata la finestra.</span><span class="sxs-lookup"><span data-stu-id="105d2-207">Since, at app launch, the system DPI is not guaranteed to be the same as the DPI of the monitor the window is launched on, the library adjust these values once the window is loaded.</span></span> <span data-ttu-id="105d2-208">La classe base **PerMonitorDPIWindow** li aggiorna nel gestore **OnLoaded ()** .</span><span class="sxs-lookup"><span data-stu-id="105d2-208">The base class **PerMonitorDPIWindow** updates these in the **OnLoaded()** handler.</span></span>

    <span data-ttu-id="105d2-209">La dimensione della finestra viene aggiornata cambiando le proprietà **Width** e **Height** della finestra.</span><span class="sxs-lookup"><span data-stu-id="105d2-209">The Window size is updated by changing the **Width** and **Height** properties of the Window.</span></span> <span data-ttu-id="105d2-210">Il layout e le dimensioni vengono aggiornati applicando una trasformazione di ridimensionamento appropriata al nodo radice della finestra WPF.</span><span class="sxs-lookup"><span data-stu-id="105d2-210">The layout and size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span>

    ```C++
    void PerMonitorDPIWindow::OnLoaded(Object^ , RoutedEventArgs^ ) 
    {   
    if (m_perMonitorEnabled)
        {
        m_source = (HwndSource^) PresentationSource::FromVisual((Visual^) this);
        HwndSourceHook^ hook = gcnew HwndSourceHook(this, &PerMonitorDPIWindow::HandleMessages);
        m_source->AddHook(hook); 
                
        //Calculate the DPI used by WPF.                    
        m_wpfDPI = 96.0 *  m_source->CompositionTarget->TransformToDevice.M11; 

        //Get the Current DPI of the monitor of the window. 
        m_currentDPI = NativeHelpers::PerMonitorDPIHelper::GetDpiForWindow(m_source->Handle);

        //Calculate the scale factor used to modify window size, graphics and text
        m_scaleFactor = m_currentDPI / m_wpfDPI; 
            
        //Update Width and Height based on the on the current DPI of the monitor
        Width = Width * m_scaleFactor;
        Height = Height * m_scaleFactor;

        //Update graphics and text based on the current DPI of the monitor
    UpdateLayoutTransform(m_scaleFactor);
        }
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

-   <span data-ttu-id="105d2-211">**Risponde a WM \_ Notifica della finestra DPICHANGED:** aggiornamento delle dimensioni della finestra, della grafica e delle dimensioni del carattere in base al valore dpi passato nella notifica della finestra.</span><span class="sxs-lookup"><span data-stu-id="105d2-211">**Responds to WM\_DPICHANGED window notification:** Update the window size, graphics and font size based on the DPI passed in the window notification.</span></span> <span data-ttu-id="105d2-212">La classe base **PerMonitorDPIWindow** gestisce la notifica della finestra nel metodo **HandleMessages ()** .</span><span class="sxs-lookup"><span data-stu-id="105d2-212">The base class **PerMonitorDPIWindow** handles the window notification in the **HandleMessages()** method.</span></span>

    <span data-ttu-id="105d2-213">La dimensione della finestra viene aggiornata chiamando **SetWindowPos** usando le informazioni passate nell' *lParam* del messaggio della finestra.</span><span class="sxs-lookup"><span data-stu-id="105d2-213">The Window size is updated by calling **SetWindowPos** using the information passed in the *lparam* of the window message.</span></span> <span data-ttu-id="105d2-214">Il layout e le dimensioni della grafica vengono aggiornati applicando una trasformazione di ridimensionamento appropriata al nodo radice della finestra WPF.</span><span class="sxs-lookup"><span data-stu-id="105d2-214">The layout and graphics size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span> <span data-ttu-id="105d2-215">Il fattore di scala viene calcolato utilizzando il valore DPI passato nel *wParam* del messaggio della finestra.</span><span class="sxs-lookup"><span data-stu-id="105d2-215">The scale factor is calculated by using the DPI passed in the *wparam* of the window message.</span></span>

    ```C++
    IntPtr PerMonitorDPIWindow::HandleMessages(IntPtr hwnd, int msg, IntPtr wParam, IntPtr lParam, bool% )
    {
    double oldDpi;
    switch (msg)
        {
        case WM_DPICHANGED:
        LPRECT lprNewRect = (LPRECT)lParam.ToPointer();
        SetWindowPos(static_cast<HWND>(hwnd.ToPointer()), 0, lprNewRect->left, lprNewRect-
            >top, lprNewRect->right - lprNewRect->left, lprNewRect->bottom - lprNewRect->top, 
           SWP_NOZORDER | SWP_NOOWNERZORDER | SWP_NOACTIVATE);
        oldDpi = m_currentDPI;
        m_currentDPI = static_cast<int>(LOWORD(wParam.ToPointer()));
        if (oldDpi != m_currentDPI) 
            {
            OnDPIChanged();
            }
        break;
        }
    return IntPtr::Zero;
    }

    void PerMonitorDPIWindow::OnDPIChanged() 
    {
    m_scaleFactor = m_currentDPI / m_wpfDPI;
    UpdateLayoutTransform(m_scaleFactor);
    DPIChanged(this, EventArgs::Empty);
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

## <a name="handling-dpi-change-for-assets-like-images"></a><span data-ttu-id="105d2-216">Gestione delle modifiche DPI per asset come le immagini</span><span class="sxs-lookup"><span data-stu-id="105d2-216">Handling DPI change for assets like images</span></span>

<span data-ttu-id="105d2-217">Per aggiornare il contenuto della grafica, l'applicazione WPF di esempio applica una trasformazione di ridimensionamento al nodo radice dell'applicazione WPF.</span><span class="sxs-lookup"><span data-stu-id="105d2-217">In order to update graphics content, the sample WPF application applies a scale transform to the root node of the WPF application.</span></span> <span data-ttu-id="105d2-218">Sebbene questa operazione funzioni correttamente per il contenuto di cui è stato eseguito il rendering in modo nativo da WPF (rettangolo, testo e così via), ciò implica che gli asset bitmap come le immagini vengono ridimensionati da WPF.</span><span class="sxs-lookup"><span data-stu-id="105d2-218">While this works well for content that is rendered natively by WPF (rectangle, text etc.), this implies that bitmap assets like images are scaled by WPF.</span></span>

<span data-ttu-id="105d2-219">Per evitare bitmap sfocate causate dalla scalabilità, lo sviluppatore di applicazioni WPF può scrivere un controllo immagine DPI personalizzato che seleziona un asset diverso in base al valore DPI corrente del monitoraggio su cui si trova la finestra.</span><span class="sxs-lookup"><span data-stu-id="105d2-219">In order to avoid blurred bitmaps caused by scaling, the WPF application developer can write a custom DPI image control that selects a different asset based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="105d2-220">Il controllo immagine può basarsi sull'evento **DPIChanged ()** generato per la finestra WPF che utilizza da **PerMonitorDPIWindow**, quando viene modificato il valore dpi.</span><span class="sxs-lookup"><span data-stu-id="105d2-220">The image control can rely on the **DPIChanged()** event fired for the WPF window that consumes from the **PerMonitorDPIWindow**, when the DPI changes.</span></span>

> [!Note]  
> <span data-ttu-id="105d2-221">Il controllo immagine deve anche selezionare il controllo destro durante l'avvio dell'app nel gestore eventi della finestra WPF **caricata ()** .</span><span class="sxs-lookup"><span data-stu-id="105d2-221">The image control should also select the right control during app launch in the **Loaded()** WPF window event handler.</span></span>

 

 

 