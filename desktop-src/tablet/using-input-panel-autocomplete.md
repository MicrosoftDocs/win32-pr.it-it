---
description: In Windows Vista, il pannello input penna di Tablet PC integra nuove funzionalità di completamento automatico che consentono di aggiornare l'elenco di completamento automatico di un'applicazione in tempo reale quando l'input penna di un utente viene riconosciuto nel pannello di input.
ms.assetid: 0f01f546-f76b-4c61-a204-2a06079a374a
title: Uso del completamento automatico del pannello di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9e7f108631eb2723b71bf8ed919c17a0eabff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128994"
---
# <a name="using-input-panel-autocomplete"></a>Uso del completamento automatico del pannello di input

In Windows Vista, il pannello input penna di Tablet PC integra nuove funzionalità di completamento automatico che consentono di aggiornare l'elenco di completamento automatico di un'applicazione in tempo reale quando l'input penna di un utente viene riconosciuto nel pannello di input. Inoltre, l'elenco di completamento automatico dell'applicazione è posizionato in una posizione comoda per gli utenti del pannello di input. Senza il completamento automatico del pannello di input, l'uso delle funzionalità di completamento automatico con il pannello input è un processo complesso, che richiede agli utenti di inserire un carattere alla volta e spostare il pannello di input per accedere ai suggerimenti per il completamento automatico. Con l'integrazione di, il completamento automatico è uno strumento potente per gli utenti di Tablet PC che accelera e aumenta la facilità di immissione di testo con il pannello di input.

![Pannello di input con elenco di completamento automatico IE](images/9e769482-543a-4e29-b274-8f19ae10250d.jpg)

Sono disponibili tre opzioni per il modo in cui un'applicazione può sfruttare l'integrazione di completamento automatico del pannello di input. Le applicazioni che contengono la funzionalità di completamento automatico compilata usando la funzionalità di completamento automatico della shell (tramite l'interfaccia [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) ) o .NET Framework il completamento automatico (tramite l'enumerazione [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) ) ricevono l'integrazione di completamento automatico del pannello di input senza dover apportare modifiche al codice. Le applicazioni che includono campi di testo personalizzati di completamento automatico possono usare l'API di completamento automatico del pannello di input per ottenere la stessa funzionalità.

In tutti i casi, è possibile apportare queste modifiche all'elenco di completamento automatico dell'applicazione senza duplicare o modificare l'interfaccia utente o la logica di stima usata da un'applicazione per generare un elenco di completamento automatico. L'elenco di completamento automatico continua a essere il proprietario creato dall'applicazione e il contenuto dell'elenco di completamento automatico è identico a quello in cui il testo è stato digitato direttamente nel campo di modifica.

L'integrazione di completamento automatico del pannello di input è supportata nel sistema operativo Windows Vista o versioni successive. L'integrazione di completamento automatico del pannello di input è incorporata nel completamento automatico della shell a partire da Windows Vista e in Windows Form sviluppo a partire da .NET Framework versione 3,0. Sebbene [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) e [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) siano eseguiti in versioni precedenti di Windows, l'integrazione di completamento automatico del pannello di input non è supportata nei sistemi operativi Microsoft Windows XP Tablet PC Edition o versioni precedenti. Se si esegue il completamento automatico del pannello di input nelle versioni precedenti di Tablet PC, le applicazioni ripristinano il comportamento di pre-integrazione.

## <a name="reasons-to-integrate-application-autocomplete-lists-with-input-panel"></a>Motivi per integrare gli elenchi di completamento automatico dell'applicazione con il pannello di input

L'integrazione dell'elenco di completamento automatico di un'applicazione consente la massima facilità e velocità di input per gli utenti che immettono testo in un campo di testo che include la funzionalità di completamento automatico. Inoltre, un'applicazione che include l'integrazione di completamento automatico del pannello di input viene immediatamente visualizzata come se fosse stata sviluppata tenendo conto del Tablet PC, rendendo l'applicazione più interessante per gli utenti di Tablet PC.

