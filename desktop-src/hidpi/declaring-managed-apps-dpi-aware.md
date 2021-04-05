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
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a>Sviluppo di un'applicazione WPF sensibile ai valori DPI del monitor

**API importanti**

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> **Questa pagina illustra lo sviluppo WPF legacy per Windows 8.1.** Per lo sviluppo di applicazioni WPF per Windows 10, vedere la <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">documentazione più recente su GitHub.</a>

 

Windows 8.1 offre agli sviluppatori nuove funzionalità per la creazione di applicazioni desktop con compatibilità DPI per monitor. Per sfruttare i vantaggi di questa funzionalità, un'applicazione con riconoscimento DPI per monitor deve eseguire le operazioni seguenti:

-   Modificare le dimensioni della finestra per mantenere una dimensione fisica che risulti coerente in qualsiasi visualizzazione
-   Ricreare il layout e rieseguire il rendering della grafica per le nuove dimensioni della finestra
-   Selezione dei tipi di carattere ridimensionati in modo appropriato per il livello DPI
-   Selezionare e caricare asset bitmap personalizzati per il livello DPI

Per semplificare la creazione di un'applicazione compatibile con DPI per il monitoraggio, Windows 8.1 fornisce le seguenti Win32APIs Microsoft:

-   [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (o voce del manifesto dpi) imposta il processo su un livello di riconoscimento dpi specificato, che quindi determina il modo in cui Windows ridimensiona l'interfaccia utente. Questa operazione sostituisce [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).
-   [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) restituisce il livello di riconoscimento dpi. Questa operazione sostituisce [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).
-   [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) restituisce il valore dpi per un monitoraggio.
-   La notifica della finestra [**WM \_ DPICHANGED**](wm-dpichanged.md) viene inviata a applicazioni compatibili con DPI per monitor quando la posizione di una finestra viene modificata in modo che la maggior parte dell'area interseca un monitor con un valore DPI diverso da dpi prima della modifica della posizione o quando l'utente sposta il dispositivo di scorrimento della visualizzazione. Per creare un'applicazione che esegue il ridimensionamento e il nuovo rendering quando un utente lo sposta in una visualizzazione diversa, usare questa notifica.

Per ulteriori informazioni sui vari livelli di riconoscimento DPI supportati per le applicazioni desktop in Windows 8.1 vedere l'argomento relativo alla [scrittura di applicazioni desktop e Win32 DPI-Aware](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).

## <a name="dpi-scaling-and-wpf"></a>Ridimensionamento DPI e WPF

Per impostazione predefinita, le applicazioni Windows Presentation Foundation (WPF) sono compatibili con DPI di sistema. Per le definizioni dei diversi livelli di riconoscimento DPI, vedere l'argomento relativo alla [scrittura DPI-Aware applicazioni desktop e Win32](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)). Il sistema grafico WPF USA unità indipendenti dal dispositivo per abilitare la risoluzione e l'indipendenza del dispositivo. WPF ridimensiona ogni Device Independent Pixel automaticamente in base al valore DPI corrente del sistema. Questo consente la scalabilità automatica delle applicazioni WPF quando il DPI del monitoraggio su cui si trova la finestra è lo stesso valore DPI del sistema. Tuttavia, poiché le applicazioni WPF sono compatibili con i dpi di sistema, l'applicazione verrà ridimensionata dal sistema operativo quando l'applicazione viene spostata in un monitor con un valore DPI diverso o quando il dispositivo di scorrimento nel pannello di controllo viene usato per modificare il valore DPI. Il ridimensionamento del sistema operativo può comportare la visualizzazione sfocatura delle applicazioni WPF, soprattutto quando il ridimensionamento non è integrale. Per evitare il ridimensionamento di applicazioni WPF, è necessario aggiornarle in modo che siano compatibili con i valori DPI per monitor.

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a>Procedura dettagliata per l'esempio WPF compatibile con monitoraggio

L' [esempio WPF per monitoraggio](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) con rilevamento è un'applicazione WPF di esempio aggiornata per essere compatibile con i valori dpi per monitor. L'esempio è costituito da due progetti:

-   NativeHelpers. vcxproj: si tratta di un progetto Helper nativo che implementa la funzionalità di base per fare in modo che un'applicazione WPF sia compatibile con DPI per il monitoraggio usando il Win32APIs precedente. Il progetto contiene due classi:
    -   PerMonDPIHelpers: classe che fornisce funzioni di supporto per le operazioni correlate a DPI come il recupero del valore DPI corrente del monitoraggio attivo, l'impostazione di un processo in modo che sia compatibile con DPI per il monitoraggio e così via.
    -   PerMonitorDPIWindow: classe di base derivata da **System. Windows. Window** che implementa la funzionalità per fare in modo che una finestra dell'applicazione WPF sia compatibile con DPI per il monitoraggio. Regola le dimensioni della finestra, le dimensioni del rendering della grafica e le dimensioni del carattere in base al valore DPI del monitoraggio anziché al valore DPI del sistema.
-   WPFApplication. csproj: applicazione WPF di esempio che usa PerMonitorDPIWindow (PerMonitorDPIWindow) e Mostra come la finestra dell'applicazione e il rendering vengono ridimensionati quando la finestra viene spostata in un monitor con un valore DPI diverso o quando il dispositivo di scorrimento nel pannello di controllo dello schermo viene usato per modificare il valore DPI.

Per eseguire l'esempio, attenersi alla procedura seguente:

1.  Scaricare e decomprimere l' [esempio WPF per monitoraggio](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) con rilevamento
2.  Avviare Microsoft Visual Studio e selezionare **File > apri > progetto/soluzione**
3.  Passare alla directory che contiene l'esempio decompresso. Passare alla directory denominata per l'esempio e fare doppio clic sul file della soluzione Visual Studio (. sln).
4.  Premere F7 o utilizzare **compila > Compila soluzione** per compilare l'esempio
5.  Premere CTRL + F5 o utilizzare **debug > avvia senza eseguire debug** per eseguire l'esempio

Per vedere l'effetto della modifica del valore DPI in un'applicazione WPF aggiornata in modo da essere compatibile con DPI per il monitoraggio utilizzando la classe di base nell'esempio, spostare la finestra dell'applicazione da e verso le visualizzazioni con DPI diversi. Quando la finestra viene spostata tra i monitoraggi, le dimensioni della finestra e la scalabilità dell'interfaccia utente vengono aggiornate in base al valore DPI della visualizzazione utilizzando il sistema grafico scalabile di WPF, anziché essere ridimensionato dal sistema operativo. L'interfaccia utente dell'applicazione viene sottoposta a rendering in modo nativo e non appare sfocata. Se non sono presenti due schermi con DPI diversi, modificare il valore DPI cambiando il dispositivo di scorrimento nel pannello di controllo dello schermo. Se si modifica il dispositivo di scorrimento e si fa clic su **applica** , la finestra dell'applicazione verrà ridimensionata e verrà aggiornata automaticamente.

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a>Aggiornamento di un'applicazione WPF esistente in modo che sia in grado di riconoscere DPI per monitoraggio usando un progetto Helper nell'esempio WPF

Se si dispone di un'applicazione WPF esistente e si desidera utilizzare il progetto Helper DPI dall'esempio per renderla compatibile con DPI, attenersi alla seguente procedura.

1.  Scaricare e decomprimere l'esempio WPF per monitoraggio con rilevamento
2.  Avviare Visual Studio e selezionare **File > aprire > progetto/soluzione**
3.  Passare alla directory che contiene un'applicazione WPF esistente e fare doppio clic sul file della soluzione Visual Studio (. sln).
4.  Fare clic con il pulsante destro del mouse su **soluzione > aggiungi > progetto esistente** ![ una schermata che illustra la selezione del menu Aggiungi: progetto esistente](images/scrvs-image1.png)
5.  Nella finestra di dialogo selezione file passare alla directory che contiene l'esempio decompresso. Aprire la directory denominata per l'esempio, passare alla cartella "NativeHelpers", selezionare il file di progetto Visual C++ "NativeHelpers. vcxproj" e fare clic su **OK** .
6.  Fare clic con il pulsante destro del mouse sul progetto NativeHelpers e selezionare **Compila**. Questa operazione genererà NativeHelpers.dll che verrà aggiunta come riferimento all'applicazione WPF nel passaggio successivo ![ una schermata che illustra la selezione del menu Compila](images/scrvs-image2.png)
7.  Aggiungere un riferimento a NativeHelpers.dll dall'applicazione WPF. Espandere il progetto di applicazione WPF, fare clic con il pulsante destro del mouse su **riferimenti** e scegliere **Aggiungi riferimento.**
8.  Nella finestra di dialogo risultante espandere la sezione **soluzione** . In **progetti**, selezionare NativeHelpers e fare clic su **OK** per ![ scattare una schermata che illustra la finestra di dialogo Resource Manager](images/scrvs-image3.png)
9.  Espandere il progetto di applicazione WPF, espandere **Proprietà** e aprire **AssemblyInfo. cs**. Apportare le aggiunte seguenti a AssemblyInfo. cs
    -   Aggiungere un riferimento a System. Windows. Media nella sezione di riferimento (mediante System. Windows. Media;)
    -   Aggiungere l'attributo DisableDpiAwareness ( `[assembly: DisableDpiAwareness]` )

    ![screenshot che illustra le proprietà aggiuntive](images/scrvs-image4.png)
10. Ereditare la classe principale della finestra WPF dalla classe base PerMonitorDPIWindow
    -   Aggiornare il file con estensione CS della finestra principale di WPF per ereditare dalla classe di base PerMonitorDPIWindow
        -   Aggiungere un riferimento a NativeHelpers nella sezione di riferimento aggiungendo la riga `using NativeHelpers;`
        -   Ereditare la classe della finestra principale dalla classe PerMonitorDPIWindow

        ![screenshot che illustra il riferimento c++](images/scrvs-image5.png)
    -   Aggiornare il file con estensione XAML della finestra principale di WPF per ereditare dalla classe di base PerMonitorDPIWindow
        -   Aggiungere un riferimento a NativeHelpers nella sezione di riferimento aggiungendo la riga `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`
        -   Ereditare la classe della finestra principale dalla classe PerMonitorDPIWindow

        ![screenshot che illustra l'aggiunta del riferimento. XAML](images/scrvs-image6.png)
11. Premere F7 o utilizzare **compila > Compila soluzione** per compilare l'esempio
12. Premere CTRL + F5 o utilizzare **debug > avvia senza eseguire debug** per eseguire l'esempio

L'applicazione di [esempio WPF compatibile con monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) illustra come un'applicazione WPF può essere aggiornata in modo che sia compatibile con DPI per il monitoraggio rispondendo alla notifica della finestra [**\_ DPICHANGED di WM**](wm-dpichanged.md) . In risposta alla notifica della finestra, l'esempio aggiorna la trasformazione di scala utilizzata da WPF in base al valore DPI corrente del monitoraggio su cui si trova la finestra. Il *wParam* della notifica della finestra contiene il nuovo valore dpi in *wParam*. *LParam* contiene un rettangolo con le dimensioni e la posizione della nuova finestra suggerita, ridimensionata per il nuovo valore dpi.

Nota:

> [!Note]  
> Poiché questo esempio sovrascrive le dimensioni della finestra e la trasformazione di ridimensionamento del nodo radice della finestra WPF, è possibile che lo sviluppatore di applicazioni possa richiedere ulteriore lavoro se:
>
> -   Le dimensioni della finestra influiscano su altre parti dell'applicazione come questa finestra WPF ospitata all'interno di un'altra applicazione.
> -   L'applicazione WPF che estende questa classe sta impostando altre trasformazioni sull'oggetto visivo radice. Nell'esempio è possibile sovrascrivere un'altra trasformazione applicata dall'applicazione WPF stessa.

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a>Cenni preliminari sul progetto Helper nell'esempio WPF

Per rendere un'applicazione WPF esistente compatibile con DPI per il monitoraggio, la libreria NativeHelpers offre le funzionalità seguenti:

-   **Contrassegna l'applicazione WPF come compatibile con DPI per ponitor:** L'applicazione WPF è contrassegnata come compatibile con DPI per monitoraggio chiamando [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) per il processo corrente. Contrassegnare l'applicazione come compatibile con DPI per il monitoraggio garantisce che

    -   Il sistema operativo non ridimensiona l'applicazione quando il valore DPI del sistema non corrisponde al valore DPI corrente del monitoraggio in cui si trova la finestra dell'applicazione.
    -   Il messaggio [**WM \_ DPICHANGED**](wm-dpichanged.md) viene inviato ogni volta che viene modificato il valore dpi della finestra

-   Consente **di regolare la dimensione della finestra, di ricreare il layout e di eseguire nuovamente il rendering del contenuto grafico e di selezionare i tipi di carattere basati sul valore dpi iniziale del monitoraggio su cui si trova la finestra:** Una volta che l'applicazione è contrassegnata come compatibile con DPI per monitor, WPF continuerà a ridimensionare le dimensioni della finestra, la grafica e le dimensioni del carattere in base al valore DPI del sistema. Poiché, all'avvio dell'app, non è garantito che il valore DPI del sistema corrisponda a quello del monitor su cui è stata avviata la finestra, la libreria regola questi valori una volta caricata la finestra. La classe base **PerMonitorDPIWindow** li aggiorna nel gestore **OnLoaded ()** .

    La dimensione della finestra viene aggiornata cambiando le proprietà **Width** e **Height** della finestra. Il layout e le dimensioni vengono aggiornati applicando una trasformazione di ridimensionamento appropriata al nodo radice della finestra WPF.

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

    

-   **Risponde a WM \_ Notifica della finestra DPICHANGED:** aggiornamento delle dimensioni della finestra, della grafica e delle dimensioni del carattere in base al valore dpi passato nella notifica della finestra. La classe base **PerMonitorDPIWindow** gestisce la notifica della finestra nel metodo **HandleMessages ()** .

    La dimensione della finestra viene aggiornata chiamando **SetWindowPos** usando le informazioni passate nell' *lParam* del messaggio della finestra. Il layout e le dimensioni della grafica vengono aggiornati applicando una trasformazione di ridimensionamento appropriata al nodo radice della finestra WPF. Il fattore di scala viene calcolato utilizzando il valore DPI passato nel *wParam* del messaggio della finestra.

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

    

## <a name="handling-dpi-change-for-assets-like-images"></a>Gestione delle modifiche DPI per asset come le immagini

Per aggiornare il contenuto della grafica, l'applicazione WPF di esempio applica una trasformazione di ridimensionamento al nodo radice dell'applicazione WPF. Sebbene questa operazione funzioni correttamente per il contenuto di cui è stato eseguito il rendering in modo nativo da WPF (rettangolo, testo e così via), ciò implica che gli asset bitmap come le immagini vengono ridimensionati da WPF.

Per evitare bitmap sfocate causate dalla scalabilità, lo sviluppatore di applicazioni WPF può scrivere un controllo immagine DPI personalizzato che seleziona un asset diverso in base al valore DPI corrente del monitoraggio su cui si trova la finestra. Il controllo immagine può basarsi sull'evento **DPIChanged ()** generato per la finestra WPF che utilizza da **PerMonitorDPIWindow**, quando viene modificato il valore dpi.

> [!Note]  
> Il controllo immagine deve anche selezionare il controllo destro durante l'avvio dell'app nel gestore eventi della finestra WPF **caricata ()** .

 

 

 