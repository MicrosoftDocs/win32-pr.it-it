---
description: In Windows Vista, il pannello input penna di Tablet PC integra nuove funzionalità di completamento automatico che consentono l'aggiornamento in tempo reale dell'elenco di completamento automatico di un'applicazione quando l'input penna dell'utente viene riconosciuto nel Pannello di input penna.
ms.assetid: 0f01f546-f76b-4c61-a204-2a06079a374a
title: Uso del completamento automatico del pannello di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb0589cca00a45d007c7df6a605f051161c07a62c864504780c307693fe8897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934382"
---
# <a name="using-input-panel-autocomplete"></a>Uso del completamento automatico del pannello di input

In Windows Vista, il pannello input penna di Tablet PC integra nuove funzionalità di completamento automatico che consentono l'aggiornamento in tempo reale dell'elenco di completamento automatico di un'applicazione quando l'input penna dell'utente viene riconosciuto nel Pannello di input penna. Inoltre, l'elenco di completamento automatico dell'applicazione viene posizionato in una posizione comoda per gli utenti del Pannello di input. Senza il completamento automatico del pannello di input, l'uso delle funzionalità di completamento automatico con il Pannello di input è un processo difficile e richiede agli utenti di inserire un carattere alla volta e spostare il Pannello di input per accedere ai suggerimenti di completamento automatico. Con l'integrazione, il completamento automatico è uno strumento potente per gli utenti di Tablet PC che accelera e aumenta la facilità di immissione di testo con il Pannello di input.

![Pannello di input con elenco di completamento automatico di ie](images/9e769482-543a-4e29-b274-8f19ae10250d.jpg)

Sono disponibili tre opzioni per il modo in cui un'applicazione può sfruttare i vantaggi dell'integrazione del completamento automatico del pannello di input. Le applicazioni che contengono funzionalità di completamento automatico compilate usando il completamento automatico della shell (tramite l'interfaccia [**IAutoComplete)**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) o il completamento automatico di .NET Framework (tramite l'enumerazione [AutoCompleteMode)](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) ricevono l'integrazione del completamento automatico del pannello di input senza la necessità di modifiche al codice. Le applicazioni che includono campi di testo personalizzati di completamento automatico possono usare l'API completamento automatico del pannello di input per ottenere la stessa funzionalità.

In tutti i casi, è possibile apportare queste modifiche all'elenco di completamento automatico dell'applicazione senza duplicare o modificare l'interfaccia utente o la logica di stima usata da un'applicazione per generare un elenco di completamento automatico. L'elenco di completamento automatico continua a essere il proprietario dell'applicazione e il contenuto dell'elenco di completamento automatico è lo stesso che se il testo fosse stato digitato direttamente nel campo di modifica.

L'integrazione del completamento automatico del pannello di input è supportata nel sistema operativo Windows Vista o versioni successive. L'integrazione del completamento automatico del pannello di input è integrata nel completamento automatico della shell a partire da Windows Vista e nello sviluppo di Windows Forms a partire .NET Framework versione 3.0. Anche [**se IAutoComplete**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) e [AutoCompleteMode](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) vengono eseguiti in versioni precedenti di Windows, l'integrazione del completamento automatico del pannello di input non è supportata in Microsoft Windows XP Tablet PC Edition o nei sistemi operativi precedenti. Se si esegue il completamento automatico del Pannello input penna in versioni precedenti di Tablet PC, le applicazioni ripristinano il comportamento di pre-integrazione.

## <a name="reasons-to-integrate-application-autocomplete-lists-with-input-panel"></a>Motivi per integrare gli elenchi di completamento automatico delle applicazioni con il Pannello di input

L'integrazione dell'elenco di completamento automatico di un'applicazione consente la massima facilità e velocità di input per gli utenti che immettono testo in un campo di testo che include la funzionalità di completamento automatico. Inoltre, un'applicazione che include l'integrazione del completamento automatico del pannello di input viene immediatamente visualizzata come se fosse stata sviluppata in base al Tablet PC, rendendo l'applicazione più interessante per gli utenti di Tablet PC.

### <a name="how-input-panel-and-autocomplete-list-interact-without-integration"></a>Interazione tra il Pannello di input e l'elenco di completamento automatico senza integrazione

Uso del Pannello di input per immettere testo in un campo di testo che include un elenco di completamento automatico ma che non è integrato con il Pannello di input:

1.  L'utente posiziona lo stato attivo nel campo di testo e apre il Pannello di input.
2.  L'utente scrive uno o due caratteri.
3.  L'utente tocca **Inserisci.** Il pannello di input immette il testo nel campo di testo dell'applicazione. L'elenco Di completamento automatico dell'applicazione viene visualizzato ed è probabilmente parzialmente o completamente nascosto dal Pannello di input.
4.  L'utente trascina il pannello di input per individuare l'elenco di completamento automatico dell'applicazione.
5.  Supponendo che nell'elenco di completamento automatico sia inclusa la voce corretta, l'utente può selezionare tale voce. In caso contrario, l'utente deve ripetere i passaggi 2 e 3.

Si tratta chiaramente di un processo complicato. Le aspettative dell'utente in fatto di funzionamento di un elenco di completamento automatico sono tratteggiate e la loro capacità di eseguire attività ne risentirà.

### <a name="how-input-panel-and-autocomplete-list-interaction-improves-with-integration"></a>Miglioramento dell'interazione tra il pannello di input e l'elenco di completamento automatico con l'integrazione

Uso del Pannello di input per immettere testo in un campo di testo che include un elenco di completamento automatico integrato nel Pannello di input:

1.  L'utente posiziona lo stato attivo nel campo di testo e apre il Pannello di input.
2.  L'utente scrive uno o due caratteri. L'elenco di completamento automatico dell'applicazione viene visualizzato direttamente sopra o sotto il Pannello di input mentre l'utente scrive il testo.
3.  L'utente seleziona la voce dall'elenco Completamento automatico. La voce viene inserita direttamente nel campo di testo dell'applicazione oppure l'utente ripete il passaggio 2 fino a quando non viene visualizzata la voce corretta.

A causa dell'integrazione, l'elenco completamento automatico viene visualizzato e aggiornato mentre l'utente scrive nel pannello di input. Inoltre, l'elenco viene posizionato in modo che sia comodo per l'utente accedere durante la scrittura e non nasconderlo nel Pannello di input. Infine, quando l'utente seleziona un elemento da un elenco di completamento automatico, l'elemento viene inserito direttamente nel campo di immissione di testo dell'applicazione, consentendo all'utente di ignorare il passaggio di inserimento del testo dal Pannello di input.