### <a name="how-input-panel-and-autocomplete-list-interact-without-integration"></a>Interazione tra il pannello di input e l'elenco di completamento automatico senza integrazione

Uso del pannello input per immettere il testo in un campo di testo che include un elenco di completamento automatico ma che non è integrato con il pannello di input:

1.  L'utente inserisce lo stato attivo nel campo di testo e apre il pannello di input.
2.  L'utente scrive uno o due caratteri.
3.  L'utente tocca **Insert**. Il pannello input immette il testo nel campo di testo dell'applicazione. Viene visualizzato l'elenco di completamento automatico dell'applicazione ed è probabilmente parzialmente o completamente nascosto dal pannello di input.
4.  L'utente trascina il pannello di input per individuare l'elenco di completamento automatico dell'applicazione.
5.  Supponendo che la voce corretta sia inclusa nell'elenco di completamento automatico, l'utente può ora selezionare tale voce. in caso contrario, l'utente deve ripetere i passaggi 2 e 3.

Si tratta ovviamente di un processo complesso. Le aspettative dell'utente relative al funzionamento di un elenco di completamento automatico sono tratteggiate e la loro capacità di eseguire le attività subisce problemi.

### <a name="how-input-panel-and-autocomplete-list-interaction-improves-with-integration"></a>Miglioramento dell'interazione tra il pannello di input e l'elenco di completamento automatico con l'integrazione

Uso del pannello input per immettere il testo in un campo di testo che include un elenco di completamento automatico integrato con il pannello di input:

1.  L'utente inserisce lo stato attivo nel campo di testo e apre il pannello di input.
2.  L'utente scrive uno o due caratteri. L'elenco di completamento automatico dell'applicazione viene visualizzato direttamente sopra o direttamente sotto il pannello di input quando l'utente scrive il testo.
3.  L'utente seleziona la voce dall'elenco di completamento automatico; la voce viene inserita direttamente nel campo di testo dell'applicazione oppure l'utente ripete il passaggio 2 fino a quando non viene visualizzata la voce corretta.

A causa dell'integrazione, l'elenco di completamento automatico viene visualizzato e viene aggiornato mentre l'utente scrive nel pannello di input. Inoltre, l'elenco è posizionato in modo da consentire all'utente di accedere durante la scrittura e non è nascosto dal pannello di input. Infine, quando l'utente seleziona un elemento da un elenco di completamento automatico, l'elemento viene inserito direttamente nel campo immissione testo dell'applicazione, consentendo così all'utente di ignorare il passaggio dell'inserimento di testo dal pannello di input.

![Pannello di input con elenco di completamento automatico di Outlook Express](images/ba59a513-e538-4092-89a6-6d691424dc3d.jpg)

## <a name="standard-autocomplete-components-that-include-input-panel-autocomplete-integration"></a>Componenti di completamento automatico standard che includono l'integrazione di completamento automatico del pannello di input

Sia [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) che [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) includono l'integrazione integrata del completamento automatico del pannello di input. Le applicazioni che usano uno di questi componenti di completamento automatico standard possono sfruttare la funzionalità di completamento automatico del pannello di input senza alcuna attività aggiuntiva. Inoltre, mentre il completamento automatico del pannello di input è supportato solo in Windows Vista o nelle nuove versioni del sistema operativo Windows, le applicazioni compilate utilizzando **IAutoComplete** prima del rilascio di Windows Vista ottengono automaticamente l'integrazione automatica del pannello di input quando vengono eseguite in Windows Vista. Le sezioni seguenti contengono ulteriori informazioni sugli elementi **IAutoComplete** e AutoCompleteMode specifici che includono l'integrazione di completamento automatico del pannello di input.

### <a name="shell-autocomplete-with-input-panel-autocomplete-integration"></a>Completamento automatico della shell con integrazione di completamento automatico del pannello di input

