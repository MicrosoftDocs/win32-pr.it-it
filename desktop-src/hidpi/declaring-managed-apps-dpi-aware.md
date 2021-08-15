---
title: Sviluppo di un'applicazione WPF sensibile ai valori DPI del monitor
description: Nota Questa pagina illustra lo sviluppo WPF legacy per Windows 8.1. Se si sviluppano applicazioni WPF per Windows 10, vedere la documentazione più recente su GitHub. .
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Windows Interfaccia utente, applicazioni con grado di riconoscere DPI
- Windows Interfaccia utente, DPI elevato
- Applicazioni che sono in grado di riconoscere DPI
- valori DPI alti
- scrittura di applicazioni Win32 in grado di riconoscere DPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1527412e3259efca7d81285c6ba7ed42dbaebf43d37307342de02f1d2ce9d339
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249687"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a>Sviluppo di un'applicazione WPF sensibile ai valori DPI del monitor

**API importanti**

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> **Questa pagina illustra lo sviluppo WPF legacy per Windows 8.1.** Se si sviluppano applicazioni WPF per Windows 10, vedere la <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">documentazione più recente su GitHub.</a>

 

Windows 8.1 offre agli sviluppatori nuove funzionalità per creare applicazioni desktop che sono in grado di riconoscere DPI per monitor. Per sfruttare questa funzionalità, un'applicazione con supporto DPI per monitor deve eseguire le operazioni seguenti:

-   Modificare le dimensioni della finestra per mantenere dimensioni fisiche coerenti su qualsiasi schermo
-   Eseguire di nuovo il layout e il rendering della grafica per le nuove dimensioni della finestra
-   Selezionare i tipi di carattere che vengono ridimensionati in modo appropriato per il livello DPI
-   Selezionare e caricare asset bitmap personalizzati per il livello DPI

Per semplificare la creazione di un'applicazione con supporto DPI per monitor, Windows 8.1 fornisce le seguenti api Microsoft Win32API:

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (o voce del manifesto DPI) imposta il processo su un livello di consapevolezza DPI specificato, che determina quindi come Windows ridimensiona l'interfaccia utente. Questo sostituisce [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).
-   [**GetProcessDpiAwareness restituisce**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) il livello di consapevolezza DPI. Questo sostituisce [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) restituisce il valore DPI per un monitoraggio.
-   La notifica della finestra [**WM \_ DPICHANGED**](wm-dpichanged.md) viene inviata alle applicazioni con supporto DPI per monitor quando la posizione di una finestra cambia in modo che la maggior parte dell'area interseci un monitor con un valore DPI diverso dal valore DPI prima della modifica della posizione o quando l'utente sposta il dispositivo di scorrimento dello schermo. Per creare un'applicazione che viene ridimensionata e di cui viene nuovamente eseguito il rendering quando un utente la sposta in una visualizzazione diversa, usare questa notifica.

Per altri dettagli sui vari livelli di riconoscimento DPI supportati per le applicazioni desktop in Windows 8.1 vedere l'argomento Writing DPI-Aware Desktop and Win32 Applications (Scrittura di applicazioni desktop e [Win32).](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

## <a name="dpi-scaling-and-wpf"></a>Ridimensionamento DPI e WPF

Windows Presentation Foundation (WPF) sono in grado di riconoscere DPI di sistema per impostazione predefinita. Per le definizioni dei diversi livelli di riconoscimento DPI, vedere l'argomento Writing DPI-Aware Desktop and Win32 Applications (Scrittura di applicazioni [Desktop e Win32).](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)) Il sistema grafico WPF usa unità indipendenti dal dispositivo per abilitare la risoluzione e l'indipendenza del dispositivo. WPF ridimensiona automaticamente ogni pixel indipendente dal dispositivo in base al valore DPI del sistema corrente. In questo modo le applicazioni WPF possono essere ridimensionate automaticamente quando il valore DPI del monitor in cui si trova la finestra è lo stesso DPI di sistema. Tuttavia, poiché le applicazioni WPF supportano dpi di sistema, l'applicazione verrà ridimensionata dal sistema operativo quando l'applicazione viene spostata in un monitor con un valore DPI diverso o quando il dispositivo di scorrimento nel pannello di controllo viene usato per modificare il valore DPI. Il ridimensionamento del sistema operativo può causare la sfocatura delle applicazioni WPF, soprattutto quando il ridimensionamento è non integrale. Per evitare il ridimensionamento delle applicazioni WPF, è necessario aggiornarlo in modo che siano in grado di riconoscere DPI per ogni monitor.

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a>Procedura dettagliata per l'esempio WPF con supporto per monitor

