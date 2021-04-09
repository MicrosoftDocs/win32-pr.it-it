---
title: Sviluppo di applicazioni desktop con DPI elevato in Windows
description: Questo contenuto è destinato agli sviluppatori che vogliono aggiornare le applicazioni desktop per gestire il fattore di scalabilità della visualizzazione dinamica (noto anche come
ms.assetid: 6C419EEF-D898-4B50-8D16-E65A594487AA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7af4a7a1d65077838dfa65f7cf89dee475a0b4dc
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104118595"
---
# <a name="high-dpi-desktop-application-development-on-windows"></a>Sviluppo di applicazioni desktop con DPI elevato in Windows

Questo contenuto è destinato agli sviluppatori che desiderano aggiornare le applicazioni desktop per gestire in modo dinamico il fattore di scalabilità di visualizzazione (punti per pollice o DPI), consentendo alle applicazioni di essere nitide in qualsiasi visualizzazione di cui viene eseguito il rendering.

Per iniziare, se si sta creando una nuova app di Windows da zero, è consigliabile creare un'applicazione [piattaforma UWP (Universal Windows Platform) (UWP)](/windows/uwp/get-started/whats-a-uwp) . Le applicazioni UWP vengono &mdash; ridimensionate automaticamente e in modo dinamico &mdash; per ogni visualizzazione su cui sono in esecuzione.

Le applicazioni desktop che usano le tecnologie di programmazione Windows precedenti (programmazione Win32 non elaborata, Windows Form, Windows Presentation Framework (WPF) e così via) non sono in grado di gestire automaticamente il ridimensionamento DPI senza ulteriori operazioni da parte degli sviluppatori. Senza questo tipo di lavoro, le applicazioni appariranno sfocate o ridimensionate in modo errato in molti scenari di utilizzo comuni. Questo documento fornisce il contesto e le informazioni relative all'aggiornamento di un'applicazione desktop per il rendering corretto.

## <a name="display-scale-factor--dpi"></a>Visualizzare il fattore di scala & DPI

Con l'avanzare della tecnologia di visualizzazione, i produttori del pannello di visualizzazione hanno compresso un numero crescente di pixel in ogni unità di spazio fisico nei rispettivi pannelli. Ciò ha comportato la presenza di punti per pollice (DPI) di pannelli di visualizzazione moderni molto più elevati rispetto a quelli precedenti. In passato, la maggior parte degli schermi aveva 96 pixel per ogni pollice lineare di spazio fisico (96 DPI); in 2017, le visualizzazioni con circa 300 DPI o versioni successive sono immediatamente disponibili.

La maggior parte dei Framework legacy dell'interfaccia utente desktop include presupposti incorporati che il valore DPI visualizzato non cambierà nel corso del processo.  Questo presupposto non è più valido, con la visualizzazione di dpi di solito modificate più volte durante la durata di un processo dell'applicazione. Di seguito sono riportati alcuni scenari comuni in cui le modifiche al fattore di scala/DPI di visualizzazione sono:

-   Configurazioni a più monitor in cui ogni schermo presenta un fattore di scala diverso e l'applicazione viene spostata da una visualizzazione all'altra (ad esempio, 4K e una visualizzazione 1080p)
-   Ancoraggio e disancoraggio di un computer portatile con DPI elevato con schermo esterno a DPI basso (o viceversa)
-   Connessione tramite Desktop remoto da un computer portatile/tablet a DPI elevato a un dispositivo a basso DPI (o viceversa)
-   Apportare modifiche alle impostazioni del fattore di scalabilità durante l'esecuzione delle applicazioni

In questi scenari, le applicazioni UWP si ritraggono automaticamente per il nuovo valore DPI. Per impostazione predefinita, e senza altre attività di sviluppo, le applicazioni desktop non lo eseguono. Le applicazioni desktop che non eseguono questo lavoro aggiuntivo per rispondere alle modifiche DPI possono apparire sfocate o ridimensionate in modo errato per l'utente.

## <a name="dpi-awareness-mode"></a>Modalità di riconoscimento DPI

Le applicazioni desktop devono indicare a Windows se supportano la scalabilità DPI. Per impostazione predefinita, il sistema considera le applicazioni desktop DPI incompatibili e bitmap-estende le finestre. Impostando una delle seguenti modalità di riconoscimento DPI disponibili, le applicazioni possono comunicare in modo esplicito a Windows come vogliono gestire il ridimensionamento DPI:

### <a name="dpi-unaware"></a>DPI non a conoscenza

Le applicazioni non compatibili con DPI eseguono il rendering con un valore DPI fisso di 96 (100%). Ogni volta che queste applicazioni vengono eseguite su una schermata con una scala di visualizzazione superiore a 96 DPI, Windows estenderà la bitmap dell'applicazione alla dimensione fisica prevista. In questo modo l'applicazione risulta sfocata.

### <a name="system-dpi-awareness"></a>Riconoscimento DPI sistema

Le applicazioni desktop che sono compatibili con i valori DPI del sistema ricevono in genere il valore DPI del monitoraggio connesso primario al momento dell'accesso dell'utente. Durante l'inizializzazione, il layout dell'interfaccia utente è appropriato, ovvero i controlli di ridimensionamento, la scelta delle dimensioni del carattere, il caricamento di asset e così via, usando tale valore DPI del sistema. Di conseguenza, le applicazioni compatibili con DPI di sistema non vengono ridimensionate in DPI (con estensione bitmap) da Windows su Visualizza il rendering in base a tale valore DPI singolo. Quando l'applicazione viene spostata in una visualizzazione con un fattore di scala diverso o se il fattore di scala di visualizzazione cambia in altro modo, Windows eseguirà la scalabilità delle finestre dell'applicazione, facendo in modo che risulti sfocata. In realtà, le applicazioni desktop compatibili con DPI di sistema eseguono il rendering in modo nitido a un singolo fattore di scala di visualizzazione, divenendo sfocate ogni volta che il DPI cambia.

### <a name="per-monitor-and-per-monitor-v2-dpi-awareness"></a>Riconoscimento DPI Per-Monitor e Per-Monitor (v2)

È consigliabile aggiornare le applicazioni desktop in modo da utilizzare la modalità di riconoscimento DPI per monitor, consentendo di eseguire immediatamente il rendering in modo corretto ogni volta che viene modificato il valore DPI. Quando un'applicazione segnala a Windows che vuole essere eseguita in questa modalità, Windows non consente di estendere l'applicazione quando viene modificato il valore DPI, inviando invece [WM \_ DPICHANGED](wm-dpichanged.md) alla finestra dell'applicazione. È quindi responsabilità completa dell'applicazione gestire il ridimensionamento per il nuovo valore DPI. La maggior parte dei framework dell'interfaccia utente usati dalle applicazioni desktop (controlli comuni di Windows (Comctl32), Windows Form, Windows Presentation Framework e così via) non supporta la scalabilità DPI automatica, che richiede agli sviluppatori di ridimensionare e riposizionare il contenuto delle proprie finestre.

Esistono due versioni di Per-Monitor consapevolezza che un'applicazione può registrarsi come: versione 1 e versione 2 (PMv2). La registrazione di un processo come in esecuzione in modalità di riconoscimento PMv2 comporta:

1.  L'applicazione a cui viene inviata una notifica quando viene modificato il valore DPI (sia gli HWND di primo livello che quelli figlio)
2.  Applicazione che Visualizza i pixel non elaborati di ogni visualizzazione
3.  L'applicazione non è mai stata ridimensionata in base alla bitmap di Windows
4.  Area non client automatica (didascalia della finestra, barre di scorrimento e così via) Ridimensionamento DPI per Windows
5.  Finestre di dialogo Win32 (da [CreateDialog](/windows/desktop/api/winuser/nf-winuser-createdialogw)) dpi automaticamente ridimensionate da Windows
6.  Asset bitmap disegnati con tema in controlli comuni (caselle di controllo, sfondi dei pulsanti e così via) sottoposti a rendering automatico con il fattore di scala DPI appropriato

Quando è in esecuzione in modalità di riconoscimento Per-Monitor V2, le applicazioni ricevono una notifica quando viene modificato il valore DPI. Se un'applicazione non si ridimensiona automaticamente per il nuovo valore DPI, l'interfaccia utente dell'applicazione apparirà troppo piccola o troppo grande (a seconda della differenza tra i valori DPI precedenti e nuovi).

> [!Note]  
> Il riconoscimento Per-Monitor V1 (PMv1) è molto limitato. È consigliabile usare PMv2 per le applicazioni.

Nella tabella seguente viene illustrato come verrà eseguito il rendering delle applicazioni in scenari diversi:

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
<th>Versione di Windows introdotta</th>
<th>Visualizzazione dell'applicazione di DPI</th>
<th>Comportamento sulla modifica DPI</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>A conoscenza</td>
<td>N/D</td>
<td>Tutti gli schermi sono 96 DPI</td>
<td>Adattamento bitmap (sfocatura)</td>
</tr>
<tr class="even">
<td>Sistema</td>
<td>Vista</td>
<td>Tutti gli schermi hanno lo stesso valore DPI (il valore DPI dello schermo principale al momento dell'avvio della sessione utente corrente)</td>
<td>Adattamento bitmap (sfocatura)</td>
</tr>
<tr class="odd">
<td>Per-Monitor</td>
<td>8.1</td>
<td>DPI della visualizzazione in cui si trova la finestra dell'applicazione</td>
<td><ul>
<li>HWND di primo livello riceve una notifica di modifica DPI</li>
<li>Nessuna scala DPI di alcun elemento dell'interfaccia utente.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Per-Monitor V2</td>
<td>Windows 10 Creators Update (1703)</td>
<td>DPI della visualizzazione in cui si trova la finestra dell'applicazione</td>
<td><ul>
<li>Gli HWND di primo livello <span class="underline">e</span> figlio ricevono una notifica di modifica dpi</li>
</ul>
<br/> <span class="underline">Ridimensionamento DPI automatico di:</span>
<ul>
<li>Area non client</li>
<li>Bitmap disegnate da temi nei controlli comuni (comctl32 v6)</li>
<li>Finestre di dialogo (<a href="/windows/desktop/api/winuser/nf-winuser-createdialogw">CreateDialog</a>)</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>

### <a name="per-monitor-v1-dpi-awareness"></a>Riconoscimento DPI per monitor (V1)

Con Windows 8.1 è stata introdotta la modalità di riconoscimento DPI Per-Monitor V1 (PMv1). Questa modalità di riconoscimento DPI è molto limitata e offre solo le funzionalità elencate di seguito. È consigliabile che le applicazioni desktop usino la modalità di riconoscimento Per-Monitor V2, supportata in Windows 10 1703 o versioni successive.

Il supporto iniziale per la consapevolezza per monitoraggio offre solo le applicazioni seguenti:

1.  Gli HWND di primo livello ricevono una notifica di modifica DPI e forniscono nuove dimensioni suggerite
2.  Non è possibile estendere l'interfaccia utente dell'applicazione con bitmap
3.  L'applicazione Visualizza tutte le visualizzazioni in pixel fisici (vedere virtualizzazione)

In Windows 10 1607 o versioni successive, le applicazioni PMv1 possono anche chiamare [EnableNonClientDpiScaling](/windows/desktop/api/winuser/nf-winuser-enablenonclientdpiscaling) durante WM \_ NCCREATE per richiedere che Windows ridimensioni correttamente l'area non client della finestra.

## <a name="per-monitor-dpi-scaling-support-by-ui-framework--technology"></a>Supporto del ridimensionamento DPI per monitor per interfaccia utente/Framework

La tabella seguente mostra il livello di supporto per la consapevolezza DPI per monitor offerto da diversi framework dell'interfaccia utente di Windows a partire da Windows 10 1703:

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
<td>Win32/controlli comuni non elaborati V6 (comctl32.dll)</td>
<td><ul>
<li>Messaggi di notifica delle modifiche DPI inviati a tutti gli HWND</li>
<li>Il rendering degli asset disegnati con tema è corretto nei controlli comuni</li>
<li>Ridimensionamento DPI automatico per le finestre di dialogo</li>
</ul></td>
<td>1703</td>
<td>Applicazione</td>
<td><a href="https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow">Esempio di GitHub</a></td>
</tr>
<tr class="odd">
<td>Windows Forms</td>
<td>Ridimensionamento automatico limitato per monitoraggio DPI per alcuni controlli</td>
<td>1703</td>
<td>Framework dell'interfaccia utente</td>
<td><a href="/dotnet/framework/winforms/high-dpi-support-in-windows-forms">Supporto di valori DPI alti in Windows Form</a></td>
</tr>
<tr class="even">
<td>Windows Presentation Framework (WPF)</td>
<td>Per le applicazioni WPF native la scalabilità DPI di WPF ospitata in altri Framework e altri Framework ospitati in WPF non vengono ridimensionati automaticamente</td>
<td>1607</td>
<td>Framework dell'interfaccia utente</td>
<td><a href="https://github.com/Microsoft/WPF-Samples/tree/master/PerMonitorDPI">Esempio di GitHub</a></td>
</tr>
<tr class="odd">
<td>GDI</td>
<td>nessuno</td>
<td>N/D</td>
<td>Applicazione</td>
<td>Vedere <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI scaling</a></td>
</tr>
<tr class="even">
<td>GDI+</td>
<td>nessuno</td>
<td>N/D</td>
<td>Applicazione</td>
<td>Vedere <a href="https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/">GDI High-DPI scaling</a></td>
</tr>
<tr class="odd">
<td>MFC</td>
<td>nessuno</td>
<td>N/D</td>
<td>Applicazione</td>
<td>N/D</td>
</tr>
</tbody>
</table>



 

## <a name="updating-existing-applications"></a>Aggiornamento di applicazioni esistenti

Per aggiornare un'applicazione desktop esistente per gestire correttamente la scalabilità DPI, è necessario aggiornarla in modo che, come minimo, le parti importanti della relativa interfaccia utente vengano aggiornate per rispondere alle modifiche DPI.

La maggior parte delle applicazioni desktop viene eseguita con la modalità di riconoscimento DPI del sistema. Le applicazioni compatibili con DPI di sistema in genere si adattano al valore DPI dello schermo principale (la visualizzazione in cui si trovava la barra di sistema al momento dell'avvio della sessione di Windows). Quando viene modificato il valore DPI, Windows eseguirà il ridimensionamento dell'interfaccia utente di queste applicazioni, il che spesso comporta la sfocatura. Quando si aggiorna un'applicazione compatibile con DPI di sistema in modo che sia compatibile con i valori DPI per monitor, il codice che gestisce il layout dell'interfaccia utente deve essere aggiornato in modo che venga eseguito non solo durante l'inizializzazione dell'applicazione, ma anche ogni volta che viene ricevuta una notifica di modifica DPI ([WM \_ DPICHANGED](wm-dpichanged.md) nel caso di Win32). Ciò comporta in genere la rivisitazione di qualsiasi presupposto nel codice che l'interfaccia utente deve essere ridimensionata una sola volta.

Inoltre, nel caso della programmazione Win32, molte API Win32 non dispongono di un valore DPI o di un contesto di visualizzazione in modo da restituire solo i valori relativi al valore DPI del sistema. Può essere utile grep nel codice per cercare alcune di queste API e sostituirle con varianti compatibili con DPI. Di seguito sono riportate alcune delle API comuni con varianti compatibili con DPI:



| Versione con DPI singolo   | Versione Per-Monitor        |
|----------------------|----------------------------|
| GetSystemMetrics     | GetSystemMetricsForDpi     |
| AdjustWindowRectEx   | AdjustWindowRectExForDpi   |
| SystemParametersInfo | SystemParametersInfoForDpi |
| GetDpiForMonitor     | GetDpiForWindow            |



 

È inoltre consigliabile eseguire la ricerca di dimensioni hardcoded nella codebase che presuppongono un valore DPI costante, sostituendo i valori con il codice che rappresenta correttamente la scalabilità DPI. Di seguito è riportato un esempio in cui sono incorporati tutti i suggerimenti seguenti:

### <a name="example"></a>Esempio:

Nell'esempio seguente viene illustrato un caso Win32 semplificato della creazione di un HWND figlio. La chiamata a CreateWindow presuppone che l'applicazione sia in esecuzione a 96 DPI e che la dimensione o la posizione del pulsante non sia corretta a una DPI superiore:


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

1.  Il codice di creazione della finestra DPI ridimensiona la posizione e le dimensioni dell'elemento HWND figlio per il valore DPI della finestra padre
2.  Risposta alle modifiche DPI tramite il riposizionamento e il ridimensionamento dell'HWND figlio
3.  Dimensioni hardcoded rimosse e sostituite con codice che risponde alle modifiche DPI


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



Quando si aggiorna un'applicazione compatibile con DPI di sistema, alcuni passaggi comuni sono i seguenti:

1.  Contrassegnare il processo come DPI compatibile con monitor (v2) usando un manifesto dell'applicazione (o un altro metodo, a seconda dei framework dell'interfaccia utente usati).
2.  Rendere la logica di layout dell'interfaccia utente riutilizzabile e spostarla all'esterno del codice di inizializzazione dell'applicazione in modo che possa essere riutilizzata quando si verifica una modifica DPI (WM \_ DPICHANGED nel caso della programmazione Windows (Win32)).
3.  Invalidare il codice che presuppone che i dati sensibili a DPI (DPI/Fonts/sizes/e così via) non debbano mai essere aggiornati. Si tratta di una procedura molto comune per memorizzare nella cache le dimensioni dei caratteri e i valori DPI durante l'inizializzazione del processo. Quando si aggiorna un'applicazione in modo che diventi compatibile con i DPI del monitor, è necessario rivalutare i dati sensibili a DPI ogni volta che viene rilevato un nuovo valore DPI.
4.  Quando si verifica una modifica del valore DPI, ricarica o rirasterizza le risorse bitmap per il nuovo valore DPI o, facoltativamente, la bitmap estende gli asset attualmente caricati alla dimensione corretta.
5.  Grep per le API che non sono Per-Monitor DPI in grado di riconoscere e sostituirle con Per-Monitor API compatibili con DPI (se applicabile). Esempio: sostituire GetSystemMetrics con GetSystemMetricsForDpi.
6.  Testare l'applicazione in un sistema a più visualizzazioni/multi-DPI.
7.  Per tutte le finestre di primo livello dell'applicazione che non è possibile aggiornare per la scalabilità DPI corretta, usare il ridimensionamento DPI in modalità mista (descritto di seguito) per consentire l'estensione bitmap di queste finestre di primo livello da parte del sistema.

## <a name="mixed-mode-dpi-scaling-sub-process-dpi-scaling"></a>Ridimensionamento DPI Mixed-Mode (ridimensionamento DPI del processo secondario)

Quando si aggiorna un'applicazione per supportare la consapevolezza DPI per monitor, può essere talvolta impraticabile o Impossibile aggiornare ogni finestra dell'applicazione in un'unica operazione. Questo può essere dovuto solo al tempo e al lavoro richiesto per l'aggiornamento e il test di tutte le interfacce utente o perché non si è proprietari di tutto il codice dell'interfaccia utente che è necessario eseguire (se l'applicazione potrebbe caricare l'interfaccia utente di terze parti). In queste situazioni, Windows offre un modo per semplificare il mondo della consapevolezza per monitoraggio consentendo di eseguire alcune delle finestre dell'applicazione (solo di primo livello) nella modalità di riconoscimento DPI originale, mentre si concentrano il tempo e l'energia nell'aggiornamento delle parti più importanti dell'interfaccia utente.

Di seguito è riportata un'illustrazione di questo aspetto: si aggiorna l'interfaccia utente principale dell'applicazione ("finestra principale" nell'illustrazione) per eseguire con la consapevolezza DPI per monitor mentre si eseguono altre finestre nella modalità esistente ("finestra secondaria").

![differenze nella scala dpi tra le modalità di riconoscimento](images/hub-page-illustrations.png)

Prima dell'aggiornamento dell'anniversario di Windows 10 (1607), la modalità di riconoscimento DPI di un processo era una proprietà a livello di processo. A partire dall'aggiornamento dell'anniversario di Windows 10, è ora possibile impostare questa proprietà per ogni finestra **di primo livello** . (Le finestre **figlio** devono continuare a corrispondere alle dimensioni di ridimensionamento dell'elemento padre). Una finestra di primo livello viene definita come una finestra senza elemento padre. Si tratta in genere di una finestra "regolare" con i pulsanti Riduci a icona, Ingrandisci e Chiudi. Lo scenario a cui è destinata la consapevolezza DPI del sottoprocesso è quello di avere un'interfaccia utente secondaria ridimensionata da Windows (con estensione bitmap), mentre è possibile concentrarsi sul tempo e sulle risorse per l'aggiornamento dell'interfaccia utente principale.

Per abilitare la consapevolezza DPI del sottoprocesso, chiamare [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) prima e dopo le chiamate di creazione di finestre. La finestra creata verrà associata alla consapevolezza DPI impostata tramite SetThreadDpiAwarenessContext. Utilizzare la seconda chiamata per ripristinare la consapevolezza DPI del thread corrente.

Quando si usa il ridimensionamento DPI del processo secondario, è possibile fare affidamento su Windows per eseguire alcune delle operazioni di scalabilità DPI per l'applicazione, che può aumentare la complessità dell'applicazione. È importante comprendere gli svantaggi di questo approccio e la natura delle complessità introdotte. Per altre informazioni sulla consapevolezza DPI del sottoprocesso, vedere [ridimensionamento DPI in modalità mista e API compatibili con dpi.](high-dpi-improvements-for-desktop-applications.md)

## <a name="testing-your-changes"></a>Test delle modifiche

Dopo aver aggiornato l'applicazione in modo che sia compatibile con i valori DPI per monitor, è importante convalidare l'applicazione in modo che risponda correttamente alle modifiche DPI in un ambiente con DPI misto. Di seguito sono riportate alcune specifiche da testare:

1.  Spostare le finestre delle applicazioni tra le visualizzazioni di valori DPI diversi
2.  Avvio dell'applicazione in visualizzazione di valori DPI diversi
3.  Modifica del fattore di scala per il monitoraggio durante l'esecuzione dell'applicazione
4.  Modifica della visualizzazione usata come schermo principale, _disconnettersi da Windows_, quindi eseguire nuovamente il test dell'applicazione dopo aver eseguito l'accesso. Questa operazione è particolarmente utile per trovare codice che usa dimensioni/dimensioni hardcoded.

## <a name="common-pitfalls-win32"></a>Insidie comuni (Win32)

**Non usare il rettangolo suggerito fornito in WM \_ DPICHANGED**

Quando Windows invia alla finestra dell'applicazione un messaggio [**WM \_ DPICHANGED**](wm-dpichanged.md) , questo messaggio include un rettangolo suggerito da usare per ridimensionare la finestra. È fondamentale che l'applicazione usi questo rettangolo per ridimensionarsi, in quanto:

1.  Verificare che il cursore del mouse si trovi nella stessa posizione relativa della finestra durante il trascinamento tra le visualizzazioni
2.  Impedire alla finestra dell'applicazione di entrare in un ciclo di modifica dpi ricorsivo in cui una modifica dpi attiva una modifica DPI successiva, che attiva ancora un'altra variazione DPI.

Se sono presenti requisiti specifici dell'applicazione che impediscono l'uso del rettangolo suggerito fornito da Windows nel messaggio WM \_ DPICHANGED, vedere [**WM \_ GETDPISCALEDSIZE**](wm-getdpiscaledsize.md). Questo messaggio può essere usato per assegnare a Windows una dimensione desiderata da usare una volta che si è verificata la modifica del valore DPI, evitando comunque i problemi descritti in precedenza.

**Mancanza di documentazione sulla virtualizzazione**

Quando un HWND o un processo viene eseguito come valore DPI incompatibile o compatibile con DPI di sistema, può essere bitmap esteso da Windows. Quando si verifica questa situazione, Windows ridimensiona e converte le informazioni sensibili a DPI da alcune API allo spazio delle coordinate del thread chiamante. Se, ad esempio, un thread con compatibilità con DPI esegue una query sulle dimensioni dello schermo mentre è in esecuzione in un display a DPI elevato, Windows virtualizza la risposta assegnata all'applicazione come se la schermata si trovasse in unità 96 DPI. In alternativa, quando un thread compatibile con DPI di sistema interagisce con una visualizzazione con un valore DPI diverso da quello in uso quando è stata avviata la sessione dell'utente corrente, in Windows verrà eseguita la scalabilità di alcune chiamate API nello spazio delle coordinate usato da HWND se era in esecuzione con il fattore di scala DPI originale.

Quando si aggiorna l'applicazione desktop alla scala DPI, può essere difficile capire quali chiamate API possono restituire valori virtualizzati in base al contesto del thread. Queste informazioni attualmente non sono sufficientemente documentate da Microsoft. Tenere presente che se si chiama qualsiasi API di sistema da un contesto del thread compatibile con DPI o con DPI, il valore restituito potrebbe essere virtualizzato. Pertanto, assicurarsi che il thread sia in esecuzione nel contesto DPI previsto quando si interagisce con lo schermo o con le singole finestre. Quando si modifica temporaneamente il contesto DPI di un thread usando [SetThreadDpiAwarenessContext](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext), assicurarsi di ripristinare il contesto precedente al termine dell'operazione per evitare di causare un comportamento errato in un'altra posizione nell'applicazione.

**Molte API Windows non dispongono di un contesto DPI**

Molte API Windows legacy non includono un contesto DPI o HWND come parte dell'interfaccia. Di conseguenza, gli sviluppatori devono spesso eseguire ulteriori operazioni per gestire il ridimensionamento di qualsiasi informazione sensibile a DPI, ad esempio dimensioni, punti o icone. Gli sviluppatori che usano [LoadIcon](/windows/desktop/api/winuser/nf-winuser-loadiconw) , ad esempio, devono avere icone con estensione bitmap caricate o usare API alternative per caricare icone di dimensioni corrette per il valore dpi appropriato, ad esempio [LoadImage](/windows/desktop/api/winuser/nf-winuser-loadimagew).

**Ripristino forzato della consapevolezza DPI a livello di processo**

In generale, la modalità di riconoscimento DPI del processo non può essere modificata dopo l'inizializzazione del processo. Windows può, tuttavia, modificare forzatamente la modalità di riconoscimento DPI del processo se si tenta di interrompere il requisito in cui tutti gli HWND in una struttura ad albero della finestra hanno la stessa modalità di riconoscimento DPI. In tutte le versioni di Windows, a partire da Windows 10 1703, non è possibile avere HWND diversi in una struttura ad albero HWND eseguita in modalità di riconoscimento DPI diverse. Se si tenta di creare una relazione padre-figlio che interrompe questa regola, è possibile reimpostare la consapevolezza DPI dell'intero processo. Questa operazione può essere attivata da:

1.  Chiamata CreateWindow in cui la finestra padre passata è di una modalità di riconoscimento DPI diversa rispetto al thread chiamante.
2.  Una chiamata a padre dove le due finestre sono associate a diverse modalità di riconoscimento DPI.

La tabella seguente mostra cosa accade se si tenta di violare questa regola:



| Operazione                 | Windows 8.1                                  | Windows 10 (1607 e versioni precedenti)                | Windows 10 (1703 e versioni successive)                  |
|---------------------------|----------------------------------------------|----------------------------------------------|----------------------------------------------|
| CreateWindow (in-process)    | N/D                                          | **Eredita figlio** (modalità mista)              | **Eredita figlio** (modalità mista)              |
| CreateWindow (cross-process) | **Reimpostazione forzata** (del processo del chiamante)       | **Eredita figlio** (modalità mista)              | **Reimpostazione forzata** (del processo del chiamante)       |
| Padre (in-process)       | N/D                                          | **Reimpostazione forzata** (del processo corrente)        | **Esito negativo** (errore \_ stato non valido \_ )             |
| Padre (cross-process)    | **Reimpostazione forzata** (del processo della finestra figlio) | **Reimpostazione forzata** (del processo della finestra figlio) | **Reimpostazione forzata** (del processo della finestra figlio) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento all'API DPI elevato](high-dpi-reference.md)
</dt> <dt>

[Ridimensionamento DPI in modalità mista e API compatibili con DPI.](high-dpi-improvements-for-desktop-applications.md)
</dt> </dl>