Le applicazioni che usano [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) ottengono gratuitamente l'integrazione di completamento automatico del pannello di input. Mentre le API di completamento automatico della shell sono incluse in Windows 2000, l'integrazione di completamento automatico del pannello di input è supportata solo in Windows Vista e nelle versioni più recenti. Tuttavia, le applicazioni compilate prima del rilascio di Windows Vista che usano **IAutoComplete** ottengono automaticamente l'integrazione di completamento automatico del pannello di input quando vengono eseguite in Windows Vista.

Per sfruttare i vantaggi della funzionalità di completamento automatico del tablet in questo modo, è necessario utilizzare l'oggetto AutoComplete (**\_ completamento automatico CLSID**). Se si desidera fornire funzionalità di completamento automatico per URL o nomi di file, utilizzare la funzione [**SHAutoComplete**](/windows/win32/api/shlwapi/nf-shlwapi-shautocomplete) per creare l'oggetto di completamento automatico.

Oltre a [**IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete), è possibile implementare direttamente [**IAutoComplete2**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete2) o [**IAutoCompleteDropDown**](/windows/win32/api/shobjidl/nn-shobjidl-iautocompletedropdown)e ottenere automaticamente l'integrazione di AutoComplete del pannello di input.

### <a name="input-panel-autocomplete-integration-with-net-framework-applications"></a>Integrazione di completamento automatico del pannello di input con applicazioni .NET Framework

A partire da .NET Framework 3,0, le caselle di testo Windows Form includono il completamento automatico. Windows Form completamento automatico della casella di testo è basato sul completamento automatico della shell, il che significa che l'integrazione di completamento automatico del pannello di input è incorporata. .NET Framework 3,0 è supportato per le edizioni di Windows rilasciate prima di Windows Vista. Tuttavia, poiché l'integrazione di completamento automatico del pannello di input è supportata solo in Windows Vista o versioni successive, l'integrazione di completamento automatico del pannello di input funziona solo in un'applicazione .NET Framework 3,0 quando viene installata in Windows Vista o versioni successive.

Le applicazioni che desiderano sfruttare l'integrazione di completamento automatico del pannello di input in .NET Framework 3,0 devono utilizzare una [casella di testo](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) Windows Form con la proprietà [AutoCompleteMode](/dotnet/api/system.windows.forms.textbox.autocompletemode?view=netcore-3.1) abilitata. Non è necessario eseguire operazioni aggiuntive oltre a Windows Form completamento automatico per sfruttare i vantaggi dell'integrazione di completamento automatico del pannello di input.

## <a name="using-input-panel-autocomplete-apis-directly"></a>Uso diretto delle API per il completamento automatico del pannello di input

Gli sviluppatori di caselle di testo per il completamento automatico personalizzato devono usare direttamente le API di completamento automatico del pannello di input per ottenere l'esperienza di input di testo migliorata che l'integrazione di completamento automatico del pannello di input consente nelle proprie applicazioni. Le API di completamento automatico del pannello di input sono incluse come parte del sistema operativo Windows Vista e come parte di Tablet Platform SDK versione 1,9 o successiva. Le interfacce di completamento automatico del pannello di input sono interfacce basate su COM.

Nella sezione seguente viene descritto il funzionamento dettagliato di queste interfacce per un'applicazione C++. Tuttavia, queste interfacce COM possono essere implementate nella maggior parte dei linguaggi, tra cui C \# , usando l'interoperabilità COM.

Per implementare l'integrazione di completamento automatico del pannello di input in una casella di testo di completamento automatico personalizzato, le due interfacce necessarie sono l' [**interfaccia ITipAutocompleteProvider**](itipautocompleteprovider.md) e l' [**interfaccia ITipAutocompleteClient**](itipautocompleteclient.md). Le definizioni per queste interfacce si trovano in TipAutoComplete. h e TipAutoComplete \_ i.c.

