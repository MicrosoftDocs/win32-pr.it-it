---
title: Uso di Input Method Editor in un gioco
description: Questo articolo illustra come implementare un controllo di modifica IME di base in un'applicazione Microsoft DirectX a schermo intero.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a119c5933aae14e2d3e45085dafa241a4dcb11e1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118676"
---
# <a name="using-an-input-method-editor-in-a-game"></a>Uso di Input Method Editor in un gioco

> [!Note]  
> Questo articolo illustra in dettaglio l'uso di Input Method Editor (IME) di Windows XP. Sono state apportate modifiche all'IME per Windows Vista che non sono completamente dettagliate in questo articolo. Per altre informazioni sulle modifiche apportate all'IME per Windows Vista, vedere [Input Method Editors (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in Windows Vista - An Ever-Expanding View of Internationalization (Input Method Editors (IME) in [Windows Vista - An Ever-Expanding View of Internationalization](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) (Editor dei metodi di input in Windows Vista - Visualizzazione Ever-Expanding dell'internazionalizzazione) nel portale Microsoft Global Development and Computing Portal.

 

Un input method editor (IME) è un programma che consente l'immissione di testo semplice usando una tastiera standard per le lingue dell'Asia orientale, ad esempio cinese, giapponese, coreano e altre lingue con caratteri complessi. Con gli IME, ad esempio, un utente può digitare caratteri complessi in un elaboratore di testo oppure un giocatore di un gioco online multiplayer di grandi quantità può chattare con amici in caratteri complessi.

Questo articolo illustra come implementare un controllo di modifica IME di base in un'applicazione Microsoft DirectX a schermo intero. Le applicazioni che sfruttano DXUT ottengono automaticamente la funzionalità IME. Per le applicazioni che non usano il framework, questo articolo descrive come aggiungere il supporto IME a un controllo di modifica.

Contenuto:

