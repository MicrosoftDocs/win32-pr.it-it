---
description: Questa sezione descrive come stampare da un programma desktop Windows nativo.
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: Stampa di app desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf5e0ebab666258f62b1e6bb87497d38a1b521fdde9a7668bb28e3bb3e9868e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112111"
---
# <a name="desktop-app-printing"></a>Stampa di app desktop

Questa sezione descrive come stampare da un programma desktop Windows nativo.

## <a name="overview"></a>Panoramica

Per offrire la migliore esperienza utente quando si stampa da un programma Windows nativo, il programma deve essere progettato per la stampa da un thread dedicato. In un programma Windows nativo, il programma è responsabile della gestione di messaggi e eventi dell'interfaccia utente. Le operazioni di stampa possono richiedere periodi di calcolo intenso durante il rendering del contenuto dell'applicazione per la stampante, che può impedire al programma di rispondere all'interazione dell'utente se l'elaborazione viene eseguita nello stesso thread dell'elaborazione degli eventi dell'interazione dell'utente.

Se si ha già familiarità con la scrittura di un programma Windows nativo multi-thread, passare direttamente a Come stampare da un'applicazione [Windows](how-to--print-from-a-windows-application.md) e apprendere come aggiungere funzionalità di stampa al programma.

### <a name="basic-windows-program-requirements"></a>Requisiti di Windows di base

Per prestazioni ottimali e velocità di risposta del programma, non eseguire l'elaborazione del processo di stampa di un programma nel thread che elabora l'interazione dell'utente.

Questa separazione della stampa dall'interazione dell'utente influirà sul modo in cui il programma gestisce i dati dell'applicazione. È necessario comprendere attentamente queste implicazioni prima di iniziare a scrivere l'applicazione. Negli argomenti seguenti vengono descritti i requisiti di base per la gestione della stampa in un thread separato di un programma.

### <a name="windows-program-basics"></a>Windows Nozioni di base sul programma

Un programma Windows deve fornire la procedura della finestra principale per elaborare i messaggi della finestra ricevuti dal sistema operativo. Ogni finestra in un programma Windows dispone di una funzione **WndProc** corrispondente che elabora questi messaggi di finestra. Il thread in cui viene eseguita questa funzione è denominato interfaccia utente, o thread dell'interfaccia utente.

**Usare le risorse per le stringhe.**  
Usare le risorse stringa del file di risorse del programma invece delle costanti stringa per le stringhe che potrebbero dover essere modificate quando si supporta un'altra lingua. Prima che un programma possa usare una risorsa stringa come stringa, il programma deve recuperare la risorsa dal file di risorse e copiarla in un buffer di memoria locale. Ciò richiede una programmazione aggiuntiva all'inizio, ma consente di semplificare la modifica, la traduzione e la localizzazione del programma in futuro.  
**Elaborare i dati in passaggi.**  
Elaborare il processo di stampa in passaggi che possono essere interrotti. Questa progettazione consente all'utente di annullare un'operazione di elaborazione lunga prima del completamento e impedisce al programma di bloccare altri programmi che potrebbero essere in esecuzione contemporaneamente.  
**Usare i dati utente della finestra.**  
Le applicazioni di stampa hanno spesso diverse finestre e thread. Per mantenere i dati disponibili tra thread e passaggi di elaborazione senza usare variabili globali statiche, fare riferimento alle strutture di dati tramite un puntatore ai dati che fa parte della finestra in cui vengono usate.  


Nell'esempio di codice seguente viene illustrato un punto di ingresso principale per un'applicazione di stampa. Questo esempio illustra come usare le risorse stringa anziché le costanti stringa e mostra anche il ciclo di messaggi principale che elabora i messaggi della finestra del programma.


```C++
int APIENTRY 
wWinMain(
        HINSTANCE hInstance, 
        HINSTANCE hPrevInstance, 
        LPWSTR lpCmdLine, 
        int nCmdShow
)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    MSG msg;
    HACCEL hAccelTable;
    HRESULT hr = S_OK;

    // Register the main window class name
    WCHAR szWindowClass[MAXIMUM_RESOURCE_STRING_LENGTH];            
    LoadString(
        hInstance, 
        IDC_PRINTSAMPLE, 
        szWindowClass, 
        MAXIMUM_RESOURCE_STRING_LENGTH);
    MyRegisterClass(hInstance, szWindowClass);

    // Perform application initialization:
    if (!InitInstance (hInstance, nCmdShow))
    {
        // Unable to initialize this instance of the application
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_INSTINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }    
    
    // Init COM for printing interfaces
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        // Unable to initialize COM
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_COMINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }

    hAccelTable = LoadAccelerators(
                    hInstance, 
                    MAKEINTRESOURCE(IDC_PRINTSAMPLE));

    // Main message handling loop
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    // Uninitialize (close) the COM interface
    CoUninitialize();

    return (int) msg.wParam;
}
```



### <a name="document-information"></a>Informazioni sul documento

I Windows nativi che stampano devono essere progettati per l'elaborazione multi-thread. Uno dei requisiti di una progettazione multithread è proteggere gli elementi dati del programma in modo che siano sicuri per l'uso di più thread contemporaneamente. È possibile proteggere gli elementi di dati usando oggetti di sincronizzazione e organizzando i dati per evitare conflitti tra i thread. Allo stesso tempo, il programma deve impedire modifiche ai dati del programma durante la stampa. Il programma di esempio usa diverse tecniche di programmazione multi-thread.

 **Eventi di sincronizzazione**  
Il programma di esempio usa eventi, handle di thread e funzioni di attesa per sincronizzare l'elaborazione tra il thread di stampa e il programma principale e per indicare che i dati sono in uso.  
**Messaggi di errore specifici Windows'applicazione**  
Il programma di esempio usa messaggi di finestra specifici dell'applicazione per rendere il programma più compatibile con altri programmi Windows nativi. Suddividendo l'elaborazione in passaggi più piccoli e a accodamento di tali passaggi nel ciclo di messaggi della finestra, il Windows può gestire più facilmente l'elaborazione senza bloccare altre applicazioni che potrebbero essere in esecuzione nel computer.  
**strutture di dati**  
Il programma di esempio non è scritto in uno stile orientato a oggetti usando oggetti e classi, anche se raggruppa gli elementi dati in strutture di dati. L'esempio non usa un approccio orientato a oggetti per evitare di implicare che un approccio sia migliore o peggiore di un altro.  
È possibile usare le funzioni e le strutture di dati del programma di esempio come punto di partenza per la progettazione del programma. Indipendentemente dal fatto che si decida di progettare o meno un programma orientato a oggetti, l'importante considerazione da ricordare per la progettazione è raggruppare gli elementi dati correlati in modo che sia possibile usarli in modo sicuro in thread diversi in base alle esigenze.  


### <a name="printer-device-context"></a>Contesto di dispositivo della stampante

Durante la stampa, potrebbe essere necessario eseguire il rendering del contenuto da stampare in un contesto di dispositivo. [Procedura: Recuperare un contesto di dispositivo della](retrieving-a-printer-device-context.md) stampante descrive i diversi modi in cui è possibile ottenere un contesto di dispositivo della stampante.

## <a name="related-topics"></a>Argomenti correlati



[Come stampare da un'Windows applicazione](how-to--print-from-a-windows-application.md)


 

 