In primo luogo, un'applicazione deve definire e creare un'istanza di una classe del provider di completamento automatico, che implementa [**ITipAutocompleteProvider**](itipautocompleteprovider.md) per ogni campo di immissione di testo che include un elenco di completamento automatico. Questa classe gestisce il lato dell'applicazione dell'integrazione di completamento automatico. Tutte le richieste di completamento automatico dal pannello di input vengono effettuate dal client di completamento automatico all'applicazione tramite il provider di completamento automatico dell'applicazione. Il provider di completamento automatico dell'applicazione deve disporre dell'accesso a HWND per l'elenco di completamento automatico dell'applicazione e HWIND per il campo di immissione testo associato. Inoltre, è necessario implementare i seguenti metodi di **ITipAutocompleteProvider** :

-   [**Metodo ITipAutocompleteProvider:: UpdatePendingText**](itipautocompleteprovider-updatependingtext.md): questo metodo viene usato dal client di completamento automatico per notificare all'applicazione il testo scritto da un utente nel pannello di input. Alla ricezione di questa notifica, il provider è responsabile della generazione di un elenco di completamento automatico come se il testo fosse stato digitato nel campo immissione testo dell'applicazione. La stringa passa al provider di completamento automatico tramite il **Metodo ITipAutocompleteProvider:: UpdatePendingText** include solo il testo attualmente nel pannello di input. Se pertanto nel campo immissione testo è presente testo aggiuntivo, è responsabilità del provider accodarlo correttamente al testo inviato dal client. La stringa pass by **ITipAutocompleteProvider:: UpdatePendingText Method** deve essere considerata come una sostituzione per la selezione corrente nel campo. Se non è presente alcuna selezione corrente, deve essere posizionata nella posizione del punto di inserimento corrente. Una volta generato l'elenco di completamento automatico, il provider deve chiamare il [**Metodo ITipAutocompleteProvider:: Show**](itipautocompleteprovider-show.md) passando **true** per visualizzare l'elenco di completamento automatico. L'applicazione non deve memorizzare nella cache le chiamate a **UpdatePendingText** , bensì considerare ogni chiamata aggiuntiva a **UpdatePendingText** come annullamento della chiamata precedente per evitare il lampeggio di un'interfaccia utente dell'elenco di completamento automatico non aggiornato. Nell'esempio di codice riportato di seguito vengono illustrate queste procedure.

    ```C++
    HRESULT SampleProvider::UpdatePendingText(BSTR bstrPendingText)
    {
       //Discard previously cached pending text from Input Panel
       m_bstrPending.Empty();
        //Store the new pending text from Input Panel as m_bstrPending
    m_bstrPending = bstrPendingText;

        //Get the text from the field in two chunks. The characters to
    //the left of the selection and the characters to the right.
    CComBSTR bstrLeftContext = //Text to the left of the selection
            CComBSTR bstrRightContext = //Text to the right of the selection

    //Discard previously cached complete text
        m_bstrCompleteText.Empty();
        //Append to the field text from the left of the selection
        //the text from Input Panel and then append to that
        //the field text to the right of the selection
        m_bstrCompleteText.Append(bstrLeftContext);
        m_bstrCompleteText.Append(m_bstrPending);
        m_bstrCompleteText.Append(bstrRigtContext);

        //Update the app's AC list based on m_bstrCompleteText
        //...

        //Show the updated AC list by calling the provider's Show method
       Show(true);
       return S_OK;
    }
    ```

    

-   [**Metodo ITipAutocompleteProvider:: Show**](itipautocompleteprovider-show.md): questo metodo viene chiamato da [**UpdatePendingText**](itipautocompleteprovider-updatependingtext.md), ma può anche essere chiamato dal client di completamento automatico in qualsiasi momento. Al momento della ricezione della chiamata, il provider di completamento automatico deve nascondere o mostrare il provider di completamento automatico come indicato dal parametro. Prima di visualizzare l'elenco di completamento automatico, è previsto che il provider di completamento automatico consulti il client di completamento automatico in merito alla posizione in cui posizionare l'elenco di completamento automatico. Altre informazioni sul posizionamento dell'elenco di completamento automatico vengono visualizzate più avanti in questo articolo.

