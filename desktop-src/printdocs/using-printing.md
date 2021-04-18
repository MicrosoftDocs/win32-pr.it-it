---
description: In questa sezione viene descritto come stampare da un programma desktop di Windows nativo.
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: Stampa di app desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbecbac997d000f50e7c912e57be42cc8fe239b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317285"
---
# <a name="desktop-app-printing"></a>Stampa di app desktop

In questa sezione viene descritto come stampare da un programma desktop di Windows nativo.

## <a name="overview"></a>Panoramica

Per offrire la migliore esperienza utente quando si esegue la stampa da un programma Windows nativo, è necessario che il programma sia progettato per la stampa da un thread dedicato. In un programma Windows nativo il programma è responsabile della gestione degli eventi e dei messaggi dell'interfaccia utente. Le operazioni di stampa possono richiedere periodi di calcolo intensivo quando viene eseguito il rendering del contenuto dell'applicazione per la stampante, che può impedire che il programma risponda all'interazione dell'utente se questa elaborazione viene eseguita nello stesso thread dell'elaborazione di eventi dell'interazione dell'utente.

Se si ha già familiarità con la scrittura di un programma Windows nativo multithread, è possibile passare direttamente alla [modalità di stampa da un'applicazione Windows](how-to--print-from-a-windows-application.md) e apprendere come aggiungere funzionalità di stampa al programma.

### <a name="basic-windows-program-requirements"></a>Requisiti del programma Windows di base

Per ottimizzare le prestazioni e la velocità di risposta del programma, non eseguire l'elaborazione del processo di stampa di un programma nel thread che elabora l'interazione dell'utente.

Questa separazione della stampa dall'interazione dell'utente influirà sul modo in cui il programma gestisce i dati dell'applicazione. Prima di iniziare a scrivere l'applicazione, è necessario comprendere attentamente queste implicazioni. Negli argomenti seguenti vengono descritti i requisiti di base per la gestione della stampa in un thread separato di un programma.

### <a name="windows-program-basics"></a>Nozioni fondamentali sui programmi Windows

Un programma Windows nativo deve fornire la routine della finestra principale per elaborare i messaggi della finestra ricevuti dal sistema operativo. Ogni finestra di un programma Windows ha una funzione **WndProc** corrispondente che elabora i messaggi della finestra. Il thread in cui viene eseguita questa funzione è denominato interfaccia utente, o interfaccia utente, thread.

**Usare le risorse per le stringhe.**  
Usare le risorse di stringa dal file di risorse del programma invece delle costanti stringa per le stringhe che potrebbero dover essere modificate quando si supporta un'altra lingua. Prima che un programma possa usare una risorsa di stringa come stringa, il programma deve recuperare la risorsa dal file di risorse e copiarla in un buffer di memoria locale. Questa operazione richiede una programmazione aggiuntiva all'inizio, ma consente di semplificare la modifica, la traduzione e la localizzazione del programma in futuro.  
**Elaborare i dati nei passaggi.**  
Elaborare il processo di stampa nei passaggi che possono essere interrotti. Questa progettazione consente all'utente di annullare un'operazione di elaborazione lunga prima del completamento e impedisce al programma di bloccare altri programmi che potrebbero essere in esecuzione nello stesso momento.  
**Usare i dati utente della finestra.**  
Le applicazioni di stampa hanno spesso più finestre e thread. Per rendere disponibili i dati tra i thread e i passaggi di elaborazione senza utilizzare variabili globali statiche, fare riferimento alle strutture di dati mediante un puntatore ai dati che fa parte della finestra in cui vengono utilizzate.  


Nell'esempio di codice riportato di seguito viene illustrato un punto di ingresso principale per un'applicazione di stampa. Questo esempio illustra come usare le risorse di stringa anziché le costanti di stringa e Mostra anche il ciclo di messaggi principale che elabora i messaggi della finestra del programma.


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

I programmi Windows nativi stampati devono essere progettati per l'elaborazione multithread. Uno dei requisiti di una progettazione multithread consiste nel proteggere gli elementi dati del programma in modo che siano sicuri per l'uso di più thread contemporaneamente. È possibile proteggere gli elementi dati utilizzando gli oggetti di sincronizzazione e organizzando i dati per evitare conflitti tra i thread. Allo stesso tempo, il programma deve impedire modifiche ai dati del programma durante la stampa. Il programma di esempio usa diverse tecniche di programmazione multithread.

 **Eventi di sincronizzazione**  
Il programma di esempio utilizza eventi, handle di thread e funzioni di attesa per sincronizzare l'elaborazione tra il thread di stampa e il programma principale e per indicare che i dati sono in uso.  
**Messaggi di Windows specifici dell'applicazione**  
Il programma di esempio utilizza messaggi finestra specifici dell'applicazione per rendere il programma più compatibile con altri programmi Windows nativi. Suddividendo l'elaborazione in passaggi più piccoli e accodando tali passaggi nel ciclo di messaggi della finestra, è più semplice per Windows gestire l'elaborazione senza bloccare altre applicazioni che potrebbero essere in esecuzione nel computer.  
**strutture di dati**  
Il programma di esempio non viene scritto in uno stile orientato a oggetti utilizzando oggetti e classi, sebbene raggruppa gli elementi dati in strutture di dati. Nell'esempio non viene utilizzato un approccio orientato agli oggetti per evitare di implicare che un approccio è migliore o peggiore di un altro.  
È possibile utilizzare le funzioni e le strutture di dati del programma di esempio come punto di partenza quando si progetta il programma. Se si decide di progettare un programma orientato a oggetti o meno, è importante tenere presente che è necessario raggruppare gli elementi dati correlati in modo che sia possibile utilizzarli in modo sicuro in thread diversi, se necessario.  


### <a name="printer-device-context"></a>Contesto dispositivo stampante

Durante la stampa, potrebbe essere necessario eseguire il rendering del contenuto da stampare in un contesto di dispositivo. [Procedura: recuperare un contesto di dispositivo stampante](retrieving-a-printer-device-context.md) descrive i diversi modi in cui è possibile ottenere un contesto di dispositivo stampante.

## <a name="related-topics"></a>Argomenti correlati



[Come stampare da un'applicazione Windows](how-to--print-from-a-windows-application.md)


 

 



