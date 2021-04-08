---
title: Uso di un editor del metodo di input in un gioco
description: In questo articolo viene illustrato come implementare un controllo di base di modifica IME in un'applicazione Microsoft DirectX a schermo intero.
ms.assetid: 760ed960-08a3-e967-282e-7fbdbaeb7a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1519f07a4e105ae822bd13fd7acd8b29e5ad8a0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "103969282"
---
# <a name="using-an-input-method-editor-in-a-game"></a>Uso di un editor del metodo di input in un gioco

> [!Note]  
> Questo articolo descrive in dettaglio l'uso dell'IME (Input Method Editor) di Windows XP. Sono state apportate modifiche all'IME per Windows Vista che non sono completamente descritte in questo articolo. Per ulteriori informazioni sulle modifiche apportate all'IME per Windows Vista, vedere [Input Method Editor (IME)](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx#e4eac) in [Windows vista: una Ever-Expanding visualizzazione dell'internazionalizzazione](https://www.microsoft.com/globaldev/vista/Whats_New_Vista.mspx) nel portale Microsoft per lo sviluppo e l'elaborazione globale.

 

Un Input Method Editor (IME) è un programma che consente una voce di testo semplice utilizzando una tastiera standard per le lingue asiatiche orientali, come il cinese, il giapponese, il coreano e altri linguaggi con caratteri complessi. Con gli IME, ad esempio, un utente può digitare caratteri complessi in un elaboratore di testo o un giocatore di un gioco multiplayer online massive può chattare con amici in caratteri complessi.

In questo articolo viene illustrato come implementare un controllo di base di modifica IME in un'applicazione Microsoft DirectX a schermo intero. Le applicazioni che sfruttano i vantaggi di DXUT ottengono automaticamente la funzionalità IME. Per le applicazioni che non usano il Framework, in questo articolo viene descritto come aggiungere il supporto IME a un controllo di modifica.

Contenuto:

-   [Comportamento IME predefinito](#default-ime-behavior)
-   [Uso di IME con DXUT](#using-imes-with-dxut)
-   [Override del comportamento predefinito di IME](#overriding-the-default-ime-behavior)
-   [Funzioni](#functions)
-   [Messaggi](#ime-messages)
-   [esempi](#examples)
    -   [CHT IME versione 4,2, 4,3 e 4,4](#cht-ime-version-42-43-and-44)
    -   [CHT IME versione 5,0](#cht-ime-version-50)
    -   [CHT IME versione 5,1, 5,2 e CHS versione 5,3](#cht-ime-version-51-52-and-chs-ime-version-53)
    -   [CHS IME versione 4,1](#chs-ime-version-41)
    -   [CHS IME versione 4,2](#chs-ime-version-42)
-   [Messaggi IME](#ime-messages)
    -   [\_INPUTLANGCHANGE WM](#wm_inputlangchange)
    -   [\_STARTCOMPOSITION IME \_ WM](/windows)
    -   [\_composizione IME \_ WM](/windows)
    -   [\_ENDCOMPOSITION IME \_ WM](/windows)
    -   [\_notifica IME \_ WM](/windows)
-   [Rendering](#rendering)
    -   [Indicatore impostazioni locali di input](#input-locale-indicator)
    -   [Finestra di composizione](#composition-window)
    -   [Lettura e finestre candidate](#reading-and-candidate-windows)
-   [Limitazioni](#limitations)
-   [Informazioni registro di sistema](#registry-information)
-   [Appendice A: versioni CHT per sistema operativo](#appendix-a-cht-versions-per-operating-system)
-   [Altre informazioni](#further-information)
-   [GetReadingString](#getreadingstring)
-   [ShowReadingWindow](#showreadingwindow)

## <a name="default-ime-behavior"></a>Comportamento IME predefinito

Gli IME mappano l'input da tastiera a componenti fonetici o altri elementi di linguaggio specifici di una lingua selezionata. In uno scenario tipico, l'utente digita le chiavi che rappresentano la pronuncia di un carattere complesso. Se l'IME riconosce la pronuncia come valida, presenta all'utente un elenco di candidati Word o phrase da cui l'utente può selezionare una scelta finale. La parola scelta viene quindi inviata all'applicazione tramite una serie di messaggi di Microsoft Windows [**WM \_ char**](/windows/desktop/inputdev/wm-char) . Poiché l'IME funziona a un livello al di sotto dell'applicazione intercettando l'input da tastiera, la presenza di un IME è trasparente per l'applicazione. Quasi tutte le applicazioni Windows possono sfruttare immediatamente gli IME senza essere consapevoli della loro esistenza e senza la necessità di scrivere codice speciale.

Un IME tipico Visualizza diverse finestre per guidare l'utente attraverso la voce di carattere, come illustrato negli esempi seguenti.

![IME Visualizza diverse finestre](images/ime-elements.png)

| Tipo di finestra                                       | Descrizione                                                                                                                                                                                                                                                                                                                 | Output IME                                   |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| R. Lettura della finestra                                 | Contiene le sequenze di tasti della tastiera; in genere viene modificato dopo ogni pressione di tasto.                                                                                                                                                                                                                                              | lettura stringa                               |
| B. Finestra di composizione                             | Contiene la raccolta di caratteri che l'utente ha composto con l'IME. Questi caratteri vengono disegnati dall'IME all'inizio dell'applicazione. Quando l'utente informa l'IME che la stringa di composizione è soddisfacente, l'IME invia la stringa di composizione all'applicazione tramite una serie di messaggi WM \_ Char. | stringa di composizione                           |
| C. Finestra candidata                               | Quando l'utente ha immesso una pronuncia valida, l'IME Visualizza un elenco di caratteri candidati che corrispondono alla pronuncia specificata. L'utente seleziona quindi il carattere desiderato da questo elenco e l'IME aggiunge questo carattere alla visualizzazione della finestra di composizione.                                                    | carattere successivo nella stringa di composizione |
| D. Indicatore [impostazioni locali di input](/windows/desktop/Intl/nls-terminology) | Mostra la lingua selezionata dall'utente per l'input da tastiera. Questo indicatore è incorporato nella barra delle applicazioni di Windows. È possibile selezionare la lingua di input aprendo il pannello di controllo Opzioni internazionali e della lingua e quindi facendo clic su dettagli nella scheda lingue.                                                               | \-                                           |



 

## <a name="using-imes-with-dxut"></a>Uso di IME con DXUT

In DXUT la classe CDXUTIMEEditBox implementa la funzionalità IME. Questa classe è derivata dalla classe CDXUTEditBox, il controllo di base di modifica fornito dal Framework. CDXUTIMEEditBox estende il controllo di modifica per supportare gli IME eseguendo l'override dei metodi CDXUTIMEEditBox. Queste classi sono progettate in modo da consentire agli sviluppatori di apprendere gli elementi necessari dal Framework per implementare il supporto IME nei propri controlli di modifica. Nella parte restante di questo argomento viene illustrato come, in particolare, il Framework e CDXUTIMEEditBox esegue l'override di un controllo di modifica di base per implementare la funzionalità IME.

La maggior parte delle variabili specifiche di IME in CDXUTIMEEditBox viene dichiarata come statica, perché molti buffer e Stati IME sono specifici del processo. Un processo, ad esempio, dispone di un solo buffer per la stringa di composizione. Anche se il processo ha dieci controlli di modifica, tutti condivideranno lo stesso buffer di stringhe di composizione. Il buffer della stringa di composizione per CDXUTIMEEditBox è pertanto statico e impedisce all'applicazione di occupare spazio di memoria superfluo.

CDXUTIMEEditBox viene implementato nel codice DXUT seguente:

(Radice SDK) \\ Esempi \\ comuni di C++ \\ \\ DXUTgui. cpp

## <a name="overriding-the-default-ime-behavior"></a>Override del comportamento predefinito di IME

In genere, un IME usa le procedure standard di Windows per creare una finestra (vedere [uso di Windows](/windows/desktop/winmsg/using-windows)). In circostanze normali, questo produce risultati soddisfacenti. Tuttavia, quando l'applicazione presenta la modalità schermo intero, come avviene in genere per i giochi, le finestre standard non funzionano più e potrebbero non essere visualizzate sopra l'applicazione. Per ovviare a questo problema, l'applicazione deve creare le finestre IME anziché basarsi su Windows per eseguire questa attività.

Quando il comportamento predefinito della creazione della finestra IME non fornisce ciò che un'applicazione richiede, l'applicazione può eseguire l'override della gestione della finestra IME. Per ottenere questo risultato, un'applicazione può elaborare i messaggi relativi a IME e chiamare l'API di [Input Method Manager](/windows/desktop/Intl/input-method-manager) (IMM).

Quando un utente interagisce con un IME per inserire caratteri complessi, IMM invia messaggi all'applicazione per notificare gli eventi importanti, ad esempio l'avvio di una composizione o la visualizzazione della finestra candidata. Un'applicazione in genere ignora questi messaggi e li passa al gestore di messaggi predefinito, che ne determina la gestione da parte dell'IME. Quando l'applicazione, anziché il gestore predefinito, gestisce i messaggi, controlla esattamente cosa accade in ogni evento IME. Spesso il gestore di messaggi Recupera il contenuto delle varie finestre IME chiamando l'API IMM. Una volta fornite queste informazioni, l'applicazione può disegnare correttamente le finestre IME quando è necessario eseguirne il rendering sullo schermo.

## <a name="functions"></a>Funzioni

È necessario che un IME ottenga la stringa di lettura, nasconda la finestra di lettura e ottenga l'orientamento della finestra di lettura. Questa tabella mostra le funzionalità per ogni versione di IME:



|                    | Recupero della stringa di lettura                                                | Nascondere la finestra di lettura                       | Orientamento della finestra di lettura                              |
|--------------------|-----------------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------|
| Prima della versione 6,0 | R. Lettura diretta dei dati di accesso alla finestra IME privata. Vedere "4 struttura" | Trap messaggi privati IME. Vedere "3 messaggi" | Esaminare le informazioni del registro di sistema. Vedere "5 informazioni sul Registro di sistema" |
| Dopo la versione 6,0  | [GetReadingString](#getreadingstring)                                 | [ShowReadingWindow](#showreadingwindow)     | [GetReadingString](#getreadingstring)                      |



 

## <a name="messages"></a>Messaggi

I messaggi seguenti non devono essere elaborati per l'IME più recente che implementa [ShowReadingWindow](#showreadingwindow)().

I messaggi seguenti sono intercettati dal gestore di messaggi dell'applicazione, ovvero non vengono passati a DefWindowProc, per impedire la visualizzazione della finestra di lettura.

``` syntax
Msg == WM_IME_NOTIFY
wParam == IMN_PRIVATE
lParam == 1, 2 (CHT IME version 4.2, 4.3 and 4.4 / CHS IME 4.1 and 4.2)
lParam == 16, 17, 26, 27, 28 (CHT IME version 5.0, 5.1, 5.2 / CHS IME 5.3)
```

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato come ottenere informazioni sulla stringa da un IME precedente che non dispone di GetReadingString (). Il codice genera gli output seguenti:



|              |                                                                                       |
|--------------|---------------------------------------------------------------------------------------|
| Dwlen DWORD  | Lunghezza della stringa di lettura                                                          |
| Dwerr DWORD  | Indice del carattere di errore                                                                   |
| WSTR LPWSTR  | Puntatore alla stringa di lettura                                                         |
| BOOL Unicode | Se true, la stringa di lettura è in formato Unicode. In caso contrario, è in formato multibyte. |



 

### <a name="cht-ime-version-42-43-and-44"></a>CHT IME versione 4,2, 4,3 e 4,4

``` syntax
LPINPUTCONTEXT lpIMC = _ImmLockIMC(himc);
LPBYTE p = *(LPBYTE *)((LPBYTE)_ImmLockIMCC(lpIMC->hPrivate) + 24);
if (!p) break;
dwlen = *(DWORD *)(p + 7*4 + 32*4);
dwerr = *(DWORD *)(p + 8*4 + 32*4);
wstr = (WCHAR *)(p + 56);
unicode = TRUE;
```

### <a name="cht-ime-version-50"></a>CHT IME versione 5,0

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

### <a name="cht-ime-version-51-52-and-chs-ime-version-53"></a>CHT IME versione 5,1, 5,2 e CHS versione 5,3

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

### <a name="chs-ime-version-41"></a>CHS IME versione 4,1

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

### <a name="chs-ime-version-42"></a>CHS IME versione 4,2

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

Un'applicazione a schermo intero deve gestire correttamente i messaggi relativi a IME seguenti:

### <a name="wm_inputlangchange"></a>\_INPUTLANGCHANGE WM

IMM Invia un messaggio WM \_ INPUTLANGCHANGE alla finestra attiva di un'applicazione dopo che l'utente ha modificato le impostazioni locali di input con una combinazione di tasti (in genere Alt + Maiusc) o con l'indicatore delle impostazioni locali di input sulla barra delle applicazioni o sulla barra della lingua. La barra del linguaggio è un controllo su schermo con il quale l'utente può configurare un servizio di testo. Vedere [come visualizzare la barra della lingua](/windows/desktop/TSF/how-to-set-up-tsf). Lo screenshot seguente mostra un elenco di selezione della lingua che viene visualizzato quando l'utente fa clic sull'indicatore delle impostazioni locali.

![elenco di selezione della lingua visualizzato quando l'utente fa clic sull'indicatore delle impostazioni locali](images/ime-langselection.png)

Quando IMM Invia un messaggio WM \_ INPUTLANGCHANGE, CDXUTIMEEditBox deve eseguire diverse attività importanti:

1.  Il metodo GetKeyboardLayout viene chiamato per restituire l'identificatore delle impostazioni locali di input (ID) per il thread dell'applicazione. La classe CDXUTIMEEditBox Salva questo ID nelle variabili membro statiche s \_ hklCurrent per un uso successivo. È importante che l'applicazione conosca le impostazioni locali di input correnti, perché l'IME per ogni lingua presenta un proprio comportamento distinto. Lo sviluppatore potrebbe dover fornire codice diverso per le diverse impostazioni locali di input.
2.  CDXUTIMEEditBox Inizializza una stringa da visualizzare nell'indicatore della lingua della casella di modifica. Questo indicatore può visualizzare la lingua di input attiva quando l'applicazione è in esecuzione in modalità a schermo intero e non è visibile né la barra delle applicazioni né la barra della lingua.
3.  Il metodo ImmGetConversionStatus viene chiamato per indicare se le impostazioni locali di input sono in modalità di conversione nativa o non nativa. La modalità di conversione nativa consente all'utente di immettere testo nella lingua scelta. La modalità di conversione non nativa fa in modo che la tastiera funga da tastiera inglese standard. È importante fornire all'utente un segnale visivo per il tipo di modalità di conversione in cui si trova l'IME, in modo che l'utente possa facilmente sapere quali sono i caratteri da prevedere quando si preme un tasto. CDXUTIMEEditBox fornisce questo segnale visivo con un colore dell'indicatore di lingua. Quando le impostazioni locali di input usano un IME con la modalità di conversione nativa, la classe CDXUTIMEEditBox disegna il testo dell'indicatore con il colore definito dal \_ parametro m IndicatorImeColor. Quando l'IME si trova in modalità di conversione non nativa oppure non viene utilizzato alcun IME, la classe disegna il testo dell'indicatore con il colore definito dal parametro m \_ IndicatorEngColor.
4.  CDXUTIMEEditBox controlla le impostazioni locali di input e imposta la variabile membro statica s \_ bInsertOnType su true per il coreano e false per tutte le altre lingue. Questo flag è obbligatorio a causa dei diversi comportamenti degli IME coreano e di tutti gli altri IME. Quando si immettono caratteri in lingue diverse dal coreano, il testo immesso dall'utente viene visualizzato nella finestra di composizione e l'utente può modificare liberamente il contenuto della stringa di composizione. L'utente preme il tasto INVIO quando è soddisfatto dalla stringa di composizione e la stringa di composizione viene inviata all'applicazione come una serie di messaggi WM \_ Char. Negli IME coreano, tuttavia, quando un utente preme un tasto per immettere il testo, un carattere viene immediatamente inviato all'applicazione. Quando l'utente preme successivamente più tasti per modificare il carattere iniziale, il carattere nella casella di modifica viene modificato in modo da riflettere l'input aggiuntivo da parte dell'utente. In sostanza, l'utente sta componendo i caratteri nella casella di modifica. Questi due comportamenti sono abbastanza diversi da consentire a CDXUTIMEEditBox di scrivere codice per ognuno di essi in modo specifico.
5.  Il metodo del membro statico SetupImeApi viene chiamato per recuperare gli indirizzi di due funzioni dal modulo IME: GetReadingString e ShowReadingWindow. Se queste funzioni esistono, viene chiamato ShowReadingWindow per nascondere la finestra di lettura predefinita per questo IME. Poiché l'applicazione esegue il rendering della finestra di lettura, viene inviata una notifica all'IME per disabilitare il disegno della finestra di lettura predefinita in modo che non interferisca con il rendering a schermo intero.

IMM Invia un \_ \_ messaggio di contestuale di WM IME quando viene attivata una finestra dell'applicazione. Il parametro lParam di questo messaggio contiene un flag che indica all'IME quali finestre devono essere disegnate e quali no. Poiché l'applicazione gestisce tutto il disegno, non è necessario che l'IME disegni le finestre IME. Il gestore di messaggi dell'applicazione, pertanto, imposta semplicemente lParam su 0 e restituisce.

Per consentire alle applicazioni di supportare l'IME, è necessaria un'elaborazione speciale per il messaggio relativo al contesto IME di WM per il messaggio correlato a IME \_ \_ . Poiché Windows in genere invia questo messaggio all'applicazione prima di chiamare il metodo PanoramaInitialize (), panorama non ha la possibilità di elaborare l'interfaccia utente per visualizzare le finestre di elenco dei candidati.

Il frammento di codice seguente specifica alle applicazioni Windows di non visualizzare alcuna interfaccia utente associata alla finestra elenco candidati, consentendo a Panorama di gestire questa interfaccia utente in modo specifico.

``` syntax
case WM_IME_SETCONTEXT:
         lParam = 0;
    lRet = DefWindowProc(hWnd, msg, wParam, lParam);
    break;
    //... more message processing
    return lRet;
```

### <a name="wm_ime_startcomposition"></a>\_STARTCOMPOSITION IME \_ WM

IMM Invia un \_ \_ messaggio STARTCOMPOSITION di WM IME all'applicazione quando una composizione IME sta per iniziare in seguito a sequenze di tasti da parte dell'utente. Se l'IME usa la finestra di composizione, Visualizza la stringa di composizione corrente in una finestra di composizione. CDXUTIMEEditBox gestisce questo messaggio eseguendo due attività:

1.  CDXUTIMEEditBox Cancella il buffer della stringa di composizione e il buffer dell'attributo. Questi buffer sono membri statici di CDXUTIMEEditBox.
2.  CDXUTIMEEditBox imposta la \_ variabile membro statico s bHideCaret su true. Questo membro, definito nella classe di base CDXUTEditBox, determina se il cursore nella casella di modifica deve essere disegnato quando viene eseguito il rendering della casella di modifica. La finestra di composizione funziona in modo analogo a una casella di modifica con testo e cursore. Per evitare confusione quando la finestra di composizione è visibile, la casella di modifica nasconde il cursore in modo che sia visibile solo un cursore alla volta.

### <a name="wm_ime_composition"></a>\_composizione IME \_ WM

IMM Invia un \_ \_ messaggio di composizione IME WM all'applicazione quando l'utente immette una sequenza di tasti per modificare la stringa di composizione. Il valore di lParam indica il tipo di informazioni che l'applicazione può recuperare da input Method Manager (IMM). L'applicazione deve recuperare le informazioni disponibili chiamando [**ImmGetCompositionString**](/windows/desktop/api/imm/nf-imm-immgetcompositionstringa) e quindi salvare le informazioni nel buffer privato in modo che sia in grado di eseguire il rendering degli elementi IME in un secondo momento.

CDXUTIMEEditBox verifica e recupera i dati di stringa di composizione seguenti:



| [**WM \_ Valore \_**](/windows/desktop/Intl/wm-ime-composition) del flag lParam composizione IME | Data                           | Descrizione                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| comaccarezzatore cataloghi globali \_                                                         | Attributo Composition          | Questo attributo contiene informazioni quali lo stato di ogni carattere nella stringa di composizione (ad esempio, convertito o non convertito). Queste informazioni sono necessarie perché CDXUTIMEEditBox colora i caratteri della stringa di composizione in modo diverso in base ai rispettivi attributi.                                                                                   |
| COMPCLAUSE cataloghi globali \_                                                       | Informazioni sulla clausola di composizione | Le informazioni sulla clausola vengono utilizzate quando l'IME giapponese è attivo. Quando viene convertita una stringa di composizione giapponese, i caratteri possono essere raggruppati come una clausola che viene convertita in una singola entità. Quando l'utente sposta il cursore, CDXUTIMEEditBox usa queste informazioni per evidenziare l'intera clausola, anziché un solo carattere nella clausola. |
| COMPSTR cataloghi globali \_                                                          | Stringa di composizione             | Questa stringa è la stringa aggiornata composta dall'utente. Si tratta anche della stringa visualizzata nella finestra di composizione.                                                                                                                                                                                                                                        |
| CURSORPOS cataloghi globali \_                                                        | Posizione del cursore di composizione    | La finestra di composizione implementa un cursore, simile al cursore in una casella di modifica. L'applicazione può recuperare la posizione del cursore durante l'elaborazione del \_ messaggio di composizione IME WM per \_ creare correttamente il cursore.                                                                                                                                            |
| RESULTSTR cataloghi globali \_                                                        | Stringa di risultato                  | La stringa di risultato è disponibile quando l'utente sta per completare il processo di composizione. Questa stringa deve essere recuperata e i caratteri devono essere inviati alla casella di modifica.                                                                                                                                                                                        |



 

### <a name="wm_ime_endcomposition"></a>\_ENDCOMPOSITION IME \_ WM

IMM Invia un \_ \_ messaggio ENDCOMPOSITION di WM IME all'applicazione al termine dell'operazione di composizione IME. Questa situazione può verificarsi quando l'utente preme il tasto INVIO per approvare la stringa di composizione o il tasto ESC per annullare la composizione. CDXUTIMEEditBox gestisce questo messaggio impostando il buffer della stringa di composizione come vuoto. Imposta quindi s \_ bHideCaret su false perché la finestra di composizione è chiusa e il cursore nella casella di modifica deve essere nuovamente visibile.

Il gestore di messaggi CDXUTIMEEditBox imposta inoltre s \_ bShowReadingWindow su false. Questo flag controlla se la classe disegna la finestra di lettura quando viene eseguito il rendering della casella di modifica, pertanto deve essere impostata su FALSE al termine di una composizione.

### <a name="wm_ime_notify"></a>\_notifica IME \_ WM

IMM Invia un \_ \_ messaggio di notifica dell'IME WM all'applicazione ogni volta che viene modificata una finestra IME. Un'applicazione che gestisce il disegno delle finestre IME deve elaborare questo messaggio in modo che sia in grado di riconoscere eventuali aggiornamenti al contenuto della finestra. Il wParam indica il comando o la modifica che si sta verificando. CDXUTIMEEditBox gestisce i comandi seguenti:



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
<td>Questo attributo contiene informazioni quali lo stato di ogni carattere nella stringa di composizione (ad esempio, convertito o non convertito). Queste informazioni sono necessarie perché CDXUTIMEEditBox colora i caratteri della stringa di composizione in modo diverso in base ai rispettivi attributi.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/Intl/imn-opencandidate">IMN_OPENCANDIDATE</a>  /  <a href="/windows/desktop/Intl/imn-changecandidate">IMN_CHANGECANDIDATE</a></td>
<td>Inviato all'applicazione quando la finestra candidata sta per essere aperta o aggiornata rispettivamente. La finestra candidato si apre quando un utente desidera modificare la scelta del testo convertito. La finestra viene aggiornata quando un utente sposta l'indicatore di selezione o modifica la pagina. CDXUTIMEEditBox usa un gestore di messaggi per entrambi i comandi perché le attività richieste sono esattamente le stesse:<br/>
<ol>
<li>CDXUTIMEEditBox imposta il membro bShowWindow della struttura dell'elenco dei candidati s_CandList su TRUE per indicare che è necessario disegnare la finestra candidata durante il rendering del frame.</li>
<li>CDXUTIMEEditBox recupera l'elenco dei candidati chiamando <a href="/windows/desktop/api/imm/nf-imm-immgetcandidatelista"><strong>ImmGetCandidateList</strong></a>, prima di tutto per ottenere la dimensione del buffer richiesta e quindi di nuovo per ottenere i dati effettivi.</li>
<li>La struttura dell'elenco dei candidati privati s_CandList viene inizializzata con i dati candidati recuperati.</li>
<li>Le stringhe candidate vengono archiviate come una matrice di stringhe.</li>
<li>L'indice della voce selezionata, nonché l'indice della pagina, viene salvato.</li>
<li>CDXUTIMEEditBox controlla se lo stile della finestra candidato è verticale o orizzontale. Se lo stile della finestra è orizzontale, un buffer di stringa aggiuntivo, il membro HoriCand di s_CandList, deve essere inizializzato con tutte le stringhe candidate, con spazi compresi tra tutte le stringhe adiacenti. Quando si esegue il rendering di una finestra candidata verticale, le singole stringhe candidate vengono disegnate una alla volta, con le coordinate y incrementate per ogni stringa. Questa stringa HoriCand deve tuttavia essere usata per il rendering di una finestra candidata orizzontale, perché il carattere spazio è il modo migliore per separare due stringhe adiacenti sulla stessa riga.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/Intl/imn-closecandidate">IMN_CLOSECANDIDATE</a></td>
<td>Inviato all'applicazione quando una finestra candidata sta per essere chiusa. Questo errore si verifica quando un utente ha effettuato una selezione dall'elenco dei candidati. CDXUTIMEEditBox gestisce questo comando impostando il flag visibile della finestra candidata su FALSE e quindi deselezionando il buffer di stringhe candidato.</td>
</tr>
<tr class="even">
<td>IMN_PRIVATE</td>
<td>Inviato all'applicazione quando l'IME ha aggiornato la relativa stringa di lettura in seguito alla digitazione o alla rimozione di caratteri da parte dell'utente. L'applicazione deve recuperare la stringa di lettura e salvarla per il rendering. CDXUTIMEEditBox dispone di due metodi per recuperare la stringa di lettura, in base al modo in cui le stringhe di lettura sono supportate nell'IME: <br/>
<ul>
<li>Se l'IME supporta la funzione GetReadingString, viene chiamato GetReadingString per recuperare la stringa di lettura.</li>
<li>Se l'IME non implementa GetReadingString, CDXUTIMEEditBox recupera la stringa di lettura dal contenuto del contesto di input.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="rendering"></a>Rendering

Il rendering degli elementi e delle finestre IME è semplice. CDXUTIMEEditBox consente di eseguire prima il rendering della classe di base perché le finestre IME verranno visualizzate nella parte superiore del controllo di modifica. Dopo il rendering della casella di modifica di base, CDXUTIMEEditBox controlla il flag di visibilità di ogni finestra IME (indicatore, composizione, candidato e finestra di lettura) e disegna la finestra se deve essere visibile. Vedere comportamento IME predefinito per le descrizioni dei diversi tipi di finestra IME.

### <a name="input-locale-indicator"></a>Indicatore impostazioni locali di input

Viene eseguito il rendering dell'indicatore delle impostazioni locali di input prima di qualsiasi altra finestra IME perché è un elemento che viene sempre visualizzato. Viene pertanto visualizzato sotto le altre finestre IME. CDXUTIMEEditBox esegue il rendering dell'indicatore chiamando il metodo RenderIndicator, in cui il colore del tipo di carattere dell'indicatore viene determinato esaminando la \_ variabile statica di proprietà, che riflette la modalità di conversione IME corrente. Quando l'IME è abilitato e la conversione nativa è attiva, il metodo usa m \_ IndicatorImeColor come colore dell'indicatore. Se l'IME è disabilitato o si trova in modalità di conversione non nativa, \_ viene usato m IndicatorImeColor per creare il testo dell'indicatore. Per impostazione predefinita, la finestra indicatore viene disegnata a destra della casella di modifica. Le applicazioni possono modificare questo comportamento eseguendo l'override del metodo RenderIndicator.

Nella figura seguente vengono illustrati i diversi aspetti di un indicatore delle impostazioni locali di input per la lingua inglese, giapponese in modalità di conversione alfanumerica e giapponese in modalità di conversione nativa:

![aspetti diversi di un indicatore delle impostazioni locali di input per l'inglese e il giapponese](images/ime-indicator.png)

### <a name="composition-window"></a>Finestra di composizione

Il disegno della finestra di composizione viene gestito nel metodo RenderComposition di CDXUTIMEEditBox. La finestra di composizione viene spostata sopra la casella di modifica. Deve essere disegnato in corrispondenza della posizione del cursore del controllo di modifica sottostante. CDXUTIMEEditBox gestisce il rendering come segue:

1.  L'intera stringa di composizione viene disegnata utilizzando i colori predefiniti della stringa di composizione.
2.  I caratteri con determinati attributi speciali devono essere disegnati in colori diversi, quindi CDXUTIMEEditBox esamina i caratteri della stringa di composizione e controlla l'attributo della stringa. Se l'attributo richiede colori diversi, il carattere viene disegnato nuovamente con i colori appropriati.
3.  Il cursore della finestra di composizione viene disegnato per completare il rendering.

Il cursore deve lampeggiare per gli IME coreano, ma non per altri IME. RenderComposition determina se il cursore deve essere visibile in base ai valori del timer quando viene utilizzato l'IME coreano.

### <a name="reading-and-candidate-windows"></a>Lettura e finestre candidate

Il rendering delle finestre di lettura e candidato viene eseguito dallo stesso metodo CDXUTIMEEditBox, RenderCandidateReadingWindow. Entrambe le finestre contengono una matrice di stringhe per il layout verticale o una singola stringa nel caso del layout orizzontale. La maggior parte del codice in RenderCandidateReadingWindow viene utilizzata per posizionare la finestra in modo che nessuna parte della finestra venga ritagliata all'esterno della finestra dell'applicazione.

## <a name="limitations"></a>Limitazioni

Gli IME talvolta contengono funzionalità avanzate per migliorare la facilità di inserimento del testo. Alcune delle funzionalità disponibili negli IME più recenti sono illustrate nelle figure seguenti. Queste funzionalità avanzate non sono presenti in DXUT. L'implementazione del supporto per queste funzionalità avanzate può risultare complessa perché non è stata definita alcuna interfaccia per ottenere le informazioni necessarie dagli IME.

IME cinese tradizionale avanzato con elenco di candidati espanso:

![IME cinese tradizionale avanzato con elenco di candidati espanso](images/ime-advanced1.png)

IME giapponese avanzato con alcune voci candidate contenenti testo aggiuntivo per descrivere i loro significati:

![IME giapponese avanzato con alcune voci candidate che contengono testo aggiuntivo per descrivere i significati](images/ime-advanced2.png)

IME coreano avanzato che include un sistema di riconoscimento della grafia:

![IME coreano avanzato che include un sistema di riconoscimento della grafia](images/ime-advanced3.png)

## <a name="registry-information"></a>Informazioni registro di sistema

Le seguenti informazioni del registro di sistema vengono verificate per determinare l'orientamento della finestra di lettura, quando l'IME corrente è un nuovo fonetico precedente, che non implementa GetReadingString ().



| Chiave                                                           | Valore            |
|---------------------------------------------------------------|------------------|
| HKCU \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ IME \_ nome | mappatura della tastiera |



 

Dove: \_ il nome IME è MSTCIPH se la versione del file IME è 5,1 o successiva; in caso contrario, il \_ nome IME è tintlgnt.

L'orientamento della finestra di lettura è orizzontale se uno dei valori seguenti:

-   L'IME è la versione 5,0 e il valore di mappatura della tastiera è 0x22 o 0x23
-   L'IME è la versione 5,1 o la versione 5,2 e il valore di mappatura della tastiera è 0x22, 0x23 o 0x24.

Se nessuna delle due condizioni viene soddisfatta, la finestra di lettura è verticale.

## <a name="appendix-a-cht-versions-per-operating-system"></a>Appendice A: versioni CHT per sistema operativo



| Sistema operativo           | Versione IME di CHT |
|----------------------------|-----------------|
| Windows 98                 | 4.2             |
| Windows 2000               | 4.3             |
| unknown                    | 4.4             |
| Windows ME                 | 5.0             |
| Office XP                  | 5.1             |
| Windows XP                 | 5,2             |
| Downloadble Web autonome | 6.0             |



 

## <a name="further-information"></a>Altre informazioni

Per ulteriori informazioni, vedere gli argomenti seguenti:

-   [Installazione e utilizzo degli editor del metodo di input](/windows/desktop/DxTechArts/installing-and-using-input-method-editors)
-   [Visualizzazione del testo internazionale](/windows/desktop/Intl/creating-your-own-format-selection-user-interface)
-   [Il Consorzio Unicode](https://www.unicode.org/)
-   Sviluppo di software internazionale. Dr. International. secondo ed. Redmond, WA: Microsoft Press, 2003.

## <a name="getreadingstring"></a>GetReadingString

Ottiene informazioni sulla stringa di lettura.

**Parametri**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[nel \] contesto di input.

</dd> <dt>

<span id="uReadingBufLen"></span><span id="ureadingbuflen"></span><span id="UREADINGBUFLEN"></span>*uReadingBufLen*
</dt> <dd>

\[\]lunghezza di lpwReadingBuf in WCHAR. Se è zero, indica la lunghezza del buffer di lettura della query.

</dd> <dt>

<span id="lpwReadingBuf_"></span><span id="lpwreadingbuf_"></span><span id="LPWREADINGBUF_"></span>*lpwReadingBuf* 
</dt> <dd>

\[out \] restituisce la stringa di lettura (non zero end).

</dd> <dt>

<span id="pnErrorIndex_"></span><span id="pnerrorindex_"></span><span id="PNERRORINDEX_"></span>*pnErrorIndex* 
</dt> <dd>

\[out \] restituisce l'indice del carattere di errore nella stringa di lettura se è presente.

</dd> <dt>

<span id="pfIsVertical_"></span><span id="pfisvertical_"></span><span id="PFISVERTICAL_"></span>*pfIsVertical* 
</dt> <dd>

\[\]se è true, la lettura dell'interfaccia utente è verticale. In caso contrario, puMaxReadingLen orizzontali.

</dd> <dt>

<span id="puMaxReadingLen_"></span><span id="pumaxreadinglen_"></span><span id="PUMAXREADINGLEN_"></span>*puMaxReadingLen* 
</dt> <dd>

\[\]lunghezza dell'interfaccia utente di lettura. La lunghezza massima di lettura non è fissa; dipende non solo dal layout della tastiera, ma anche dalla modalità di input (ad esempio, codice interno, input surrogato).

</dd> </dl>

**Valori restituiti**

Lunghezza della stringa di lettura.

**Osservazioni:**

Se il valore restituito è maggiore del valore di uReadingBufLen, tutti i parametri di output non sono definiti.

Questa funzione è implementata in CHT IME 6,0 o versioni successive e può essere acquisita da GetProcAddress in un handle del modulo IME. l'handle del modulo IME può essere acquisito da ImmGetIMEFileName e LoadLibrary.

**Requisiti**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Intestazione**
</dt> <dd>

Dichiarata in Imm. h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Libreria di importazione**
</dt> <dd>

Usare Imm. lib.

</dd> </dl>

## <a name="showreadingwindow"></a>ShowReadingWindow

Mostra (o Nascondi) la finestra di lettura.

**Parametri**

<dl> <dt>

<span id="himc_"></span><span id="HIMC_"></span>*himc* 
</dt> <dd>

\[nel \] contesto di input.

</dd> <dt>

<span id="bShow_"></span><span id="bshow_"></span><span id="BSHOW_"></span>*bShow* 
</dt> <dd>

\[in \] impostare su true per visualizzare la finestra di lettura (o false per nasconderla).

</dd> </dl>

**Valori restituiti**

**Osservazioni:**

Restituisce TRUE se ha esito positivo o FALSE in caso contrario.

**Requisiti**

<dl> <dt>

<span id="Header"></span><span id="header"></span><span id="HEADER"></span>**Intestazione**
</dt> <dd>

Dichiarata in Imm. h.

</dd> <dt>

<span id="Import_Library"></span><span id="import_library"></span><span id="IMPORT_LIBRARY"></span>**Libreria di importazione**
</dt> <dd>

Usare Imm. lib.

</dd> </dl>