Successivamente, l'applicazione deve utilizzare la funzione Active Template Library (ATL) [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per produrre un'istanza dell' [**interfaccia ITipAutocompleteClient**](itipautocompleteclient.md) con ID di classe **CLSID \_ TipAutoCompleteClient** come server in-process e quindi registrare il provider con il client. Il [**Metodo ITipAutocompleteClient:: AdviseProvider**](itipautocompleteclient-adviseprovider.md) del client di completamento automatico registra il provider con il client per consentire al client di chiamare l'oggetto provider di completamento automatico dell'applicazione. Se tiptsf.dll non è presente nel sistema, la funzione **CoCreateInstance** ha esito negativo e restituisce **REGDB \_ e \_ CLASSNOTREG**. A questo punto, l'applicazione può rimuovere il relativo oggetto [**ITipAutocompleteProvider**](itipautocompleteprovider.md) e procedere come se il pannello di input non esiste, perché non si trova in un sistema di questo tipo.

L'applicazione può scegliere di creare un'istanza di [**ITipAutocompleteClient**](itipautocompleteclient.md) o un'istanza per ogni campo di testo. Per la prima opzione è necessario annullare la registrazione e la registrazione del provider ogni volta che lo stato attivo viene modificato. Altre informazioni sull'annullamento della registrazione del provider di completamento automatico sono riportate più avanti in questo argomento.

Sono necessari diversi passaggi per posizionare l'elenco di completamento automatico che deve essere coordinato tra il provider di completamento automatico (applicazione) e il client di completamento automatico (Pannello input). Prima che venga visualizzato l'elenco di completamento automatico, in seguito a una chiamata al metodo [**show**](itipautocompleteprovider-show.md) del provider di completamento automatico o a causa dell'immissione di testo da parte dell'utente tramite la tastiera, è necessario che il provider consulti il client in merito alla posizione in cui posizionare l'elenco di completamento automatico. Il provider deve eseguire i passaggi seguenti:

-   Usare il [**Metodo ITipAutocompleteClient:: RequestShowUI**](itipautocompleteclient-requestshowui.md) del client di completamento automatico per determinare se il pannello di input è pronto per visualizzare l'elenco di completamento automatico. **RequestShowUI** accetta il parametro *HWND* che rappresenta HWND per la finestra elenco di completamento automatico e il metodo restituisce **true** o **false** per indicare se si tratta dello stato in cui è possibile visualizzare l'elenco di completamento automatico. Se il client restituisce **false**, il provider non deve tentare di visualizzare l'elenco di completamento automatico.
-   Chiamare [**RequestShowUI**](itipautocompleteclient-requestshowui.md) per impostare l'handle della finestra elenco di completamento automatico popup prima di chiamare il [**metodo ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md). In caso contrario, viene generato un errore **E \_ INVALIDARG** quando si chiama **PreferredRects**.
-   Se [**RequestShowUI**](itipautocompleteclient-requestshowui.md) restituisce **true**, il provider deve calcolare il rettangolo predefinito della coordinata della schermata dell'elenco di completamento automatico in base alla posizione del campo immissione testo e quindi chiamare il [**Metodo ITipAutocompleteClient::P referredrects**](itipautocompleteclient-preferredrects.md)del client di completamento automatico. Ciò consente al client di completamento automatico di modificare il rettangolo per evitare l'elenco di completamento automatico sovrapposto al pannello di input. Il metodo **PreferredRects** accetta quattro parametri:

    -   RECT *rcACList*: rettangolo predefinito delle coordinate dello schermo dell'elenco di completamento automatico.
    -   RECT *rcField*: rettangolo delle coordinate dello schermo del campo di immissione di testo corrispondente.
    -   RECT *\* prcModifiedACList*: rettangolo della coordinata dello schermo adattato per il completamento automatico
    -   BOOL *\* pfShowAbove*: questo parametro indica al provider se il rettangolo *prcModifiedACList* posiziona l'elenco di completamento automatico sopra o sotto il pannello di input. L'applicazione può usare queste informazioni per creare correttamente gli elementi dell'interfaccia utente, ad esempio gli handle di ridimensionamento e le barre di scorrimento. Il provider deve passare inizialmente nella direzione in cui l'elenco di completamento automatico verrebbe posizionato rispetto al campo di immissione di testo da *rcACList*. Il client non modifica *pfShowAbove* se imposta *PrcModifiedACList* uguale a *rcACList*.

    Usare i valori restituiti degli argomenti *prcModifiedACList* e *pfShowAbove* out per posizionare e visualizzare la finestra elenco di completamento automatico. Se il pannello di input non è in uso, [**RequestShowUI**](itipautocompleteclient-requestshowui.md) restituisce sempre **true** e *PrcModifiedACList* è sempre uguale a *rcACList*. anche *pfShowAbove* è invariato e il risultato è che le chiamate non hanno alcun effetto sul comportamento dell'applicazione. Nell'esempio di codice riportato di seguito vengono illustrate queste procedure.