![Pannello di input con l'elenco di completamento automatico di Outlook Express](images/ba59a513-e538-4092-89a6-6d691424dc3d.jpg)

## <a name="standard-autocomplete-components-that-include-input-panel-autocomplete-integration"></a>Componenti di completamento automatico standard che includono l'integrazione del completamento automatico del pannello di input

Sia [**IAutoComplete che**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) [AutoCompleteMode includono](/dotnet/api/system.windows.forms.autocompletemode?view=netcore-3.1) l'integrazione incorporata del completamento automatico del pannello di input. Le applicazioni che usano uno di questi componenti di completamento automatico standard possono sfruttare le funzionalità di completamento automatico del Pannello input penna senza eseguire operazioni aggiuntive. Inoltre, anche se il completamento automatico del pannello di input è supportato solo in Windows Vista o nelle nuove versioni del sistema operativo Windows, le applicazioni compilate con **IAutoComplete** prima del rilascio di Windows Vista ottengono automaticamente l'integrazione del completamento automatico del pannello di input quando vengono eseguite in Windows Vista. Le sezioni seguenti contengono altre informazioni sugli elementi **IAutoComplete** e AutoCompleteMode specifici che includono l'integrazione del completamento automatico del pannello di input.

### <a name="shell-autocomplete-with-input-panel-autocomplete-integration"></a>Completamento automatico della shell con integrazione del completamento automatico del pannello di input

Le applicazioni che usano [**IAutoComplete ottengono**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete) gratuitamente l'integrazione del completamento automatico del pannello di input. Anche se le API di completamento automatico della shell sono incluse in Windows 2000 e versioni successive, l'integrazione del completamento automatico del pannello di input è supportato solo in Windows Vista e versioni più recenti. Tuttavia, le applicazioni compilate prima del rilascio di Windows Vista che usano **IAutoComplete** ottengono automaticamente l'integrazione del completamento automatico del pannello di input quando vengono eseguite in Windows Vista.

Per sfruttare i vantaggi del completamento automatico dei tablet in questo modo, è necessario usare l'oggetto di completamento automatico (completamento automatico **CLSID \_**). Se si vuole fornire funzionalità di completamento automatico per URL o nomi di file, usare la [**funzione SHAutoComplete**](/windows/win32/api/shlwapi/nf-shlwapi-shautocomplete) per creare l'oggetto di completamento automatico.

Oltre a [**IAutoComplete,**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete)è possibile implementare [**IAutoComplete2**](/windows/win32/api/shldisp/nn-shldisp-iautocomplete2) o [**IAutoCompleteDropDown**](/windows/win32/api/shobjidl/nn-shobjidl-iautocompletedropdown)direttamente e ottenere comunque automaticamente l'integrazione del completamento automatico del pannello di input.

### <a name="input-panel-autocomplete-integration-with-net-framework-applications"></a>Integrazione del completamento automatico del pannello di input con .NET Framework applicazioni

A partire da .NET Framework 3.0, le Windows di testo dei moduli includono Completamento automatico. Windows Il completamento automatico della casella di testo Moduli si basa sul completamento automatico della shell, il che significa che è incorporata anche l'integrazione del completamento automatico del pannello di input. .NET Framework 3.0 è supportato a livello inferiore nelle edizioni Windows rilasciate prima di Windows Vista. Tuttavia, poiché l'integrazione del completamento automatico del pannello di input è supportata solo in Windows Vista o versioni successive, l'integrazione del completamento automatico del pannello di input funziona solo in un'applicazione .NET Framework 3.0 quando è installata in Windows Vista o versioni successive.

Le applicazioni che vogliono sfruttare l'integrazione del completamento automatico del pannello di input in .NET Framework 3.0 devono usare un controllo [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) di Windows Forms con la [proprietà AutoCompleteMode](/dotnet/api/system.windows.forms.textbox.autocompletemode?view=netcore-3.1) abilitata. Non è necessario eseguire altre operazioni oltre a ottenere Windows completamento automatico dei moduli per sfruttare i vantaggi dell'integrazione del completamento automatico del pannello di input.

## <a name="using-input-panel-autocomplete-apis-directly"></a>Uso diretto delle API di completamento automatico del pannello di input

Gli sviluppatori di caselle di testo personalizzate di completamento automatico devono usare direttamente le API di completamento automatico del pannello di input per ottenere un'esperienza di input di testo migliorata abilitata dall'integrazione del completamento automatico del pannello di input nelle applicazioni. Le API di completamento automatico del pannello di input sono incluse come parte del sistema operativo Windows Vista e come parte di Tablet Platform SDK versione 1.9 o successiva. Le interfacce di completamento automatico del pannello di input sono interfacce basate su COM.

La sezione seguente descrive in dettaglio l'uso di queste interfacce per un'applicazione C++. Tuttavia, queste interfacce COM possono essere implementate nella maggior parte dei linguaggi, incluso C \# , tramite l'uso dell'interoperabilità COM.

Per implementare l'integrazione del completamento automatico del pannello di input in una casella di testo di completamento automatico personalizzata, le due interfacce necessarie sono [**l'interfaccia ITipAutocompleteProvider**](itipautocompleteprovider.md) e [**l'interfaccia ITipAutocompleteClient**](itipautocompleteclient.md). Le definizioni per queste interfacce sono disponibili in TipAutoComplete.h e TipAutoComplete \_ i.c.

In primo luogo, un'applicazione deve definire e creare un'istanza di una classe provider di completamento automatico, che implementa [**ITipAutocompleteProvider**](itipautocompleteprovider.md) per ogni campo di immissione di testo che include un elenco di completamento automatico. Questa classe gestisce il lato dell'applicazione dell'integrazione del completamento automatico. Tutte le richieste di completamento automatico dal pannello di input vengono effettuate dal client di completamento automatico all'applicazione tramite il provider di completamento automatico dell'applicazione. Il provider di completamento automatico dell'applicazione deve avere accesso sia all'HWND per l'elenco di completamento automatico dell'applicazione che a HWIND per il campo di immissione testo associato. È inoltre necessario che siano implementati i metodi **seguenti di ITipAutocompleteProvider:**

-   [**Metodo ITipAutocompleteProvider::UpdatePendingText:**](itipautocompleteprovider-updatependingtext.md)questo metodo viene usato dal client di completamento automatico per notificare all'applicazione il testo scritto da un utente nel pannello di input. Al momento della ricezione di questa notifica, il provider è responsabile della generazione di un elenco di completamento automatico come se il testo fosse stato digitato nel campo di immissione testo dell'applicazione. La stringa passata al provider di completamento automatico tramite il metodo **ITipAutocompleteProvider::UpdatePendingText** include solo il testo attualmente presente nel pannello di input. Pertanto, se nel campo di immissione di testo è presente testo aggiuntivo, è responsabilità del provider accodarlo correttamente al testo inviato dal client. La stringa passata dal metodo **ITipAutocompleteProvider::UpdatePendingText** deve essere considerata come una sostituzione per la selezione corrente nel campo . Se non è presente alcuna selezione corrente, deve essere posizionata nella posizione del punto di inserimento corrente. Dopo la generazione dell'elenco di completamento automatico, il provider deve chiamare il metodo [**ITipAutocompleteProvider::Show**](itipautocompleteprovider-show.md) passando **TRUE** per visualizzare l'elenco di completamento automatico. L'applicazione non deve memorizzare nella cache le chiamate a **UpdatePendingText,** ma considerare ogni chiamata aggiuntiva a **UpdatePendingText** come annullamento della chiamata precedente per evitare di lampeggiare in un'interfaccia utente dell'elenco di completamento automatico non aggiornata. Il codice di esempio seguente illustra queste procedure.

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

    

-   [**Metodo ITipAutocompleteProvider::Show:**](itipautocompleteprovider-show.md)questo metodo viene chiamato da [**UpdatePendingText,**](itipautocompleteprovider-updatependingtext.md)ma può anche essere chiamato dal client di completamento automatico in qualsiasi momento. Al momento della ricezione di questa chiamata, il provider di completamento automatico deve nascondere o visualizzare il provider di completamento automatico come indicato dal parametro . Prima di visualizzare l'elenco di completamento automatico, è previsto che il provider di completamento automatico consulti il client di completamento automatico per informazioni su dove posizionare l'elenco di completamento automatico. Altre informazioni sul posizionamento dell'elenco Completamento automatico sono disponibili più avanti in questo articolo.

Successivamente, l'applicazione deve usare la funzione [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) di Active Template Library (ATL) per produrre un'istanza dell'interfaccia [**ITipAutocompleteClient**](itipautocompleteclient.md) con ID di classe **CLSID \_ TipAutoCompleteClient** come server in-process e quindi registrare il provider con il client. Il metodo [**ITipAutocompleteClient::AdviseProvider**](itipautocompleteclient-adviseprovider.md) del client di completamento automatico registra il provider con il client per consentire al client di chiamare l'oggetto provider di completamento automatico dell'applicazione. Se tiptsf.dll non è presente nel sistema, la **funzione CoCreateInstance** ha esito negativo e restituisce **REGDB \_ E \_ CLASSNOTREG**. A questo punto l'applicazione può rimuovere il relativo oggetto [**ITipAutocompleteProvider**](itipautocompleteprovider.md) e procedere come se il pannello di input non esistesse, perché non è presente in un sistema di questo tipo.

L'applicazione può scegliere di creare un'istanza di [**ITipAutocompleteClient**](itipautocompleteclient.md) o un'istanza per ogni campo di testo. La prima opzione richiede l'annullamento della registrazione e la registrazione del provider ogni volta che viene modificato lo stato attivo. Altre informazioni sull'annullamento della registrazione del provider di completamento automatico sono disponibili più avanti in questo argomento.

Esistono diversi passaggi necessari per posizionare l'elenco di completamento automatico che deve essere coordinato tra il provider di completamento automatico (applicazione) e il client di completamento automatico (pannello di input). Prima che venga visualizzato l'elenco di completamento automatico, in seguito a una chiamata al metodo [**Show**](itipautocompleteprovider-show.md) del provider di completamento automatico o a causa dell'immissione di testo da parte dell'utente tramite la tastiera, il provider deve consultare il client su dove posizionare l'elenco di completamento automatico. Il provider deve eseguire i passaggi seguenti:

-   Usare il metodo [**ITipAutocompleteClient::RequestShowUI**](itipautocompleteclient-requestshowui.md) del client di completamento automatico per determinare se il Pannello di input è pronto per visualizzare l'elenco di completamento automatico. **RequestShowUI** accetta il parametro *HWND* che corrisponde a HWND per la finestra dell'elenco di completamento automatico e il metodo restituisce **TRUE** o **FALSE** per indicare se è lo stato in cui è possibile visualizzare l'elenco di completamento automatico. Se il client restituisce **FALSE,** il provider non deve tentare di visualizzare l'elenco di completamento automatico.
-   Chiamare [**RequestShowUI**](itipautocompleteclient-requestshowui.md) per impostare l'handle della finestra elenco di completamento automatico popup prima di chiamare il metodo [**ITipAutocompleteClient::P referredRects**](itipautocompleteclient-preferredrects.md). In caso negativo, verrà generato un **errore E \_ INVALIDARG** quando si **chiama PreferredRects**.
-   Se [**RequestShowUI**](itipautocompleteclient-requestshowui.md) restituisce **TRUE,** il provider deve calcolare il rettangolo delle coordinate dello schermo predefinito dell'elenco di completamento automatico in base alla posizione del campo di immissione di testo e quindi chiamare il metodo [**ITipAutocompleteClient::P referredRects del**](itipautocompleteclient-preferredrects.md)client di completamento automatico. Ciò consente al client di completamento automatico di regolare il rettangolo per evitare che l'elenco di completamento automatico si sovrapponga al Pannello input penna. Il **metodo PreferredRects** accetta quattro parametri:

    -   RECT *rcACList:* rettangolo delle coordinate dello schermo predefinito dell'elenco di completamento automatico.
    -   RECT *rcField:* rettangolo delle coordinate dello schermo del campo di immissione testo corrispondente.
    -   RECT *\* prcModifiedACList:* rettangolo delle coordinate dello schermo regolato per completamento automatico
    -   BOOL *\* pfShowAbove:* questo parametro indica al provider se il rettangolo *prcModifiedACList* posiziona l'elenco di completamento automatico sopra o sotto il Pannello di input. L'applicazione può usare queste informazioni per disegnare correttamente elementi dell'interfaccia utente, ad esempio quadratini di ridimensionamento e barre di scorrimento. Il provider deve inizialmente passare nella direzione in cui l'elenco di completamento automatico verrebbe posizionato rispetto al campo di immissione di testo *da rcACList*. Il client non modifica *pfShowAbove se* imposta *prcModifiedACList* su *rcACList*.

    Usare i valori restituiti degli argomenti *prcModifiedACList* e *pfShowAbove* out per posizionare e visualizzare la finestra elenco di completamento automatico. Se il Pannello input non è in uso, [**RequestShowUI**](itipautocompleteclient-requestshowui.md) restituisce sempre **TRUE** e *prcModifiedACList* è sempre uguale a *rcACList*. *Anche pfShowAbove* rimane invariato, in quanto le chiamate non influiscono sul comportamento dell'applicazione. Il codice di esempio seguente illustra queste procedure.


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



Quando l'utente seleziona un elemento nell'elenco Completamento automatico, il provider deve chiamare il metodo [**ITipAutocompleteClient::UserSelection**](itipautocompleteclient-userselection.md) del client oltre a inserire il testo dell'elemento selezionato nel campo di immissione testo. Il Pannello input penna usa questa notifica per rimuovere tutto il testo rimanente che non è ancora stato inserito dal Pannello input penna.

Infine, quando il provider non è più necessario, il provider deve essere scollegato dal client di completamento automatico chiamando il metodo [**ITipAutocompleteClient::UnadviseProvider**](itipautocompleteclient-unadviseprovider.md) del client di completamento automatico per annullare la registrazione del provider. Potrebbe essere necessario annullare la registrazione del provider per uno dei due motivi seguenti: perché il campo di immissione testo a cui è associato il provider è stato eliminato o perché l'applicazione sceglie di creare un solo client di completamento automatico, anziché uno per ogni campo di immissione di testo. In questo caso il provider deve essere annullato ogni volta che lo stato attivo viene rimosso dal campo di testo.

## <a name="conclusion"></a>Conclusione

L'integrazione del completamento automatico del pannello input è uno strumento potente per migliorare l'esperienza utente nelle applicazioni Windows che includono elenchi di completamento automatico nei Tablet PC. Senza integrazione, gli utenti del Pannello input penna devono eseguire un noioso processo di inserimento di testo un carattere alla volta e il riposizionamento del Pannello input penna per usare il completamento automatico. Con l'integrazione, gli elenchi di completamento automatico vengono visualizzati in una posizione comoda come input penna degli utenti nel Pannello input penna, aumentando sia la velocità che la facilità di immissione del testo. Nelle applicazioni che includono funzionalità di completamento automatico create in base al completamento automatico della shell o .NET Framework 3.0, l'integrazione del completamento automatico del Pannello input penna è una funzionalità gratuita e accattivante. Viene inoltre fornito un semplice set di interfacce basate su COM per abilitare la stessa esperienza integrata per le applicazioni che scelgono di usare controlli di completamento automatico personalizzati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sul pannello di input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 