[L'esempio WPF con supporto per monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) è un'applicazione WPF di esempio aggiornata per essere in grado di riconoscere DPI per monitor. L'esempio è costituito da due progetti:

-   NativeHelpers.vcxproj: si tratta di un progetto helper nativo che implementa la funzionalità di base per rendere un'applicazione WPF in base al monitoraggio che supporta DPI utilizzando le api Win32 precedenti. Il progetto contiene due classi:
    -   PerMonDPIHelpers: classe che fornisce funzioni helper per operazioni correlate a DPI, ad esempio il recupero del valore DPI corrente del monitoraggio attivo, l'impostazione di un processo in modo che sia in grado di riconoscere DPI per monitor e così via.
    -   PerMonitorDPIWindow: classe di base derivata da **System.Windows. Finestra** che implementa la funzionalità per fare in modo che una finestra dell'applicazione WPF sia in grado di riconoscere dpi per monitor. Regola le dimensioni della finestra, le dimensioni del rendering della grafica e le dimensioni del carattere in base al valore DPI del monitor anziché al valore DPI di sistema.
-   WPFApplication.csproj: applicazione WPF di esempio che usa PerMonitorDPIWindow (PerMonitorDPIWindow) e illustra come la finestra dell'applicazione e il rendering vengono ridimensionati quando la finestra viene spostata in un monitor con un valore DPI diverso o quando il dispositivo di scorrimento nel pannello di controllo Visualizza viene usato per modificare il valore DPI.

Per eseguire l'esempio, seguire questa procedura:

1.  Scaricare e decomprimere [l'esempio WPF con supporto per monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)
2.  Avviare Microsoft Visual Studio e selezionare **File > Apri > Project/Soluzione**
3.  Passare alla directory che contiene l'esempio decompresso. Passare alla directory denominata per l'esempio e fare doppio clic sul file Visual Studio soluzione (con estensione sln)
4.  Premere F7 o usare Build **> Build Solution (Compila soluzione)** per compilare l'esempio
5.  Premere CTRL+F5 o usare Debug > **Avvia senza eseguire** debug per eseguire l'esempio

Per vedere l'impatto della modifica del valore DPI in un'applicazione WPF che viene aggiornata per essere in grado di riconoscere DPI per monitor usando la classe di base nell'esempio, spostare la finestra dell'applicazione da e verso schermi con DPI diversi. Quando la finestra viene spostata tra i monitor, le dimensioni della finestra e la scala dell'interfaccia utente vengono aggiornate in base al valore DPI dello schermo usando il sistema grafico scalabile di WPF, anziché essere ridimensionato dal sistema operativo. Il rendering dell'interfaccia utente dell'applicazione viene eseguito in modo nativo e non appare sfocato. Se non sono presenti due schermi con valori DPI diversi, modificare il valore DPI modificando il dispositivo di scorrimento nel pannello di controllo Schermo. Modificando il dispositivo di scorrimento e **facendo clic su Applica,** la finestra dell'applicazione verrà ridimensionata e la scalabilità dell'interfaccia utente verrà automaticamente aggiornato.

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a>Aggiornamento di un'applicazione WPF esistente in modo che sia in grado di riconoscere dpi per monitor usando un progetto helper nell'esempio WPF

Se si dispone di un'applicazione WPF esistente e si vuole sfruttare il progetto helper DPI dell'esempio per renderlo in grado di riconoscere DPI, seguire questa procedura.

1.  Scaricare e decomprimere l'esempio WPF con supporto per monitor
2.  Avviare Visual Studio e selezionare **File > Apri > Project/Soluzione**
3.  Passare alla directory che contiene un'applicazione WPF esistente e fare doppio clic sul file Visual Studio soluzione (con estensione sln)
4.  Fare clic con il **pulsante destro del mouse > aggiungi > esistente Project** screenshot che illustra la selezione del menu Aggiungi progetto ![ esistente](images/scrvs-image1.png)
5.  Nella finestra di dialogo di selezione dei file passare alla directory che contiene l'esempio decompresso. Aprire la directory denominata per l'esempio, passare alla cartella "NativeHelpers", selezionare il file di progetto Visual C++ "NativeHelpers.vcxproj" e fare clic su **OK**
6.  Fare clic con il pulsante destro del mouse sul progetto NativeHelpers e **scegliere Compila.** Verrà generata una NativeHelpers.dll che verrà aggiunta come riferimento all'applicazione WPF nel passaggio successivo, una schermata che illustra la selezione del ![ menu di compilazione](images/scrvs-image2.png)
7.  Aggiungere un riferimento a NativeHelpers.dll dall'applicazione WPF. Espandere il progetto di applicazione WPF, fare clic con il pulsante destro **del mouse su Riferimenti** e scegliere Aggiungi **riferimento.**
8.  Nella finestra di dialogo risultante espandere la **sezione** Soluzione. In **Progetti selezionare** NativeHelpers e fare clic su **OK,** ![ schermata che illustra la finestra di dialogo gestione risorse](images/scrvs-image3.png)
9.  Espandere il progetto di applicazione WPF, **espandere Proprietà** e **aprire AssemblyInfo.cs.** Apportare le aggiunte seguenti ad AssemblyInfo.cs
    -   Aggiungere un riferimento a System. Windows. Supporti nella sezione di riferimento (usando System.Windows. Media;)
    -   Aggiungere l'attributo DisableDpiAwareness ( `[assembly: DisableDpiAwareness]` )

    ![Screenshot che illustra le proprietà aggiuntive](images/scrvs-image4.png)
10. Ereditare la classe finestra WPF principale dalla classe di base PerMonitorDPIWindow
    -   Aggiornare il file cs della finestra WPF principale in modo che erediti dalla classe di base PerMonitorDPIWindow
        -   Aggiungere un riferimento a NativeHelpers nella sezione reference aggiungendo la riga `using NativeHelpers;`
        -   Ereditare la classe della finestra principale dalla classe PerMonitorDPIWindow

        ![Screenshot che illustra le informazioni di riferimento su c++](images/scrvs-image5.png)
    -   Aggiornare il file con estensione xaml della finestra WPF principale in modo che erediti dalla classe di base PerMonitorDPIWindow
        -   Aggiungere un riferimento a NativeHelpers nella sezione reference aggiungendo la riga `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`
        -   Ereditare la classe della finestra principale dalla classe PerMonitorDPIWindow

        ![Screenshot che illustra l'aggiunta del riferimento xaml](images/scrvs-image6.png)
11. Premere F7 o usare Build **> Build Solution (Compila soluzione)** per compilare l'esempio
12. Premere CTRL+F5 o usare Debug > **Avvia senza eseguire** debug per eseguire l'esempio

[L'applicazione](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) di esempio WPF con supporto per monitor illustra come aggiornare un'applicazione WPF in modo che sia in grado di riconoscere DPI per monitor rispondendo alla notifica della finestra [**WM \_ DPICHANGED.**](wm-dpichanged.md) In risposta alla notifica della finestra, l'esempio aggiorna la trasformazione della scala usata da WPF in base al valore DPI corrente del monitoraggio in cui è attivata la finestra. Il *parametro wParam* della notifica della finestra contiene il nuovo valore DPI in *wParam*. lParam *contiene* un rettangolo con le dimensioni e la posizione della nuova finestra suggerita, ridimensionata per il nuovo valore DPI.

Nota:

> [!Note]  
> Poiché questo esempio sovrascrive le dimensioni della finestra e la trasformazione della scala del nodo radice della finestra WPF, lo sviluppatore dell'applicazione potrebbe richiedere ulteriori operazioni se:
>
> -   Le dimensioni della finestra influiscono su altre parti dell'applicazione, ad esempio questa finestra WPF, ospitate all'interno di un'altra applicazione.
> -   L'applicazione WPF che estende questa classe imposta un'altra trasformazione nell'oggetto visivo radice; L'esempio può sovrascrivere un'altra trasformazione applicata dall'applicazione WPF stessa.

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a>Panoramica del progetto helper nell'esempio WPF

Per rendere un'applicazione WPF esistente in grado di riconoscere DPI per monitor, la libreria NativeHelpers fornisce le funzionalità seguenti:

-   **Contrassegna l'applicazione WPF in base al valore DPI:** L'applicazione WPF viene contrassegnata come in grado di riconoscere DPI in base al monitor chiamando [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) per il processo corrente. Contrassegnando l'applicazione come in grado di riconoscere DPI per monitor, si garantisce che

    -   Il sistema operativo non ridimensiona l'applicazione quando il valore DPI del sistema non corrisponde al valore DPI corrente del monitoraggio in cui è attivata la finestra dell'applicazione
    -   Il [**messaggio \_ WM DPICHANGED**](wm-dpichanged.md) viene inviato ogni volta che cambia il valore DPI della finestra

-   **Regola la dimensione della finestra, ri-layout** ed esegue nuovamente il rendering del contenuto grafico e seleziona i tipi di carattere in base al valore DPI iniziale del monitoraggio in cui si trova la finestra: Dopo che l'applicazione è stata contrassegnata come in grado di riconoscere DPI per monitor, WPF ridimensiona comunque le dimensioni della finestra, della grafica e del carattere in base al valore DPI del sistema. Poiché, all'avvio dell'app, non è garantito che il valore DPI di sistema sia uguale al valore DPI del monitoraggio in cui viene avviata la finestra, la libreria regola questi valori dopo il caricamento della finestra. La classe di base **PerMonitorDPIWindow** le aggiorna nel **gestore OnLoaded().**

    Le dimensioni della finestra vengono aggiornate modificando **le proprietà Width** e **Height** della finestra. Il layout e le dimensioni vengono aggiornati applicando una trasformazione di scala appropriata al nodo radice della finestra WPF.

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

    

-   **Risponde a WM \_ Notifica della finestra DPICHANGED: aggiorna** le dimensioni della finestra, la grafica e le dimensioni del carattere in base al valore DPI passato nella notifica della finestra. La classe di base **PerMonitorDPIWindow** gestisce la notifica della finestra nel **metodo HandleMessages().**

    Le dimensioni della finestra vengono aggiornate chiamando **SetWindowPos** usando le informazioni passate nel *parametro del* messaggio della finestra. Il layout e le dimensioni della grafica vengono aggiornati applicando una trasformazione di scala appropriata al nodo radice della finestra WPF. Il fattore di scala viene calcolato usando il valore DPI passato nel *parametro wparam* del messaggio della finestra.

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

    

## <a name="handling-dpi-change-for-assets-like-images"></a>Gestione della modifica DPI per asset come le immagini

Per aggiornare il contenuto grafico, l'applicazione WPF di esempio applica una trasformazione di scala al nodo radice dell'applicazione WPF. Anche se funziona bene per il contenuto di cui VIENE eseguito il rendering in modo nativo da WPF (rettangolo, testo e così via), ciò implica che gli asset bitmap come le immagini vengono ridimensionati da WPF.

Per evitare bitmap sfocate causate dal ridimensionamento, lo sviluppatore di applicazioni WPF può scrivere un controllo immagine DPI personalizzato che seleziona un asset diverso in base al valore DPI corrente del monitor in cui si trova la finestra. Il controllo immagine può basarsi sull'evento **DPIChanged()** generato per la finestra WPF che utilizza **da PerMonitorDPIWindow,** quando il valore DPI cambia.

> [!Note]  
> Il controllo immagine deve anche selezionare il controllo appropriato durante l'avvio dell'app nel gestore eventi della finestra WPF **Loaded().**

 

 

 