```C++
HRESULT SampleProvider::Show(BOOL fShow)
{
    //Ask the AC client if it is OK to show the Autocomplete list.
    BOOL fAllowShowing = FALSE;
    m_spACClient->RequestShowUI(m_hWndList, &fAllowShowing);

    if (fShow && fAllowingShowing)
        {
            // Create the parameters required to call PreferredRects
            RECT rcField = //Rectangle for app's text field
            RECT rcACList = //Default rectangle for app's AC list
            RECT rcModifiedACList = {0, 0, 0, 0};
            BOOL fShowAbove = TRUE;

//Ask the AC client to modify the position of the AC list
m_spACClient->PreferredRects(&rcACList, &rcField,
&rcModifiedACList, &fShowAbove);

            //Show the Autocomplete UI at the modified preferred rectangle
            //from rcModifiedACList and the directional info provide by
//fShowAbove
            //...
        }
    else
        {
        //Hide the Autocomplete list and clean up
        //...
        }
    return S_OK;
}
```



Quando l'utente seleziona un elemento nell'elenco di completamento automatico, il provider deve chiamare il [**Metodo ITipAutocompleteClient:: UserSelection**](itipautocompleteclient-userselection.md) del client oltre a inserire il testo dell'elemento selezionato nel campo di immissione di testo. Il pannello input usa questa notifica per rimuovere tutto il testo rimanente che non è ancora stato inserito dal pannello di input.

Infine, quando il provider non è più necessario, il provider deve essere scollegato dal client di completamento automatico chiamando il [**Metodo ITipAutocompleteClient:: UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) del client di completamento automatico per annullare la registrazione del provider. Potrebbe essere necessario annullare la registrazione del provider per uno dei due motivi seguenti: poiché il campo di immissione di testo a cui è associato il provider è stato eliminato definitivamente o perché l'applicazione sceglie di creare un solo client di completamento automatico, anziché uno per ogni campo di immissione di testo. In questo caso è necessario annullare la registrazione del provider ogni volta che lo stato attivo viene disattivato dal campo di testo.

## <a name="conclusion"></a>Conclusione

L'integrazione di completamento automatico del pannello di input è uno strumento potente per migliorare l'esperienza utente nelle applicazioni Windows che includono gli elenchi di completamento automatico nei tablet PC. Senza integrazione, gli utenti del pannello di input devono eseguire un processo noioso di inserimento del testo un carattere alla volta e riposizionare il pannello di input per poter utilizzare il completamento automatico. Con l'integrazione, gli elenchi di completamento automatico vengono visualizzati in una posizione comoda come input penna nel Pannello input, aumentando sia la velocità che la facilità di immissione di testo. Nelle applicazioni che includono la funzionalità di completamento automatico basata sul completamento automatico della shell o il completamento automatico di .NET Framework 3,0, l'integrazione del pannello di input automatico è una funzionalità gratuita e accattivante. Viene inoltre fornito un semplice set di interfacce basate su COM per abilitare la stessa esperienza integrata per le applicazioni che scelgono di utilizzare controlli di completamento automatico personalizzati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al pannello input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 
