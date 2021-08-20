---
title: Sviluppo di applicazioni desktop DPI elevate in Windows
description: Questo contenuto è destinato agli sviluppatori che stanno cercando di aggiornare le applicazioni desktop per gestire il fattore di scala dello schermo dinamico(ovvero
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c6389553ce2265752e3552fdaaf848e3ac70eede8df3b4fd9e560861bf15f33d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036254"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a>Sviluppo di applicazioni desktop DPI elevate in Windows

Questo contenuto è destinato agli sviluppatori che vogliono aggiornare le applicazioni desktop per gestire le modifiche del fattore di scala di visualizzazione (punti per pollice o DPI) in modo dinamico, consentendo alle applicazioni di essere nitide su qualsiasi visualizzazione su cui viene eseguito il rendering.

Per iniziare, se si crea una nuova app Windows da zero, è consigliabile creare un'applicazione [UWP (Universal Windows Platform).](/windows/uwp/get-started/whats-a-uwp) Le applicazioni UWP vengono &mdash; ridimensionate automaticamente e dinamicamente per ogni visualizzazione su cui &mdash; sono in esecuzione.

Le applicazioni desktop che usano tecnologie di programmazione Windows meno recenti (programmazione Win32 non elaborata, form Windows, Windows Presentation Framework (WPF) e così via, non sono in grado di gestire automaticamente il ridimensionamento DPI senza ulteriori attività di sviluppo. Senza questo tipo di lavoro, le applicazioni appariranno sfocate o con dimensioni erre in molti scenari di utilizzo comuni. Questo documento fornisce contesto e informazioni su ciò che riguarda l'aggiornamento di un'applicazione desktop per il rendering corretto.

## <a name="display-scale-factor--dpi"></a>Visualizzare il fattore di scala & DPI

Con l'avanzamento della tecnologia di visualizzazione, i produttori di pannelli di visualizzazione hanno inserito un numero crescente di pixel in ogni unità di spazio fisico nei pannelli. Ciò ha comportato che i punti per pollice (DPI) dei pannelli di visualizzazione moderni siano molto più alti di quanto non siano stati in origine. In passato, la maggior parte degli schermi aveva 96 pixel per pollice lineare di spazio fisico (96 DPI); nel 2017 sono immediatamente disponibili schermi con quasi 300 DPI o versioni successive.

La maggior parte dei framework dell'interfaccia utente desktop legacy presuppone che il valore DPI dello schermo non cambi durante la durata del processo.  Questo presupposto non è più vero, con le DPA di visualizzazione che cambiano comunemente più volte nel corso della durata di un processo dell'applicazione. Alcuni scenari comuni in cui il fattore di scala di visualizzazione/modifiche DPI sono:

-   Configurazioni a più monitor in cui ogni visualizzazione ha un fattore di scala diverso e l'applicazione viene spostata da uno schermo a un altro (ad esempio un display 4K e uno da 1080p)
-   Ancoraggio e disinserzione di un computer portatile DPI alto con un display esterno a basso DPI (o viceversa)
-   Connessione tramite Desktop remoto da un portatile/tablet DPI alto a un dispositivo con DPI basso (o viceversa)
-   Modifica delle impostazioni del fattore di scalabilità di visualizzazione durante l'esecuzione delle applicazioni

In questi scenari, le applicazioni UWP si ridisegnano automaticamente per il nuovo valore DPI. Per impostazione predefinita, e senza altre attività di sviluppo, le applicazioni desktop non lo fanno. Le applicazioni desktop che non esigino questo lavoro aggiuntivo per rispondere alle modifiche DPI possono apparire sfocate o con dimensioni erre per l'utente.

## <a name="dpi-awareness-mode"></a>Modalità di riconoscimento DPI

Le applicazioni desktop devono indicare Windows se supportano il ridimensionamento DPI. Per impostazione predefinita, il sistema considera le applicazioni desktop DPI inconsapevoli e estende le finestre con bitmap. Impostando una delle modalità di riconoscimento DPI disponibili seguenti, le applicazioni possono indicare in modo esplicito Windows come gestire il ridimensionamento DPI:

### <a name="dpi-unaware"></a>DPI inconsapevole

Il rendering delle applicazioni DPI non consapevoli viene eseguito con un valore DPI fisso pari a 96 (100%). Ogni volta che queste applicazioni vengono eseguite su uno schermo con una scala di visualizzazione maggiore di 96 DPI, Windows estenderà la bitmap dell'applicazione alle dimensioni fisiche previste. In questo modo l'applicazione appare sfocata.

### <a name="system-dpi-awareness"></a>Riconoscimento DPI di sistema

Le applicazioni desktop che sono in grado di riconoscere DPI di sistema ricevono in genere il valore DPI del monitoraggio connesso primario al momento dell'accesso utente. Durante l'inizializzazione, l'interfaccia utente viene adattata (controlli di ridimensionamento, scelta delle dimensioni dei caratteri, caricamento di asset e così via) usando il valore DPI di sistema. Di conseguenza, le applicazioni che supportano DPI di sistema non sono ridimensionate da DPI (bitmap estesa) Windows il rendering dei display in tale singola DPI. Quando l'applicazione viene spostata in una visualizzazione con un fattore di scala diverso o se il fattore di scala dello schermo cambia in caso contrario, Windows ridimensiona le finestre dell'applicazione, rendendole sfocate. In effetti, le applicazioni desktop che sono in grado di riconoscere DPI di sistema vengono visualizzate solo con un unico fattore di scala dello schermo, diventando sfocate ogni volta che cambia il valore DPI.

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a>Per-Monitor e Per-Monitor riconoscimento DPI (V2)

È consigliabile aggiornare le applicazioni desktop per usare la modalità di riconoscimento DPI per monitoraggio, consentendo loro di eseguire immediatamente il rendering corretto ogni volta che cambia il valore DPI. Quando un'applicazione segnala Windows che vuole essere eseguita in questa modalità, Windows non eseguirà l'estensione dell'applicazione quando il valore DPI cambia, ma invierà [WM \_ DPICHANGED](wm-dpichanged.md) alla finestra dell'applicazione. È quindi responsabilità completa dell'applicazione gestire il ridimensionamento per il nuovo valore DPI. La maggior parte dei framework dell'interfaccia utente usati dalle applicazioni desktop (Windows controlli comuni (comctl32), Windows Forms, Windows Presentation Framework e così via, non supporta il ridimensionamento DPI automatico, richiedendo agli sviluppatori di ridimensionare e riposizionare il contenuto delle finestre.

Esistono due versioni di Per-Monitor che un'applicazione può registrarsi come: versione 1 e versione 2 (PMv2). La registrazione di un processo come in esecuzione in modalità di riconoscimento PMv2 comporta:

1.  L'applicazione che viene notificata quando cambia il valore DPI (HWND di primo livello e figlio)
2.  L'applicazione visualizza i pixel non elaborati di ogni visualizzazione
3.  L'applicazione non viene mai ridimensionata in base Windows
4.  Area automatica non client (didascalia della finestra, barre di scorrimento e così via) Ridimensionamento DPI per Windows
5.  Le finestre di dialogo Win32 [(da CreateDialog)](/windows/desktop/api/winuser/nf-winuser-createdialogw)vengono ridimensionate automaticamente in base Windows
6.  Asset bitmap disegnati dal tema nei controlli comuni (caselle di controllo, sfondi dei pulsanti e così via) di cui viene eseguito automaticamente il rendering con il fattore di scala DPI appropriato

Quando vengono eseguite in Per-Monitor modalità di riconoscimento v2, le applicazioni vengono notificate quando il valore DPI è stato modificato. Se un'applicazione non si ridimensiona per il nuovo valore DPI, l'interfaccia utente dell'applicazione sarà troppo piccola o troppo grande (a seconda della differenza nei valori DPI precedente e nuovo).

> [!Note]  
> Per-Monitor consapevolezza V1 (PMv1) è molto limitata. È consigliabile che le applicazioni usino PMv2.

La tabella seguente illustra il rendering delle applicazioni in scenari diversi:

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Modalità di riconoscimento DPI</th>
<th>Windows Versione introdotta</th>
<th>Visualizzazione di DPI da parte dell'applicazione</th>
<th>Comportamento in base alla modifica DPI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignari</td>
<td>N/A</td>
<td>Tutti gli schermi sono da 96 DPI</td>
<td>Estensione bitmap (sfocata)</td>
</tr>
<tr class="even">
<td>Sistema</td>
<td>Vista</td>
<td>Tutti gli schermi hanno lo stesso valore DPI (il valore DPI della visualizzazione primaria al momento dell'avvio della sessione utente corrente)</td>
<td>Estensione bitmap (sfocata)</td>
</tr>
<tr class="odd">
<td>Per-Monitor</td>
<td>8.1</td>
<td>Valore DPI della visualizzazione in cui si trova principalmente la finestra dell'applicazione</td>
<td><ul>
<li>HWND di primo livello viene notificato della modifica DPI</li>
<li>Nessun ridimensionamento DPI di elementi dell'interfaccia utente.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Per-Monitor V2</td>
<td>Windows 10 Creators Update (1703)</td>
<td>Valore DPI della visualizzazione in cui si trova principalmente la finestra dell'applicazione</td>
<td><ul>
<li>Gli HWND <span class="underline">di primo</span> livello e figlio vengono informati della modifica DPI</li>
</ul>
<br/> <span class="underline">Ridimensionamento DPI automatico di:</span>
<ul>
<li>Area non client</li>
<li>Bitmap disegnate dal tema nei controlli comuni (comctl32 V6)</li>
<li>Dialogs (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a>Riconoscimento DPI per ogni monitoraggio (V1)

Per-Monitor la modalità di riconoscimento DPI V1 (PMv1) è stata introdotta con Windows 8.1. Questa modalità di riconoscimento DPI è molto limitata e offre solo le funzionalità elencate di seguito. È consigliabile che le applicazioni desktop usino Per-Monitor modalità di riconoscimento v2, supportata Windows 10 1703 o versioni successive.

Il supporto iniziale per la consapevolezza per ogni monitoraggio offriva solo le applicazioni seguenti:

1.  Gli HWND di primo livello vengono informati di una modifica DPI e vengono fornite nuove dimensioni suggerite
2.  Windows l'estensione dell'interfaccia utente dell'applicazione non verrà mappata in bitmap
3.  L'applicazione visualizza tutti gli schermi in pixel fisici (vedere la virtualizzazione)

In Windows 10 1607 o versioni successive, le applicazioni PMv1 possono anche chiamare [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) durante WM NCCREATE per richiedere che Windows ridimensiona correttamente \_ l'area non client della finestra.

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a>Supporto del ridimensionamento DPI per ogni monitoraggio da parte del framework dell'interfaccia utente/tecnologia

La tabella seguente mostra il livello di supporto di riconoscimento DPI per monitoraggio offerto da vari framework dell'interfaccia Windows a Windows 10 1703:

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Framework/tecnologia</th>
<th>Supporto</th>
<th>Versione sistema operativo</th>
<th>Ridimensionamento DPI gestito da</th>
<th>Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Piattaforma UWP (Universal Windows Platform)</td>
<td>Full</td>
<td>1607</td>
<td>Framework dell'interfaccia utente</td>
<td><a href="/windows/uwp/get-started/whats-a-uwp">Piattaforma UWP (Universal Windows Platform)</a></td>
</tr>
<tr class="even">
<td>Raw Win32/Common Controls V6 (comctl32.dll)</td>
<td><ul>
<li>Messaggi di notifica delle modifiche DPI inviati a tutti gli HWND</li>
<li>Il rendering degli asset disegnati dal tema viene eseguito correttamente nei controlli comuni</li>
<li>Ridimensionamento DPI automatico per i dialoghe</li>
</ul></td>
<td>1703</td>
<td>Applicazione</td>
<td><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">GitHub Esempio</a></td>
</tr>
<tr class="odd">
<td>Windows Forms</td>
<td>Ridimensionamento DPI automatico per monitoraggio limitato per alcuni controlli</td>
<td>1703</td>
<td>Framework dell'interfaccia utente</td>
<td><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Supporto DPI elevato in Windows moduli</a></td>
</tr>
<tr class="even">
<td>Windows Presentation Framework (WPF)</td>
<td>Le applicazioni WPF native ridimensionano WPF ospitato in altri framework e altri framework ospitati in WPF non vengono ridimensionati automaticamente</td>
<td>1607</td>
<td>Framework dell'interfaccia utente</td>
<td><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">GitHub Esempio</a></td>
</tr>
<tr class="odd">
<td>GDI</td>
<td>Nessuno</td>
<td>N/A</td>
<td>Applicazione</td>
<td>Vedere <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">Ridimensionamento GDI con valori DPI elevati</a></td>
</tr>
<tr class="even">
<td>GDI+</td>
<td>Nessuno</td>
<td>N/A</td>
<td>Applicazione</td>
<td>Vedere <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">Ridimensionamento GDI con valori DPI elevati</a></td>
</tr>
<tr class="odd">
<td>MFC</td>
<td>Nessuno</td>
<td>N/A</td>
<td>Applicazione</td>
<td>N/A</td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a>Aggiornamento di applicazioni esistenti

Per aggiornare un'applicazione desktop esistente per gestire correttamente il ridimensionamento DPI, è necessario aggiornarla in modo che, come minimo, le parti importanti dell'interfaccia utente siano aggiornate per rispondere alle modifiche DPI.

La maggior parte delle applicazioni desktop viene eseguita in modalità di riconoscimento DPI di sistema. Le applicazioni che sono in grado di riconoscere DPI di sistema vengono in genere ridimensionate in base al valore DPI dello schermo primario ,ovvero la visualizzazione in cui si trova la barra delle applicazioni al momento dell'avvio della sessione Windows sistema. Quando il valore DPI cambia, Windows bitmap estenderà l'interfaccia utente di queste applicazioni, causando spesso la sfocatura. Quando si aggiorna un'applicazione con supporto DPI di sistema per diventare in grado di riconoscere DPI per monitor, il codice che gestisce il layout dell'interfaccia utente deve essere aggiornato in modo che non sia eseguito solo durante l'inizializzazione dell'applicazione, ma anche ogni volta che viene ricevuta una notifica di modifica DPI[(WM \_ DPICHANGED](wm-dpichanged.md) nel caso di Win32). Ciò comporta in genere la revisione di eventuali presupposti nel codice che l'interfaccia utente deve essere ridimensionata una sola volta.

Inoltre, nel caso della programmazione Win32, molte API Win32 non hanno alcun contesto DPI o di visualizzazione, quindi restituiranno solo valori relativi all'API DPI di sistema. Può essere utile eseguire il grep del codice per cercare alcune di queste API e sostituirle con varianti con supporto DPI. Alcune delle API comuni con varianti che sono in grado di riconoscere DPI sono:



| Versione DPI singola   | Per-Monitor versione        |
|----------------------|----------------------------|
| GetSystemMetrics     | GetSystemMetricsForDpi     |
| AdjustWindowRectEx   | AdjustWindowRectExForDpi   |
| Systemparametersinfo | SystemParametersInfoForDpi |
| GetDpiForMonitor     | GetDpiForWindow            |



 

È anche buona idea cercare dimensioni hard-coded nella codebase che presuppongono un valore DPI costante, sostituendole con codice che conti correttamente per il ridimensionamento DPI. Di seguito è riportato un esempio che incorpora tutti questi suggerimenti:

### <a name="example"></a>Esempio:

L'esempio seguente illustra un caso Win32 semplificato di creazione di un HWND figlio. La chiamata a CreateWindow presuppone che l'applicazione sia in esecuzione a 96 DPI e che le dimensioni e la posizione del pulsante non siano corrette in corrispondenza di DPI più elevati:


```
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON,  
        50,  
        50,  
        100,  
        50,  
        hWnd, (HMENU)NULL, NULL, NULL); 
} 
```



Il codice aggiornato seguente mostra:

1.  Codice di creazione della finestra DPI che ridimensiona la posizione e le dimensioni dell'HWND figlio per il valore DPI della finestra padre
2.  Risposta alla modifica DPI riposizionando e ridimensionando HWND figlio
3.  Dimensioni hard-coded rimosse e sostituite con codice che risponde alle modifiche DPI


```
#define INITIALX_96DPI 50 
#define INITIALY_96DPI 50 
#define INITIALWIDTH_96DPI 100 
#define INITIALHEIGHT_96DPI 50 
 
 
// DPI scale the position and size of the button control 
void UpdateButtonLayoutForDpi(HWND hWnd) 
{ 
    int iDpi = GetDpiForWindow(hWnd); 
    int dpiScaledX = MulDiv(INITIALX_96DPI, iDpi, 96); 
    int dpiScaledY = MulDiv(INITIALY_96DPI, iDpi, 96); 
    int dpiScaledWidth = MulDiv(INITIALWIDTH_96DPI, iDpi, 96); 
    int dpiScaledHeight = MulDiv(INITIALHEIGHT_96DPI, iDpi, 96); 
    SetWindowPos(hWnd, hWnd, dpiScaledX, dpiScaledY, dpiScaledWidth, dpiScaledHeight, SWP_NOZORDER | SWP_NOACTIVATE); 
} 
 
... 
 
case WM_CREATE: 
{ 
    // Add a button 
    HWND hWndChild = CreateWindow(L"BUTTON", L"Click Me",  
        WS_CHILD|WS_VISIBLE|BS_PUSHBUTTON, 
        0, 
        0, 
        0, 
        0, 
        hWnd, (HMENU)NULL, NULL, NULL); 
    if (hWndChild != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndChild); 
    } 
} 
break; 
 
case WM_DPICHANGED: 
{ 
    // Find the button and resize it 
    HWND hWndButton = FindWindowEx(hWnd, NULL, NULL, NULL); 
    if (hWndButton != NULL) 
    { 
        UpdateButtonLayoutForDpi(hWndButton); 
    } 
} 
break; 
```



Quando si aggiorna un'applicazione in grado di riconoscere DPI di sistema, alcuni passaggi comuni da seguire sono:

1.  Contrassegnare il processo come con supporto DPI per monitoraggio (V2) usando un manifesto dell'applicazione (o un altro metodo, a seconda dei framework dell'interfaccia utente usati).
2.  Rendere riutilizzabile la logica di layout dell'interfaccia utente e spostarla dal codice di inizializzazione dell'applicazione in modo che possa essere riutilizzata quando si verifica una modifica DPI (WM DPICHANGED nel caso della programmazione \_ Windows (Win32).
3.  Invalidare il codice che presuppone che i dati sensibili API (DPI/fonts/sizes/etc.) non devono mai essere aggiornati. È molto comune memorizzare nella cache le dimensioni dei caratteri e i valori DPI durante l'inizializzazione del processo. Quando si aggiorna un'applicazione per diventare in grado di riconoscere DPI per ogni monitoraggio, i dati sensibili alle DPI devono essere rivalutati ogni volta che viene rilevato un nuovo valore DPI.
4.  Quando si verifica una modifica DPI, ricaricare (o rasterizzare) tutti gli asset bitmap per il nuovo valore DPI o, facoltativamente, estendere gli asset attualmente caricati alle dimensioni corrette.
5.  Grep per le API che non sono Per-Monitor DPI e le sostituisce con Per-Monitor api che supportano DPI (se applicabile). Esempio: sostituire GetSystemMetrics con GetSystemMetricsForDpi.
6.  Testare l'applicazione in un sistema multi-DPI/multi-display.
7.  Per tutte le finestre di primo livello nell'applicazione che non è possibile aggiornare per la scala DPI correttamente, usare il ridimensionamento DPI in modalità mista (descritto di seguito) per consentire l'estensione bitmap di queste finestre di primo livello dal sistema.

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a>Mixed-Mode ridimensionamento DPI (ridimensionamento DPI sub-process)

Quando si aggiorna un'applicazione per supportare la consapevolezza DPI per ogni monitoraggio, a volte può diventare poco pratica o impossibile aggiornare ogni finestra dell'applicazione in un'unica operazione. Ciò può essere dovuto semplicemente al tempo e al lavoro necessario per aggiornare e testare tutta l'interfaccia utente o perché non si è proprietari di tutto il codice dell'interfaccia utente che è necessario eseguire (se l'applicazione carica probabilmente l'interfaccia utente di terze parti). In queste situazioni, Windows offre un modo per semplificare il mondo della consapevolezza per ogni monitoraggio consentendo di eseguire alcune delle finestre dell'applicazione (solo di primo livello) nella modalità di riconoscimento DPI originale, concentrando il tempo e l'aggiornamento energetico sulle parti più importanti dell'interfaccia utente.

Di seguito è riportata un'illustrazione dell'aspetto seguente: si aggiorna l'interfaccia utente principale dell'applicazione ("Finestra principale" nell'illustrazione) per l'esecuzione con riconoscimento DPI per monitoraggio mentre si eseguono altre finestre nella modalità esistente ("Finestra secondaria").

![differenze nel ridimensionamento dpi tra le modalità di riconoscimento](images/hub-page-illustrations.png)

Prima dell'Windows 10 dell'anniversario (1607), la modalità di riconoscimento DPI di un processo era una proprietà a livello di processo. A partire dal Windows 10 dell'anniversario, questa proprietà può ora essere impostata per ogni **finestra di primo** livello. (**Le finestre** figlio devono continuare a corrispondere alle dimensioni di ridimensionamento dell'elemento padre). Una finestra di primo livello è definita come finestra senza padre. Si tratta in genere di una finestra "normale" con pulsanti di riduzione a icona, ingrandimento e chiusura. Lo scenario a cui è destinata la consapevolezza DPI del processo secondario è la scalabilità dell'interfaccia utente secondaria di Windows (bitmap estesa) mentre si concentrano il tempo e le risorse sull'aggiornamento dell'interfaccia utente primaria.

Per abilitare il riconoscimento DPI del processo secondario, chiamare [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) prima e dopo qualsiasi chiamata di creazione della finestra. La finestra creata verrà associata alla consapevolezza DPI impostata tramite SetThreadDpiAwarenessContext. Usare la seconda chiamata per ripristinare il riconoscimento DPI del thread corrente.

Anche se l'uso del ridimensionamento DPI sub-process consente di basarsi su Windows per eseguire parte del ridimensionamento DPI per l'applicazione, può aumentare la complessità dell'applicazione. È importante comprendere gli svantaggi di questo approccio e la natura delle complessità introdotte. Per altre informazioni sul riconoscimento DPI del processo secondario, vedere [Scalabilità DPI](high-dpi-improvements-for-desktop-applications.md) in modalità mista e API con riconoscimento DPI.

## <a name="testing-your-changes"></a>Test delle modifiche

Dopo aver aggiornato l'applicazione per diventare in grado di riconoscere DPI per ogni monitoraggio, è importante convalidare che l'applicazione risponda correttamente alle modifiche DPI in un ambiente DPI misto. Alcune specifiche da testare includono:

1.  Spostamento di finestre dell'applicazione da una visualizzazione all'altra di valori DPI diversi
2.  Avvio dell'applicazione in visualizzazione di valori DPI diversi
3.  Modifica del fattore di scala per il monitoraggio mentre l'applicazione è in esecuzione
4.  Modifica della visualizzazione utilizzata come visualizzazione _primaria,_ disconnessione dall'Windows, quindi test di nuovo dell'applicazione dopo l'accesso. Ciò è particolarmente utile per trovare codice che usa dimensioni/dimensioni hard-coded.

## <a name="common-pitfalls-win32"></a>Insidie comuni (Win32)

**Non si usa il rettangolo suggerito fornito in WM \_ DPICHANGED**

Quando Windows alla finestra dell'applicazione un messaggio [**WM \_ DPICHANGED,**](wm-dpichanged.md) questo messaggio include un rettangolo suggerito da usare per ridimensionare la finestra. È fondamentale che l'applicazione usi questo rettangolo per ridimensionare se stesso, come in questo modo:

1.  Assicurarsi che il cursore del mouse rimanga nella stessa posizione relativa nella finestra durante il trascinamento tra gli schermi
2.  Impedire alla finestra dell'applicazione di entrare in un ciclo di modifica dpi ricorsiva in cui una modifica DPI attiva una modifica DPI successiva, che attiva un'altra modifica DPI.

Se si hanno requisiti specifici dell'applicazione che impediscono di usare il rettangolo suggerito Windows nel messaggio WM \_ DPICHANGED, vedere [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md). Questo messaggio può essere usato per Windows le dimensioni desiderate, una volta che si è verificata la modifica DPI, evitando comunque i problemi descritti in precedenza.

**Mancanza di documentazione sulla virtualizzazione**

Quando un processo O HWND è in esecuzione come DPI inconsapevole o in grado di riconoscere DPI di sistema, può essere una bitmap estesa da Windows. In questo caso, Windows ridimensiona e converte le informazioni sensibili a DPI da alcune API allo spazio delle coordinate del thread chiamante. Ad esempio, se un thread senza DPI esegue query sulle dimensioni dello schermo durante l'esecuzione su uno schermo con valori DPI elevati, Windows virtualizzerà la risposta data all'applicazione come se lo schermo fosse in 96 unità DPI. In alternativa, quando un thread in grado di riconoscere DPI di sistema interagisce con una visualizzazione con un valore DPI diverso da quello in uso all'avvio della sessione dell'utente corrente, Windows ridimensiona alcune chiamate API nello spazio delle coordinate che HWND userebbe se fosse in esecuzione al fattore di scala DPI originale.

Quando si aggiorna correttamente l'applicazione desktop alla scalabilità DPI, può essere difficile sapere quali chiamate API possono restituire valori virtualizzati in base al contesto del thread. Queste informazioni non sono attualmente sufficientemente documentate da Microsoft. Tenere presente che se si chiama un'API di sistema da un contesto di thread non in grado di riconoscere DPI o di sistema, il valore restituito potrebbe essere virtualizzato. Assicurarsi quindi che il thread sia in esecuzione nel contesto DPI previsto durante l'interazione con la schermata o le singole finestre. Quando si modifica temporaneamente il contesto DPI di un thread usando [SetThreadDpiAwarenessContext,](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)assicurarsi di ripristinare il contesto precedente al termine per evitare di causare un comportamento non corretto altrove nell'applicazione.

**Molte WINDOWS non hanno un contesto DPI**

Molte API Windows legacy non includono un contesto DPI o HWND come parte della relativa interfaccia. Di conseguenza, gli sviluppatori devono spesso eseguire operazioni aggiuntive per gestire il ridimensionamento di qualsiasi informazione sensibile a DPI, ad esempio dimensioni, punti o icone. Ad esempio, gli sviluppatori che usano [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) devono usare icone con estensione bitmap o usare API alternative per caricare icone di dimensioni corrette per il valore DPI appropriato, ad esempio [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).

**Reimpostazione forzata del riconoscimento DPI a livello di processo**

In generale, la modalità di riconoscimento DPI del processo non può essere modificata dopo l'inizializzazione del processo. Windows possibile, tuttavia, modificare forzatamente la modalità di riconoscimento DPI del processo se si tenta di interrompere il requisito che tutti gli HWND in un albero della finestra hanno la stessa modalità di riconoscimento DPI. In tutte le versioni di Windows, a Windows 10 1703, non è possibile eseguire HWND diversi in un albero HWND in modalità di riconoscimento DPI diverse. Se si tenta di creare una relazione padre-figlio che interrompe questa regola, è possibile reimpostare la consapevolezza DPI dell'intero processo. Questa operazione può essere attivata da:

1.  Una chiamata CreateWindow in cui l'oggetto passato nella finestra padre è di una modalità di riconoscimento DPI diversa rispetto al thread chiamante.
2.  Una chiamata SetParent in cui le due finestre sono associate a modalità di riconoscimento DPI diverse.

La tabella seguente mostra cosa accade se si tenta di violare questa regola:



| Operazione                 | Windows 8.1                                  | Windows 10 (1607 e versioni precedenti)                | Windows 10 (1703 e versioni successive)                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| CreateWindow (in-proc)    | N/A                                          | **Eredita l'elemento figlio** (modalità mista)              | **Eredita l'elemento figlio** (modalità mista)              |
| CreateWindow (cross-proc) | **Reimpostazione forzata** (del processo del chiamante)       | **Eredita l'elemento figlio** (modalità mista)              | **Reimpostazione forzata** (del processo del chiamante)       |
| SetParent (in-proc)       | N/A                                          | **Reimpostazione forzata** (del processo corrente)        | **Esito negativo** (ERRORE \_ STATO NON \_ VALIDO)             |
| SetParent (cross-proc)    | **Reimpostazione forzata** (del processo della finestra figlio) | **Reimpostazione forzata** (del processo della finestra figlio) | **Reimpostazione forzata** (del processo della finestra figlio) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulle API DPI elevate](high-dpi-reference.md)
</dt> <dt>

[Scalabilità DPI in modalità mista e API in grado di riconoscere DPI.](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