-   [Comportamento IME predefinito](#default-ime-behavior)
-   [Uso di IME con DXUT](#using-imes-with-dxut)
-   [Override del comportamento IME predefinito](#overriding-the-default-ime-behavior)
-   [Funzioni](#functions)
-   [Messaggi](#ime-messages)
-   [esempi](#examples)
    -   [CHT IME versione 4.2, 4.3 e 4.4](#cht-ime-version-42-43-and-44)
    -   [CHT IME versione 5.0](#cht-ime-version-50)
    -   [CHT IME versione 5.1, 5.2 e CHS IME versione 5.3](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [CHS IME versione 4.1](#chs-ime-version-41)
    -   [CHS IME versione 4.2](#chs-ime-version-42)
-   [Messaggi IME](#ime-messages)
    -   [WM \_ INPUTLANGCHANGE](#wm_inputlangchange)
    -   [WM \_ IME \_ STARTCOMPOSITION](/windows)
    -   [COMPOSIZIONE \_ IME WM \_](/windows)
    -   [WM \_ IME \_ ENDCOMPOSITION](/windows)
    -   [WM \_ IME \_ NOTIFY](/windows)
-   [Rendering](#rendering)
    -   [Indicatore delle impostazioni locali di input](#input-locale-indicator)
    -   [Finestra di composizione](#composition-window)
    -   [Lettura e finestre candidate](#reading-and-candidate-windows)
-   [Limitazioni](#limitations)
-   [Informazioni del Registro di sistema](#registry-information)
-   [Appendice A: Versioni CHT per sistema operativo](#appendix-a-cht-versions-per-operating-system)
-   [Altre informazioni](#further-information)
-   [GetReadingString](#getreadingstring)
-   [ShowReadingWindow](#showreadingwindow)

## <a name="default-ime-behavior"></a>Comportamento IME predefinito

Gli IME e mappano l'input della tastiera ai componenti fonetici o ad altri elementi del linguaggio specifici di una lingua selezionata. In uno scenario tipico, l'utente tipi di chiavi che rappresentano la pronuncia di un carattere complesso. Se l'IME riconosce la pronuncia come valida, presenta all'utente un elenco di candidati per parole o frasi da cui l'utente può selezionare una scelta finale. La parola scelta viene quindi inviata all'applicazione tramite una serie di messaggi [**CHAR WM \_ di**](/windows/desktop/inputdev/wm-char) Microsoft Windows. Poiché l'IME funziona a un livello inferiore all'applicazione intercettando l'input della tastiera, la presenza di un IME è trasparente per l'applicazione. Quasi tutte le applicazioni Windows possono immediatamente sfruttare gli IME senza essere consapevoli della loro esistenza e senza richiedere codice speciale.

Un IME tipico visualizza diverse finestre per guidare l'utente attraverso l'immissione di caratteri, come illustrato negli esempi seguenti.

![ime visualizza diverse finestre](images/ime-elements.png)

| Tipo di finestra                                       | Descrizione                                                                                                                                                                                                                                                                                                                 | IME Output                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| A. Finestra di lettura                                 | Contiene le sequenze di tasti della tastiera. in genere cambia dopo ogni pressione di tasto.                                                                                                                                                                                                                                              | lettura di una stringa                               |
| B. Finestra di composizione                             | Contiene la raccolta di caratteri che l'utente ha composto con l'IME. Questi caratteri vengono disegnati dall'IME sopra l'applicazione. Quando l'utente notifica all'IME che la stringa di composizione è soddisfacente, l'IME invia quindi la stringa di composizione all'applicazione tramite una serie di messaggi WM \_ CHAR. | stringa di composizione                           |
| C. Finestra Candidata                               | Quando l'utente ha immesso una pronuncia valida, l'IME visualizza un elenco di caratteri candidati che corrispondono tutti alla pronuncia specificata. L'utente seleziona quindi il carattere desiderato dall'elenco e l'IME lo aggiunge alla visualizzazione della finestra di composizione.                                                    | carattere successivo nella stringa di composizione |
| D. [Indicatore delle impostazioni locali di](/windows/desktop/Intl/nls-terminology) input | Mostra la lingua selezionata dall'utente per l'input da tastiera. Questo indicatore è incorporato nella barra delle applicazioni di Windows. Per selezionare la lingua di input, aprire opzioni internazionali e della lingua Pannello di controllo quindi fare clic su Dettagli nella scheda Lingue.                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a>Uso di IME con DXUT

In DXUT la classe CDXUTIMEEditBox implementa la funzionalità IME. Questa classe è derivata dalla classe CDXUTEditBox, il controllo di modifica di base fornito dal framework. CDXUTIMEEditBox estende il controllo di modifica per supportare gli IME eseguendo l'override dei metodi CDXUTIMEEditBox. Le classi sono progettate in questo modo per aiutare gli sviluppatori a capire cosa devono prendere dal framework per implementare il supporto IME nei propri controlli di modifica. Nella parte restante di questo argomento viene illustrato in che modo il framework, in particolare CDXUTIMEEditBox, esegue l'override di un controllo di modifica di base per implementare la funzionalità IME.

La maggior parte delle variabili specifiche di IME in CDXUTIMEEditBox viene dichiarata come statica, perché molti buffer e stati IME sono specifici del processo. Ad esempio, un processo ha un solo buffer per la stringa di composizione. Anche se il processo ha dieci controlli di modifica, condivideranno tutti lo stesso buffer della stringa di composizione. Il buffer della stringa di composizione per CDXUTIMEEditBox è pertanto statico, impedendo all'applicazione di occupare spazio di memoria non necessario.

CDXUTIMEEditBox viene implementato nel codice DXUT seguente:

(radice SDK) \\ Esempi \\ \\ \\ DXUTgui.cpp comuni C++

## <a name="overriding-the-default-ime-behavior"></a>Override del comportamento IME predefinito

In genere un IME usa procedure standard di Windows per creare una finestra (vedere [Uso di Windows).](/windows/desktop/winmsg/using-windows) In circostanze normali, ciò produce risultati soddisfacenti. Tuttavia, quando l'applicazione viene visualizzata in modalità schermo intero, come è comune per i giochi, le finestre standard non funzionano più e potrebbero non essere visualizzate sopra l'applicazione. Per risolvere questo problema, l'applicazione deve disegnare le finestre IME anziché basarsi su Windows per eseguire questa attività.

Quando il comportamento predefinito di creazione della finestra IME non fornisce ciò che un'applicazione richiede, l'applicazione può eseguire l'override della gestione della finestra IME. Un'applicazione può ottenere questo risultato elaborando i messaggi correlati all'IME e chiamando l'API [IMM (Input Method Manager).](/windows/desktop/Intl/input-method-manager)

Quando un utente interagisce con un IME per inserire caratteri complessi, invia messaggi all'applicazione per notificare eventi importanti, ad esempio l'avvio di una composizione o la visualizzazione della finestra candidata. Un'applicazione in genere ignora questi messaggi e li passa al gestore di messaggi predefinito, in modo che l'IME li gestirà. Quando l'applicazione, anziché il gestore predefinito, gestisce i messaggi, controlla esattamente ciò che accade in ogni evento IME. Spesso il gestore di messaggi recupera il contenuto delle varie finestre IME chiamando l'API IMM. Quando l'applicazione ha queste informazioni, può disegnare correttamente le finestre IME quando deve eseguire il rendering sullo schermo.

## <a name="functions"></a>Funzioni

Un IME deve ottenere la stringa di lettura, nascondere la finestra di lettura e ottenere l'orientamento della finestra di lettura. Questa tabella mostra le funzionalità per ogni versione IME:



|                    | Recupero della stringa di lettura                                                | Nascondere la finestra di lettura                       | Orientamento della finestra di lettura                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| **Prima della versione 6.0** | A. Lettura diretta dei dati privati IME di Accesso finestra. Vedere "4 Struttura" | Intercettare i messaggi privati IME. Vedere "3 messaggi" | Esaminare le informazioni del Registro di sistema. Vedere "5 Informazioni del Registro di sistema" |
| **Dopo la versione 6.0**  | [GetReadingString](#getreadingstring)                                 | [ShowReadingWindow](#showreadingwindow)     | [GetReadingString](#getreadingstring)                      |



 

## <a name="messages"></a>Messaggi

Non è necessario elaborare i messaggi seguenti per un IME più recente che implementa [ShowReadingWindow](#showreadingwindow)().

I messaggi seguenti vengono intercettati dal gestore di messaggi dell'applicazione(ad esempio, non vengono passati a DefWindowProc) per impedire la visualizzazione della finestra di lettura.

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano come ottenere informazioni di stringa da IME meno recenti che non hanno GetReadingString(). Il codice genera gli output seguenti:



| Output              | Descrizione                                                                                      |
|--------------|---------------------------------------------------------------------------------------|
| DWORD dwlen  | Lunghezza della stringa di lettura.                                                          |
| DWORD dwerr  | Indice del carattere di errore.                                                                   |
| LPWSTR wstr  | Puntatore alla stringa di lettura.                                                         |
| UNICODE BOOL | Se true, la stringa di lettura è in formato Unicode. In caso contrario, è in formato multibyte. |



 

### <a name="cht-ime-version-42-43-and-44"></a>CHT IME versione 4.2, 4.3 e 4.4

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a>CHT IME versione 5.0

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 3*4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4 + 4*2 );
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 + 1*4);
wstr = (WCHAR *)(p + 1*4 + (16*2+2*4) + 5*4);
unicode = FALSE;
```

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a>CHT IME versione 5.1, 5.2 e CHS IME versione 5.3

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 4);
if (!p) break;
p = *(LPBYTE *)((LPBYTE)p + 1*4 + 5*4); 
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * 2 + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = TRUE;
```

### <a name="chs-ime-version-41"></a>CHS IME versione 4.1

``` syntax
// GetImeId(1) returns VS_FIXEDFILEINFO:: dwProductVersionLS of IME file
int offset = ( GetImeId( 1 ) >= 0x00000002 ) ? 8 : 7;
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + offset * 4);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 16*2*4);
dwerr = *(DWORD *)(p + 8*4 + 16*2*4);
dwerr = min(dwerr, dwlen);
wstr = (WCHAR *)(p + 6*4 + 16*2*1);
unicode = TRUE;
```

### <a name="chs-ime-version-42"></a>CHS IME versione 4.2

``` syntax
int nTcharSize = IsNT() ? sizeof(WCHAR) : sizeof(char);
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
BYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 1*4 + 1*4 + 6*4);
if (!p) break;
dwlen = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize);
dwerr = *(DWORD *)(p + 1*4 + (16*2+2*4) + 5*4 + 16 * nTcharSize + 1*4);
wstr  = (WCHAR *) (p + 1*4 + (16*2+2*4) + 5*4);
unicode = IsNT() ? TRUE : FALSE;
```

## <a name="ime-messages"></a>Messaggi IME

Un'applicazione a schermo intero deve gestire correttamente i messaggi correlati all'IME seguenti:

### <a name="wm_inputlangchange"></a>WM \_ INPUTLANGCHANGE

IMM invia un messaggio WM INPUTLANGCHANGE alla finestra attiva di un'applicazione dopo che le impostazioni locali di input sono state modificate dall'utente con una combinazione di tasti (in genere ALT+MAIUSC) o con l'indicatore delle impostazioni locali di input sulla barra delle applicazioni o sulla barra della \_ lingua. La barra della lingua è un controllo su schermo con cui l'utente può configurare un servizio di testo. Vedere [Come visualizzare la barra della lingua.](/windows/desktop/TSF/how-to-set-up-tsf) La schermata seguente mostra un elenco di selezione della lingua che viene visualizzato quando l'utente fa clic sull'indicatore delle impostazioni locali.

![elenco di selezione della lingua visualizzato quando l'utente fa clic sull'indicatore delle impostazioni locali](images/ime-langselection.png)

Quando IMM invia un messaggio WM \_ INPUTLANGCHANGE, CDXUTIMEEditBox deve eseguire diverse attività importanti:

1.  Il metodo GetKeyboardLayout viene chiamato per restituire l'identificatore delle impostazioni locali di input (ID) per il thread dell'applicazione. La classe CDXUTIMEEditBox salva questo ID nella variabile membro statica s \_ hklCurrent per un uso successivo. È importante che l'applicazione sappia le impostazioni locali di input correnti, perché l'IME per ogni lingua ha un comportamento distinto. Lo sviluppatore potrebbe dover fornire codice diverso per impostazioni locali di input diverse.
2.  CDXUTIMEEditBox inizializza una stringa da visualizzare nell'indicatore di lingua della casella di modifica. Questo indicatore può visualizzare la lingua di input attiva quando l'applicazione è in esecuzione in modalità schermo intero e non è visibile né la barra delle applicazioni né la barra della lingua.
3.  Il metodo ImmGetConversionStatus viene chiamato per indicare se le impostazioni locali di input sono in modalità di conversione nativa o non nativa. La modalità di conversione nativa consente all'utente di immettere testo nella lingua scelta. La modalità di conversione non nativa fa in modo che la tastiera funzioni come tastiera inglese standard. È importante fornire all'utente un segnale visivo sul tipo di modalità di conversione in cui si trova l'IME, in modo che l'utente possa facilmente sapere quali caratteri aspettarsi quando si tocca un tasto. CDXUTIMEEditBox fornisce questo segnale visivo con un colore indicatore della lingua. Quando le impostazioni locali di input utilizzano un IME con modalità di conversione nativa, la classe CDXUTIMEEditBox disegna il testo dell'indicatore con il colore definito dal parametro \_ m IndicatorImeColor. Quando l'IME è in modalità di conversione non nativa o non viene usato alcun IME, la classe disegna il testo dell'indicatore con il colore definito dal parametro \_ m IndicatorEngColor.
4.  CDXUTIMEEditBox controlla le impostazioni locali di input e imposta la variabile membro statica bInsertOnType su TRUE per il coreano e \_ FALSE per tutte le altre lingue. Questo flag è obbligatorio a causa dei diversi comportamenti degli IME coreani e di tutti gli altri IME. Quando si immettono caratteri in lingue diverse dal coreano, il testo immesso dall'utente viene visualizzato nella finestra di composizione e l'utente può modificare liberamente il contenuto della stringa di composizione. L'utente preme il tasto INVIO quando viene soddisfatta la stringa di composizione e la stringa di composizione viene inviata all'applicazione come una serie di messaggi WM \_ CHAR. Negli IME coreani, tuttavia, quando un utente preme un tasto per immettere testo, viene immediatamente inviato un carattere all'applicazione. Quando successivamente l'utente preme più tasti per modificare il carattere iniziale, il carattere nella casella di modifica cambia per riflettere l'input aggiuntivo dell'utente. Essenzialmente, l'utente sta componendo caratteri nella casella di modifica. Questi due comportamenti sono sufficientemente diversi che CDXUTIMEEditBox deve codificare in modo specifico per ognuno di essi.
5.  Il metodo membro statico SetupImeApi viene chiamato per recuperare gli indirizzi di due funzioni dal modulo IME: GetReadingString e ShowReadingWindow. Se queste funzioni esistono, showReadingWindow viene chiamato per nascondere la finestra di lettura predefinita per questo IME. Poiché l'applicazione esegue il rendering della finestra di lettura stessa, notifica all'IME di disabilitare il disegno della finestra di lettura predefinita in modo che non interferisca con il rendering a schermo intero.

L'IMM invia un messaggio WM \_ IME \_ SETCONTEXT quando viene attivata una finestra dell'applicazione. Il parametro lParam di questo messaggio contiene un flag che indica all'IME quali finestre devono essere disegnate e quali no. Poiché l'applicazione gestisce tutto il disegno, non è necessario l'IME per disegnare le finestre IME. Pertanto, il gestore di messaggi dell'applicazione imposta semplicemente lParam su 0 e restituisce .

Per consentire alle applicazioni di supportare IME, è necessaria un'elaborazione speciale per il messaggio WM \_ IME SETCONTEXT correlato all'IME. \_ Poiché Windows in genere invia questo messaggio all'applicazione prima di chiamare il metodo PanoramaInitialize(), Panorama non ha la possibilità di elaborare l'interfaccia utente per visualizzare le finestre dell'elenco candidato.

Il frammento di codice seguente specifica alle applicazioni Windows di non visualizzare alcuna interfaccia utente associata alla finestra dell'elenco dei candidati, consentendo a Panorama di gestire in modo specifico questa interfaccia utente.

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a>AVVIO \_ DI WM \_ IMECOMPOSITION

L'IMM invia un messaggio WM IME STARTCOMPOSITION all'applicazione quando una composizione IME sta per iniziare in seguito a sequenze di tasti da parte \_ \_ dell'utente. Se l'IME usa la finestra di composizione, visualizza la stringa di composizione corrente in una finestra di composizione. CDXUTIMEEditBox gestisce questo messaggio eseguendo due attività:

1.  CDXUTIMEEditBox cancella il buffer della stringa di composizione e il buffer degli attributi. Questi buffer sono membri statici di CDXUTIMEEditBox.
2.  CDXUTIMEEditBox imposta la variabile membro \_ statica bHideCaret su TRUE. Questo membro, definito nella classe CDXUTEditBox di base, controlla se il cursore nella casella di modifica deve essere disegnato quando viene eseguito il rendering della casella di modifica. La finestra di composizione funziona in modo simile a una casella di modifica con testo e cursore. Per evitare confusione quando la finestra di composizione è visibile, la casella di modifica nasconde il cursore in modo che sia visibile un solo cursore alla volta.

### <a name="wm_ime_composition"></a>COMPOSIZIONE \_ IME \_ WM

L'IMM invia un messaggio WM IME COMPOSITION all'applicazione quando l'utente immette una sequenza di tasti \_ per modificare la stringa di \_ composizione. Il valore di lParam indica il tipo di informazioni che l'applicazione può recuperare da Input Method Manager (IMM). L'applicazione deve recuperare le informazioni disponibili chiamando [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) e quindi salvare le informazioni nel buffer privato in modo che possa eseguire il rendering degli elementi IME in un secondo momento.

CDXUTIMEEditBox verifica e recupera i dati della stringa di composizione seguenti:



| [**WM \_ Valore \_ del**](/windows/desktop/Intl/wm-ime-composition) flag IME COMPOSITION lParam | Dati                           | Descrizione                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GCS \_ COMPATTR                                                         | Attributo di composizione          | Questo attributo contiene informazioni quali lo stato di ogni carattere nella stringa di composizione, ad esempio convertito o non convertito. Queste informazioni sono necessarie perché CDXUTIMEEditBox colora i caratteri della stringa di composizione in modo diverso in base ai relativi attributi.                                                                                   |
| GCS \_ COMPCLAUSE                                                       | Informazioni sulla clausola composition | Queste informazioni sulla clausola vengono usate quando l'IME giapponese è attivo. Quando una stringa di composizione giapponese viene convertita, i caratteri possono essere raggruppati come clausola che viene convertita in una singola entità. Quando l'utente sposta il cursore, CDXUTIMEEditBox usa queste informazioni per evidenziare l'intera clausola, anziché un solo carattere all'interno della clausola . |
| GCS \_ COMPSTR                                                          | Stringa di composizione             | Questa stringa è la stringa aggiornata composta dall'utente. Questa è anche la stringa visualizzata nella finestra di composizione.                                                                                                                                                                                                                                        |
| GCS \_ CURSORPOS                                                        | Posizione del cursore di composizione    | La finestra di composizione implementa un cursore, simile al cursore in una casella di modifica. L'applicazione può recuperare la posizione del cursore durante l'elaborazione del messaggio WM \_ IME \_ COMPOSITION per disegnare correttamente il cursore.                                                                                                                                            |
| GCS \_ RESULTSTR                                                        | Stringa di risultato                  | La stringa di risultato è disponibile quando l'utente sta per completare il processo di composizione. Questa stringa deve essere recuperata e i caratteri devono essere inviati alla casella di modifica.                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a>\_ENDCOMPOSITION DI WM IME \_

L'IMM invia un messaggio ENDCOMPOSITION IME WM all'applicazione al termine dell'operazione di composizione \_ \_ IME. Ciò può verificarsi quando l'utente preme INVIO per approvare la stringa di composizione o il tasto ESC per annullare la composizione. CDXUTIMEEditBox gestisce questo messaggio impostando il buffer della stringa di composizione su vuoto. Imposta quindi s bHideCaret su FALSE perché la finestra di composizione è chiusa e il cursore nella casella di modifica \_ dovrebbe essere nuovamente visibile.

Il gestore di messaggi CDXUTIMEEditBox imposta anche \_ bShowReadingWindow su FALSE. Questo flag controlla se la classe disegna la finestra di lettura quando la casella di modifica esegue il rendering, quindi deve essere impostata su FALSE al termine di una composizione.

### <a name="wm_ime_notify"></a>NOTIFICA \_ IME \_ WM

L'IMM invia un messaggio WM \_ IME \_ NOTIFY all'applicazione ogni volta che cambia una finestra IME. Un'applicazione che gestisce il disegno delle finestre IME deve elaborare questo messaggio in modo che sia a conoscenza di qualsiasi aggiornamento al contenuto della finestra. wParam indica il comando o la modifica in corso. CDXUTIMEEditBox gestisce i comandi seguenti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Comando IME</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/Intl/imn-setopenstatus">IMN_SETOPENSTATUS</a></td>
<td>Questo attributo contiene informazioni quali lo stato di ogni carattere nella stringa di composizione, ad esempio convertito o non convertito. Queste informazioni sono necessarie perché CDXUTIMEEditBox colora i caratteri della stringa di composizione in modo diverso in base ai relativi attributi.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></td>
<td>Inviato all'applicazione quando la finestra candidata sta per essere aperta o aggiornata, rispettivamente. La finestra candidata si apre quando un utente vuole modificare la scelta del testo convertito. La finestra viene aggiornata quando un utente sposta l'indicatore di selezione o modifica la pagina. CDXUTIMEEditBox usa un gestore di messaggi per entrambi questi comandi perché le attività necessarie sono esattamente le stesse:<br/>
<ol>
<li>CDXUTIMEEditBox imposta il membro bShowWindow della struttura dell'elenco candidato s_CandList su TRUE per indicare che la finestra candidata deve essere disegnata durante il rendering dei frame.</li>
<li>CDXUTIMEEditBox recupera l'elenco di candidati chiamando <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, prima per ottenere le dimensioni del buffer necessarie e quindi di nuovo per ottenere i dati effettivi.</li>
<li>La struttura dell'elenco s_CandList candidato privato viene inizializzata con i dati candidati recuperati.</li>
<li>Le stringhe candidate vengono archiviate come matrice di stringhe.</li>
<li>L'indice della voce selezionata, nonché l'indice della pagina, viene salvato.</li>
<li>CDXUTIMEEditBox controlla se lo stile della finestra candidata è verticale o orizzontale. Se lo stile della finestra è orizzontale, è necessario inizializzare un buffer di stringhe aggiuntivo, il membro HoriCand di s_CandList, con tutte le stringhe candidate, con spazi inseriti tra tutte le stringhe adiacenti. Quando si esegue il rendering di una finestra candidata verticale, le singole stringhe candidate vengono disegnate una alla volta, con le coordinate y incrementate per ogni stringa. Tuttavia, questa stringa HoriCand deve essere usata durante il rendering di una finestra candidata orizzontale, perché lo spazio è il modo migliore per separare due stringhe adiacenti nella stessa riga.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></td>
<td>Inviato all'applicazione quando una finestra candidata sta per essere chiusa. Ciò si verifica quando un utente ha effettuato una selezione dall'elenco dei candidati. CDXUTIMEEditBox gestisce questo comando impostando il flag visibile della finestra candidata su FALSE e quindi cancellando il buffer della stringa candidata.</td>
</tr>
<tr class="even">
<td>IMN_PRIVATE</td>
<td>Inviato all'applicazione quando l'IME ha aggiornato la stringa di lettura in seguito alla digitazione o alla rimozione di caratteri da parte dell'utente. L'applicazione deve recuperare la stringa di lettura e salvarla per il rendering. CDXUTIMEEditBox dispone di due metodi per recuperare la stringa di lettura, in base al supporto della lettura delle stringhe nell'IME: <br/>
<ul>
<li>Se l'IME supporta la funzione GetReadingString, viene chiamato GetReadingString per recuperare la stringa di lettura.</li>
<li>Se l'IME non implementa GetReadingString, CDXUTIMEEditBox recupera la stringa di lettura dal contenuto del contesto di input.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a>Rendering

Il rendering degli elementi IME e delle finestre è semplice. CDXUTIMEEditBox consente alla classe di base di eseguire il rendering per primo perché le finestre IME devono essere visualizzate sopra il controllo di modifica. Dopo il rendering della casella di modifica di base, CDXUTIMEEditBox controlla il flag di visibilità di ogni finestra IME (indicatore, composizione, candidato e finestra di lettura) e disegna la finestra se deve essere visibile. Per le descrizioni dei diversi tipi di finestra IME, vedere Comportamento IME predefinito.

### <a name="input-locale-indicator"></a>Indicatore delle impostazioni locali di input

Il rendering dell'indicatore delle impostazioni locali di input viene eseguito prima di qualsiasi altra finestra IME perché è un elemento che viene sempre visualizzato. Dovrebbe quindi essere visualizzata sotto altre finestre IME. CDXUTIMEEditBox esegue il rendering dell'indicatore chiamando il metodo RenderIndicator, in cui il colore del carattere dell'indicatore viene determinato esaminando la variabile statica S ImeState, che riflette la modalità di \_ conversione IME corrente. Quando l'IME è abilitato e la conversione nativa è attiva, il metodo usa m \_ IndicatorImeColor come colore dell'indicatore. Se l'IME è disabilitato o è in modalità di conversione non nativa, m \_ IndicatorImeColor viene usato per disegnare il testo dell'indicatore. Per impostazione predefinita, la finestra dell'indicatore viene disegnata a destra della casella di modifica. Le applicazioni possono modificare questo comportamento eseguendo l'override del metodo RenderIndicator.

La figura seguente illustra i diversi aspetti di un indicatore delle impostazioni locali di input per l'inglese, il giapponese in modalità di conversione alfanumerica e il giapponese in modalità di conversione nativa:

![diversi aspetti di un indicatore delle impostazioni locali di input per l'inglese e il giapponese](images/ime-indicator.png)

### <a name="composition-window"></a>Finestra composizione

Il disegno della finestra di composizione viene gestito nel metodo RenderComposition di CDXUTIMEEditBox. La finestra di composizione è mobile sopra la casella di modifica. Deve essere disegnata in corrispondenza della posizione del cursore del controllo di modifica sottostante. CDXUTIMEEditBox gestisce il rendering come segue:

1.  L'intera stringa di composizione viene disegnata usando i colori predefiniti della stringa di composizione.
2.  I caratteri con determinati attributi speciali devono essere disegnati in colori diversi, quindi CDXUTIMEEditBox esamina i caratteri della stringa di composizione e controlla l'attributo stringa. Se l'attributo chiama colori diversi, il carattere viene disegnato di nuovo con i colori appropriati.
3.  Il cursore della finestra di composizione viene disegnato per completare il rendering.

Il cursore dovrebbe lampeggiare per gli IME coreani, ma non per altri IME. RenderComposition determina se il cursore deve essere visibile in base ai valori del timer quando viene usato l'IME coreano.

### <a name="reading-and-candidate-windows"></a>Lettura e finestre candidate

Il rendering delle finestre di lettura e candidate viene eseguito dallo stesso metodo CDXUTIMEEditBox, RenderCandidateReadingWindow. Entrambe le finestre contengono una matrice di stringhe per il layout verticale o una singola stringa nel caso del layout orizzontale. La maggior parte del codice in RenderCandidateReadingWindow viene usata per posizionare la finestra in modo che nessuna parte della finestra sia esterna alla finestra dell'applicazione e venga ritagliata.

## <a name="limitations"></a>Limitazioni

Gli IME contengono talvolta funzionalità avanzate per migliorare la facilità di immissione del testo. Alcune delle funzionalità disponibili negli IME più recenti sono illustrate nelle figure seguenti. Queste funzionalità avanzate non sono presenti in DXUT. L'implementazione del supporto per queste funzionalità avanzate può essere complessa perché non è definita alcuna interfaccia per ottenere le informazioni necessarie dagli IME.

IME cinese tradizionale avanzato con elenco di candidati espanso:

![ime cinese tradizionale avanzato con elenco di candidati espanso](images/ime-advanced1.png)

IME giapponese avanzato con alcune voci candidate che contengono testo aggiuntivo per descriverne il significato:

![ime giapponese avanzato con alcune voci candidate che contengono testo aggiuntivo per descriverne i significati](images/ime-advanced2.png)

IME coreano avanzato che include un sistema di riconoscimento della grafia:

![ime coreano avanzato che include un sistema di riconoscimento della grafia](images/ime-advanced3.png)

## <a name="registry-information"></a>Informazioni del Registro di sistema

Le informazioni del Registro di sistema seguenti vengono controllate per determinare l'orientamento della finestra di lettura, quando l'IME corrente è CHT New Phonetic meno recente che non implementa GetReadingString().



| Chiave                                                           | Valore            |
|---------------------------------------------------------------|------------------|
| HKCU \\ software \\ microsoft \\ windows \\ currentversion \\ IME \_ Name | mapping della tastiera |



 

Dove: Nome IME è MSTCIPH se la versione del file IME è 5.1 o successiva; in caso contrario, il nome \_ IME \_ è TINTLGNT.

L'orientamento della finestra di lettura è orizzontale se:

-   L'IME è versione 5.0 e il valore di mapping della tastiera 0x22 o 0x23
-   L'IME è versione 5.1 o versione 5.2 e il valore di mapping della tastiera è 0x22, 0x23 o 0x24.

Se nessuna delle due condizioni viene soddisfatta, la finestra di lettura è verticale.

## <a name="appendix-a-cht-versions-per-operating-system"></a>Appendice A: Versioni CHT per sistema operativo



| Sistema operativo           | Versione IME di CHT |
|----------------------------|-----------------|
| Windows 98                 | 4.2             |
| Windows 2000               | 4.3             |
| unknown                    | 4.4             |
| Windows ME                 | 5.0             |
| Office XP                  | 5,1             |
| Windows XP                 | 5,2             |
| Download web autonomo | 6.0             |



 

## <a name="further-information"></a>Altre informazioni

Per altre informazioni, vedere quanto segue:

-   [Installazione e uso di editor di metodi di input](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [Visualizzazione di testo internazionale](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [Consorzio Unicode](https://www.unicode.org/)
-   Sviluppo di software internazionale. Dr. International. 2° ed. Redmond, WA: Microsoft Press, 2003.

## <a name="getreadingstring"></a>GetReadingString

Ottiene la lettura delle informazioni sulla stringa.

**Parametri**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[nel \] contesto di input.

</dd> <dt>

<span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*
</dt> <dd>

\[in \] Lunghezza di lpwReadingBuf, in WCHAR. Se è zero, significa la lunghezza del buffer di lettura delle query.

</dd> <dt>

<span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf* 
</dt> <dd>

\[out \] Restituisce la stringa di lettura (non l'estremità zero).

</dd> <dt>

<span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex* 
</dt> <dd>

\[out \] Restituisce l'indice del carattere di errore nella stringa di lettura, se presente.

</dd> <dt>

<span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical* 
</dt> <dd>

\[out \] Se è TRUE, la lettura dell'interfaccia utente è verticale. In caso contrario, puMaxReadingLen orizzontale.

</dd> <dt>

<span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen* 
</dt> <dd>

\[out \] Lunghezza dell'interfaccia utente di lettura. La lunghezza massima di lettura non è fissa. dipende non solo dal layout di tastiera, ma anche dalla modalità di input (ad esempio, codice interno, input surrogato).

</dd> </dl>

**Valori restituiti**

Lunghezza della stringa di lettura.

**Osservazioni:**

Se il valore restituito è maggiore del valore di uReadingBufLen, tutti i parametri di output non sono definiti.

Questa funzione viene implementata in CHT IME 6.0 o versione successiva e può essere acquisita da GetProcAddress in un handle di modulo IME. L'handle del modulo IME può essere acquisito da ImmGetIMEFileName e LoadLibrary.

**Requisiti**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Intestazione**
</dt> <dd>

Dichiarato in Imm.h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Importa libreria**
</dt> <dd>

Usare Imm.lib.

</dd> </dl>

## <a name="showreadingwindow"></a>ShowReadingWindow

Mostra (o nascondi) la finestra di lettura.

**Parametri**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[nel \] contesto di input.

</dd> <dt>

<span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*Bshow* 
</dt> <dd>

\[in \] Imposta su TRUE per visualizzare la finestra di lettura (o FALSE per nasconderla).

</dd> </dl>

**Valori restituiti**

**Osservazioni:**

Restituisce TRUE se l'operazione ha esito positivo o FALSE in caso contrario.

**Requisiti**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Intestazione**
</dt> <dd>

Dichiarato in Imm.h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Importa libreria**
</dt> <dd>

Usare Imm.lib.

</dd> </dl>