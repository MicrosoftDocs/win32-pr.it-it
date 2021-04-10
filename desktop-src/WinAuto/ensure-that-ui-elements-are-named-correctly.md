---
title: Verifica della corretta denominazione degli elementi dell'interfaccia utente
description: In questo argomento viene descritto il modo corretto per specificare i nomi degli elementi dell'interfaccia utente nelle applicazioni Microsoft Win32 in modo che Microsoft Active Accessibility possa esporre accuratamente i nomi alle applicazioni client tramite IAccessible \ 32; Proprietà Name.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3c4f1fc129aea9b793bac1935d678645b28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963143"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a>Verifica della corretta denominazione degli elementi dell'interfaccia utente

In questo argomento viene descritto il modo corretto per specificare i nomi degli elementi dell'interfaccia utente nelle applicazioni Microsoft Win32 in modo che Microsoft Active Accessibility possa esporre accuratamente i nomi alle applicazioni client tramite la [proprietà nome](name-property.md) [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

Le informazioni contenute in questa sezione si applicano solo a Microsoft Active Accessibility. Non si applica alle applicazioni che utilizzano l'automazione interfaccia utente Microsoft o a quelle basate su linguaggi di markup, ad esempio HTML, DHTML (Dynamic HTML) o XML.

-   [Overview](#overview)
-   [Come la denominazione non corretta causa problemi](#how-incorrect-naming-causes-problems)
-   [Come MSAA ottiene la proprietà Name](#how-msaa-gets-the-name-property)
-   [Come individuare e correggere i problemi di denominazione](#how-to-find-and-correct-naming-problems)
-   [Come assegnare un nome corretto a un TrackBar](#how-to-correctly-name-a-trackbar)
-   [Come usare le etichette invisibili per denominare i controlli](#how-to-use-invisible-labels-to-name-controls)
-   [Come usare l'annotazione diretta per specificare la proprietà Name](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [Passaggi per l'annotazione della proprietà Name](#steps-for-annotating-the-name-property)
    -   [Esempio di annotazione della proprietà Name](#example-of-annotating-the-name-property)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

In Microsoft Active Accessibility ogni elemento dell'interfaccia utente in un'applicazione è rappresentato da un oggetto che espone l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Le applicazioni client utilizzano le proprietà e i metodi dell'interfaccia **IAccessible** per interagire con l'elemento dell'interfaccia utente e per recuperare informazioni su di esso. Una delle proprietà più importanti esposte dall'interfaccia **IAccessible** è la [proprietà Name](name-property.md). Le applicazioni client si basano sulla proprietà Name per trovare, identificare o annunciare un elemento dell'interfaccia utente. Se Microsoft Active Accessibility non è in grado di esporre correttamente la proprietà Name di un particolare elemento dell'interfaccia utente, le applicazioni client non saranno in grado di presentare l'elemento dell'interfaccia utente e l'elemento dell'interfaccia utente sarà inaccessibile agli utenti con particolari esigenze.

## <a name="how-incorrect-naming-causes-problems"></a>Come la denominazione non corretta causa problemi

Per illustrare i problemi causati dalla denominazione non corretta degli elementi dell'interfaccia utente, prendere in considerazione il formato della voce di nome illustrato nella figura seguente.

![illustrazione di un modulo semplice per l'immissione del nome e del cognome](images/incorrect-form.png)

Anche se gli elementi dell'interfaccia utente nel form hanno un aspetto corretto, l'implementazione a livello di codice non è corretta. A un client di Microsoft Active Accessibility, ad esempio un'Reader per la lettura dello schermo, la [proprietà Name](name-property.md) del controllo top Edit è "Last Name:&quot; e la proprietà Name del controllo Bottom Edit è una stringa vuota (&quot;"). Il controllo di modifica superiore verrà letto dal lettore dello schermo come "cognome", sebbene l'utente debba digitare il nome. Il secondo controllo di modifica viene letto come "nessun nome", pertanto l'utente non avrà idea di cosa digitare nel secondo controllo di modifica. L'utente non è in grado di supportare l'immissione di dati in questo semplice modulo.

Un altro problema con il modulo è che nessun tasto di scelta rapida viene assegnato a uno dei controlli di modifica. L'utente è forzato a eseguire una tabulazione sui controlli o usare il mouse.

Le sezioni seguenti illustrano l'origine di questi problemi e forniscono linee guida per correggerli.

## <a name="how-msaa-gets-the-name-property"></a>Come MSAA ottiene la proprietà Name

Microsoft Active Accessibility ottiene la stringa della [proprietà Name](name-property.md) da percorsi diversi a seconda del tipo di elemento dell'interfaccia utente. Per la maggior parte degli elementi dell'interfaccia utente a cui è associato il testo della finestra, Microsoft Active Accessibility usa il testo della finestra come stringa della proprietà Name. Esempi di questo tipo di elemento dell'interfaccia utente includono controlli quali pulsanti, voci di menu e descrizioni comandi.

Per i seguenti controlli, Microsoft Active Accessibility ignora il testo della finestra e cerca invece un'etichetta di testo statico (o etichetta casella di gruppo) immediatamente prima del controllo nell'ordine di tabulazione.

-   Caselle combinate
-   Selezione data e ora
-   Modifica e controlli Rich Edit
-   Controlli degli indirizzi IP
-   Caselle di riepilogo
-   Visualizzazione elenco
-   Indicatori di stato
-   Barre
-   Controlli statici con \_ icona SS o \_ stile bitmap SS
-   TrackBar
-   Visualizzazioni ad albero

Se i controlli precedenti non sono accompagnati da etichette di testo statiche o se le etichette non sono implementate correttamente, Microsoft Active Accessibility non è in grado di fornire la [proprietà nome](name-property.md) corretta alle applicazioni client.

Alla maggior parte dei controlli precedenti è effettivamente associato il testo della finestra. L'editor risorse genera automaticamente il testo della finestra, costituito da una stringa generica, ad esempio "Edit1" o "listbox3". Sebbene gli sviluppatori possano sostituire il testo della finestra generata con testo più significativo, la maggior parte mai. Poiché il testo della finestra generata non ha significato per l'utente, Microsoft Active Accessibility lo ignora e usa invece l'etichetta di testo statico associata.

## <a name="how-to-find-and-correct-naming-problems"></a>Come individuare e correggere i problemi di denominazione

Nel modulo di immissione del nome illustrato in che modo la denominazione errata causa problemi, la causa dei problemi è che l'ordine di tabulazione dei controlli non è corretto. Esaminando l'interfaccia utente con uno strumento di test come [ispeziona](inspect-objects.md) , si riveleranno i problemi della gerarchia di oggetti. Lo screenshot seguente mostra la gerarchia di oggetti interrotta del modulo di immissione del nome come appare in ispeziona.

![screenshot dello strumento di controllo che mostra una gerarchia di oggetti non corretta del modulo di immissione del nome](images/incorrect-object-hierarchy.png)

Nello screenshot precedente si noti che la gerarchia di oggetti non corrisponde alla struttura dei controlli così come appaiono nell'interfaccia utente del modulo di immissione del nome. Si noti inoltre che l' [ispezione](inspect-objects.md) ha assegnato il nome errato all'elemento successivo all'ultimo (si tratta del controllo di modifica per l'immissione del nome e deve essere un nome denominato "First Name:". Infine, si noti che ispezionare non è stato in grado di trovare un nome per l'ultimo elemento. si tratta del controllo di modifica per l'immissione del cognome e deve avere il nome "Cognome:".

Nell'esempio seguente viene illustrato il contenuto del file di risorse per il form di immissione del nome. Si noti che l'ordine di tabulazione non è coerente con la struttura logica dei controlli così come appaiono nell'interfaccia utente. Si noti inoltre che non viene specificato alcun tasto di scelta rapida per i due controlli di modifica.

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
    LTEXT           "First Name:",IDC_STATIC,8,16,43,8
    LTEXT           "Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
END
```

Per correggere i problemi con il modulo di immissione del nome, è necessario modificare il file di risorse (RC) per specificare i tasti di scelta rapida e i controlli devono essere inseriti nell'ordine seguente:

1.  Etichetta di testo statico "&First Name:".
2.  Controllo di modifica per l'immissione del nome (IDC \_ EDIT1).
3.  Etichetta di testo statico "&Last Name:".
4.  Controllo di modifica per l'immissione del cognome (IDC \_ Edit2).
5.  Pulsante di push predefinito "OK".

Nell'esempio seguente viene illustrato il file di risorse corretto per il form di immissione del nome:

``` syntax
IDD_INPUTNAME DIALOGEX 22, 17, 312, 118
STYLE DS_SETFONT | DS_MODALFRAME | WS_CAPTION | WS_SYSMENU
CAPTION "Enter your name"
FONT 8, "System", 0, 0, 0x0
BEGIN
    LTEXT           "&First Name:",IDC_STATIC,8,16,43,8
    EDITTEXT        IDC_EDIT1,53,15,120,12,ES_AUTOHSCROLL
    LTEXT           "&Last Name:",IDC_STATIC,8,33,43,8
    EDITTEXT        IDC_EDIT2,53,34,120,12,ES_AUTOHSCROLL
    DEFPUSHBUTTON   "OK",IDOK,179,35,30,11,WS_GROUP
END
```

Per apportare correzioni a un file di risorse, è possibile modificare direttamente il file oppure utilizzare lo strumento di ordine di tabulazione in Microsoft Visual Studio. Per accedere allo strumento per l'ordine di tabulazione in Visual Studio, è possibile premere CTRL + D oppure selezionare **Tab Order** dal menu **formato** .

Dopo la correzione e la ricompilazione dell'applicazione, l'interfaccia utente del form di immissione dei nomi sarà analoga a quella precedente. Tuttavia, in Microsoft Active Accessibility verranno ora fornite le proprietà nome corrette per le applicazioni client e lo stato attivo verrà impostato correttamente quando l'utente preme i tasti di scelta rapida ALT + F o ALT + L. Inoltre, il [controllo](inspect-objects.md) visualizzerà la gerarchia di oggetti corretta, come illustrato nella schermata seguente.

![screenshot dello strumento di esplorazione accessibile che mostra una gerarchia di oggetti corretta del modulo di immissione del nome](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a>Come assegnare un nome corretto a un TrackBar

Quando si definisce un TrackBar (o un dispositivo di scorrimento), assicurarsi che l'etichetta di testo statico principale per il controllo TrackBar venga visualizzata prima del TrackBar e che le etichette di testo statiche per gli intervalli minimo e massimo vengano visualizzate dopo il controllo TrackBar. Tenere presente che Microsoft Active Accessibility usa l'etichetta di testo statico che precede immediatamente un controllo come [proprietà Name](name-property.md) per il controllo. Inserendo l'etichetta di testo statico principale immediatamente prima del TrackBar e le altre etichette dopo di essa, garantisce che Microsoft Active Accessibility fornisca la proprietà Name corretta a un client.

Nella figura seguente viene illustrato un TrackBar tipico con un'etichetta di testo statico principale denominata "Speed" e le etichette di testo statico per gli intervalli minimo ("min") e Maximum ("Max").

![illustrazione di un controllo TrackBar con un'etichetta principale ed etichette per gli intervalli minimo e massimo](images/speed-trackbar.png)

Nell'esempio seguente viene illustrato il modo corretto per definire un TrackBar e le relative etichette di testo statiche nel file di risorse:

``` syntax
BEGIN
    ...

    LTEXT           "&Speed",IDC_STATIC,47,20,43,8
    CONTROL         "",IDC_SLIDER1,"msctls_trackbar32",
                    TBS_AUTOTICKS | TBS_BOTH | WS_TABSTOP,
                    32,32,62,23
    LTEXT           "min",IDC_STATIC,16,37,15,8
    LTEXT           "max",IDC_STATIC,94,38,43,8

    ...
END
```

## <a name="how-to-use-invisible-labels-to-name-controls"></a>Come usare le etichette invisibili per denominare i controlli

Non è sempre possibile o auspicabile avere un'etichetta visibile per ogni controllo. Talvolta, ad esempio, l'aggiunta di etichette può causare modifiche indesiderate nell'aspetto dell'interfaccia utente. In questo caso, è possibile usare le etichette invisibili. Microsoft Active Accessibility rileverà comunque il testo associato a un'etichetta invisibile, ma l'etichetta non verrà visualizzata o interferirà con l'interfaccia utente visiva.

Come per le etichette visibili, un'etichetta invisibile deve precedere immediatamente il controllo nell'ordine di tabulazione. Per rendere invisibile un'etichetta in un file di risorse (RC), aggiungere `NOT WS_VISIBLE` o `|~WS_VISIBLE` alla parte di stile del controllo testo statico. Se si usa l'editor di risorse in Visual Studio, è possibile impostare la proprietà Visible su false.

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a>Come usare l'annotazione diretta per specificare la proprietà Name

I proxy predefiniti inclusi nel componente runtime di Microsoft Active Accessibility, Oleacc.dll, forniscono automaticamente un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per tutti i controlli Windows standard. Se si personalizza un controllo Windows standard, i proxy predefiniti eseguono le operazioni migliori per fornire in modo accurato tutte le proprietà **IAccessible** per il controllo personalizzato. È necessario testare accuratamente un controllo personalizzato per assicurarsi che i proxy predefiniti forniscano valori di proprietà accurati e completi. Se il test rivela valori di proprietà non accurati o incompleti, potrebbe essere possibile utilizzare la tecnica di annotazione dinamica denominata annotazione diretta per fornire valori di proprietà corretti e aggiungere quelli mancanti.

Si noti che l'annotazione dinamica non è solo per i controlli supportati dai proxy di Microsoft Active Accessibility. È anche possibile usarlo per modificare o fornire proprietà per qualsiasi controllo che fornisce la propria implementazione di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

Questa sezione è incentrata sull'uso dell'annotazione diretta per fornire un valore corretto per la [proprietà Name](name-property.md) dell'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un controllo. È possibile utilizzare l'annotazione diretta per fornire anche altri valori di proprietà. Sono inoltre disponibili altre tecniche di annotazione dinamica accanto all'annotazione diretta e le funzionalità e le funzionalità dell'API di annotazione dinamica si estendono oltre quanto descritto in questa sezione. Per altre informazioni sull'annotazione dinamica, vedere [API di annotazione dinamica](dynamic-annotation-api.md).

### <a name="steps-for-annotating-the-name-property"></a>Passaggi per l'annotazione della proprietà Name

L'uso dell'annotazione diretta per modificare la [proprietà Name](name-property.md) di un controllo prevede i passaggi seguenti.

1.  Includere i file di intestazione seguenti:
    -   Initguid. h
    -   Oleacc. h

    > [!Note]  
    > Per definire i GUID, è necessario includere Initguid. h prima di oleacc. h nello stesso file.

     

2.  Inizializzare la libreria Component Object Model (COM) chiamando la funzione [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) , in genere durante il processo di inizializzazione dell'applicazione.
3.  Subito dopo la creazione del controllo di destinazione (in genere durante il messaggio [WM \_ INITDIALOG](../dlgbox/wm-initdialog.md) ), creare un'istanza di gestione annotazioni e ottenere un puntatore al relativo puntatore [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
4.  Annotare la [proprietà Name](name-property.md) del controllo di destinazione usando il metodo [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) .

5.  Rilasciare il puntatore [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
6.  Prima che il controllo di destinazione venga eliminato definitivamente (in genere durante la gestione del messaggio [WM \_ Destroy](../winmsg/wm-destroy.md) ), creare un'istanza di gestione annotazioni e ottenere un puntatore alla relativa interfaccia [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
7.  Usare il metodo [**IAccPropServices:: ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) per cancellare le annotazioni della [proprietà Name](name-property.md) dal controllo di destinazione.
8.  Rilasciare il puntatore [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
9.  Prima di uscire dall'applicazione (in genere durante l'elaborazione del messaggio [WM \_ Destroy](../winmsg/wm-destroy.md) ), rilasciare la libreria COM chiamando la funzione [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .

La funzione [**IAccPropServices:: SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) accetta cinque parametri. I primi tre, ovvero *HWND*, *idObject* e *idChild*, vengono combinati per identificare il controllo. Il quarto parametro, *idProp*, specifica l'identificatore della proprietà da modificare. Per modificare la [proprietà Name](name-property.md), impostare *idProp* su **propid \_ ACC \_ Name**. Per un elenco di altre proprietà che è possibile impostare tramite l'annotazione diretta, vedere [uso dell'annotazione diretta](using-direct-annotation.md). L'ultimo parametro di **SetHwndPropStr**, *Str*, è la nuova stringa da usare come proprietà Name.

### <a name="example-of-annotating-the-name-property"></a>Esempio di annotazione della proprietà Name

Nell'esempio di codice seguente viene illustrato come utilizzare l'annotazione diretta per modificare la [proprietà Name](name-property.md) dell'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un controllo. Per semplificare le operazioni, nell'esempio viene utilizzata una stringa hardcoded ("nuovo nome controllo") per impostare la proprietà Name. Le stringhe hardcoded non devono essere usate nella versione finale dell'applicazione perché non possono essere localizzate. Al contrario, caricare sempre le stringhe dal file di risorse. Inoltre, nell'esempio non vengono visualizzate le chiamate alle funzioni [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [CoUninitialize](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) .


```C++
#include <initguid.h>
#include <oleacc.h>

// AnnotateControlName - Uses direct annotation to change the Name property 
// of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose Name property is to be changed.
HRESULT AnnotateControlName(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;        

    IAccPropServices *pAccPropSvc = NULL;  

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Set the Name property for the control.
    // Note: A hard-coded string is used here to keep the example simple.
    // Always use localizable string resources in your applications. 
    hr = pAccPropSvc->SetHwndPropStr(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        PROPID_ACC_NAME, L"New Control Name");

    pAccPropSvc->Release();
    
    return hr;
}

// RemoveAnnotatedNameFromControl - Removes the annotated name from the 
// Name property of the IAccessible object for a control.
//
// hDlg - Handle of the dialog box that contains the control.
// hwndCtl - Handle of the control whose annotated name is to be removed.
HRESULT RemoveAnnotatedNameFromControl(HWND hDlg, HWND hwndCtl)
{
    HRESULT hr;

    IAccPropServices *pAccPropSvc = NULL;

    // Create an instance of the annotation manager and retrieve the 
    // IAccPropServices pointer.
    hr = CoCreateInstance(CLSID_AccPropServices, NULL, CLSCTX_SERVER, 
        IID_IAccPropServices, (void **) &pAccPropSvc);

    if (hr != S_OK || pAccPropSvc == NULL)
        return hr;

    // Remove the annotated name from the Name property for the control.
    MSAAPROPID propid = PROPID_ACC_NAME;
    hr = pAccPropSvc->ClearHwndProps(hwndCtl, OBJID_CLIENT, CHILDID_SELF, 
        &propid, 1);

    // Release the annotation manager.
    pAccPropSvc->Release();

    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[API di annotazione dinamica](dynamic-annotation-api.md)
</dt> <dt>

[Specifica della proprietà Name](providing-the-name-property.md)
</dt> <dt>

[Strumenti di test](testing-tools.md)
</dt> </dl>

 

 