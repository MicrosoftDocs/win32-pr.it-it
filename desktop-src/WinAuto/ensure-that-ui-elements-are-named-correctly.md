---
title: Assicurarsi che gli elementi dell'interfaccia utente siano denominati correttamente
description: Questo argomento descrive il modo corretto per specificare i nomi degli elementi dell'interfaccia utente nelle applicazioni Microsoft Win32 in modo che Microsoft Active Accessibility possa esporre accuratamente i nomi alle applicazioni client tramite IAccessible \ 32; Proprietà Name.
ms.assetid: 5b8f23cb-9906-4cc4-83d4-73fdf96ed681
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c047228159e011ffa9a0842f1748ee07e6af4a49ff296ae8ed65b494b8c53f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052789"
---
# <a name="ensuring-that-ui-elements-are-correctly-named"></a>Assicurarsi che gli elementi dell'interfaccia utente siano denominati correttamente

Questo argomento descrive il modo corretto per specificare i nomi degli elementi dell'interfaccia utente nelle applicazioni Microsoft Win32 in modo che Microsoft Active Accessibility possa esporre accuratamente i nomi alle applicazioni client tramite la proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) [Name](name-property.md).

Le informazioni contenute in questa sezione si applicano solo Microsoft Active Accessibility. Non si applica alle applicazioni che usano Microsoft Automazione interfaccia utente o a quelle basate su linguaggi di markup come HTML, DHTML (Dynamic HTML) o XML.

-   [Overview](#overview)
-   [Come la denominazione non corretta causa problemi](#how-incorrect-naming-causes-problems)
-   [Come MSAA ottiene la proprietà Name](#how-msaa-gets-the-name-property)
-   [Come trovare e correggere i problemi di denominazione](#how-to-find-and-correct-naming-problems)
-   [Come assegnare correttamente un nome a un trackbar](#how-to-correctly-name-a-trackbar)
-   [Come usare etichette invisibili per assegnare un nome ai controlli](#how-to-use-invisible-labels-to-name-controls)
-   [Come usare l'annotazione diretta per specificare la proprietà Name](#how-to-use-direct-annotation-to-specify-the-name-property)
    -   [Passaggi per l'annotazione della proprietà Name](#steps-for-annotating-the-name-property)
    -   [Esempio di annotazione della proprietà Name](#example-of-annotating-the-name-property)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

In Microsoft Active Accessibility, ogni elemento dell'interfaccia utente in un'applicazione è rappresentato da un oggetto che espone [**l'interfaccia IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Le applicazioni client usano le proprietà e i metodi **dell'interfaccia IAccessible** per interagire con l'elemento dell'interfaccia utente e recuperare informazioni su di esso. Una delle proprietà più importanti esposte **dall'interfaccia IAccessible** è la [proprietà Name](name-property.md). Le applicazioni client si basano sulla proprietà Name per trovare, identificare o annunciare un elemento dell'interfaccia utente all'utente. Se Microsoft Active Accessibility non è in grado di esporre correttamente la proprietà Name di un particolare elemento dell'interfaccia utente, le applicazioni client non saranno in grado di presentare tale elemento all'utente e l'elemento dell'interfaccia utente sarà inaccessibile agli utenti con disabilità.

## <a name="how-incorrect-naming-causes-problems"></a>Come la denominazione non corretta causa problemi

Per illustrare i problemi causati da una denominazione non corretta degli elementi dell'interfaccia utente, prendere in considerazione il formato di immissione del nome illustrato nella figura seguente.

![illustrazione di un modulo semplice per l'immissione di nome e cognome](images/incorrect-form.png)

Anche se gli elementi dell'interfaccia utente nel modulo sembrano corretti, l'implementazione a livello di codice non è corretta. Per un client Microsoft Active Accessibility, ad esempio un'utilità per la lettura dello schermo, la proprietà [Name](name-property.md) del controllo di modifica superiore è "Last Name:" e la proprietà Name del controllo di modifica inferiore è una stringa vuota (""). L'utilità per la lettura dello schermo leggerà il primo controllo di modifica come "Cognome", anche se l'utente deve digitare il nome. L'utilità per la lettura dello schermo leggerà il secondo controllo di modifica come "nessun nome", quindi l'utente non avrà idea di cosa digitare nel secondo controllo di modifica. L'utilità per la lettura dello schermo non è in grado di assistere l'utente nell'immissione di dati in questo semplice formato.

Un altro problema con il modulo è che nessun tasto di scelta rapida viene assegnato a uno dei controlli di modifica. L'utente è obbligato a premere TAB per visualizzare i controlli o a usare il mouse.

Le sezioni seguenti illustrano l'origine di questi problemi e forniscono linee guida per correggerli.

## <a name="how-msaa-gets-the-name-property"></a>Come MSAA ottiene la proprietà Name

Microsoft Active Accessibility ottiene la stringa [della proprietà Name](name-property.md) da posizioni diverse a seconda del tipo di elemento dell'interfaccia utente. Per la maggior parte degli elementi dell'interfaccia utente a cui è associato il testo della finestra, Microsoft Active Accessibility il testo della finestra come stringa della proprietà Name. Esempi di questo tipo di elemento dell'interfaccia utente includono controlli come pulsanti, voci di menu e descrizioni comando.

Per i controlli seguenti, Microsoft Active Accessibility ignora il testo della finestra e cerca invece un'etichetta di testo statico (o etichetta della casella di gruppo) immediatamente precedente al controllo nell'ordine di tabulazione.

-   Caselle combinate
-   Selezione data e ora
-   Controlli Edit e Rich Edit
-   Controlli degli indirizzi IP
-   Caselle di riepilogo
-   Visualizzazioni elenco
-   Barre di stato
-   Scrollbars
-   Controlli statici con lo stile SS \_ ICON o SS \_ BITMAP
-   Trackbar
-   Visualizzazioni albero

Se i controlli precedenti non sono accompagnati da etichette di testo statico o se le etichette non sono implementate correttamente, Microsoft Active Accessibility non può fornire la proprietà [Name](name-property.md) corretta alle applicazioni client.

La maggior parte dei controlli precedenti ha effettivamente un testo della finestra associato. L'editor di risorse genera automaticamente il testo della finestra, costituito da una stringa generica, ad esempio "edit1" o "listbox3". Anche se gli sviluppatori possono sostituire il testo della finestra generato con testo più significativo, la maggior parte non lo fa mai. Poiché il testo della finestra generato non ha alcun significato per l'utente, Microsoft Active Accessibility lo ignora e usa invece l'etichetta di testo statico.

## <a name="how-to-find-and-correct-naming-problems"></a>Come trovare e correggere i problemi di denominazione

Nel formato di immissione del nome illustrato in Come la denominazione non corretta causa problemi, la causa dei problemi è che l'ordine di tabulazione dei controlli non è corretto. L'esame dell'interfaccia utente con uno strumento di test come [Inspect](inspect-objects.md) rivela i problemi relativi alla gerarchia di oggetti. Lo screenshot seguente mostra la gerarchia di oggetti interrotta del modulo di immissione del nome così come viene visualizzata in Inspect.

![Screenshot dello strumento di ispezione che mostra una gerarchia di oggetti non corretta nel modulo di immissione del nome](images/incorrect-object-hierarchy.png)

Nello screenshot precedente si noti che la gerarchia di oggetti non corrisponde alla struttura dei controlli così come vengono visualizzati nell'interfaccia utente del form di immissione del nome. Si noti anche che [Inspect](inspect-objects.md) ha assegnato il nome non corretto all'elemento successivo all'ultimo (è il controllo di modifica per l'immissione del nome e deve essere denominato "First Name:". Si noti infine che Inspect non è stato in grado di trovare un nome per l'ultimo elemento (è il controllo di modifica per l'immissione del cognome e deve avere il nome "Cognome:".

Nell'esempio seguente viene illustrato il contenuto del file di risorse per il modulo di immissione del nome. Si noti che l'ordine di tabulazione non è coerente con la struttura logica dei controlli visualizzati nell'interfaccia utente. Si noti inoltre che non sono specificati tasti di scelta rapida per i due controlli di modifica.

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

Per risolvere i problemi relativi al modulo di immissione del nome, il file di risorse (RC) deve essere modificato per specificare i tasti di scelta rapida e i controlli devono essere posizionati nell'ordine seguente:

1.  Etichetta di testo statico &"nome:".
2.  Controllo di modifica per l'immissione del nome (IDC \_ EDIT1).
3.  Etichetta di testo statico "&Last Name:".
4.  Controllo di modifica per l'immissione del cognome (IDC \_ EDIT2).
5.  Pulsante di comando predefinito "OK".

L'esempio seguente mostra il file di risorse corretto per il modulo di immissione del nome:

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

Per apportare correzioni a un file di risorse, è possibile modificare direttamente il file oppure usare lo strumento Ordine di tabulazione in Microsoft Visual Studio. È possibile accedere all'ordine di tabulazione Visual Studio premendo CTRL+D o scegliendo Ordine di tabulazione **dal** menu Formato. 

Dopo aver corretto e ricompilato l'applicazione, l'interfaccia utente del modulo di immissione dei nomi avrà lo stesso aspetto che aveva in precedenza. Tuttavia, Microsoft Active Accessibility ora fornirà le proprietà Name corrette alle applicazioni client e imposterà correttamente lo stato attivo quando l'utente preme i tasti di scelta rapida ALT+F o ALT+L. Inoltre, [Inspect](inspect-objects.md) mostrerà la gerarchia di oggetti corretta, come illustrato nella schermata seguente.

![Screenshot dello strumento di esplorazione accessibile che mostra una gerarchia di oggetti corretta nel modulo di immissione del nome](images/correct-object-hierarchy.png)

## <a name="how-to-correctly-name-a-trackbar"></a>Come assegnare correttamente un nome a un trackbar

Quando si definisce un trackbar (o dispositivo di scorrimento), assicurarsi che l'etichetta di testo statico principale per il trackbar venga visualizzata prima del trackbar e che le etichette di testo statico per gli intervalli minimo e massimo siano visualizzate dopo il trackbar. Tenere presente Microsoft Active Accessibility usa l'etichetta di testo statico che precede immediatamente un controllo come proprietà [Name](name-property.md) per il controllo. Posizionando l'etichetta di testo statico principale immediatamente prima del trackbar e le altre etichette dopo di essa, si garantisce che Microsoft Active Accessibility fornisce la proprietà Name corretta a un client.

La figura seguente mostra un trackbar tipico con un'etichetta di testo statico principale denominata "Speed" e le etichette di testo statico per gli intervalli minimo ("min") e massimo ("max").

![illustrazione di un controllo trackbar con un'etichetta principale ed etichette per gli intervalli minimo e massimo](images/speed-trackbar.png)

L'esempio seguente illustra il modo corretto per definire un trackbar e le relative etichette di testo statico nel file di risorse:

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

## <a name="how-to-use-invisible-labels-to-name-controls"></a>Come usare etichette invisibili per assegnare un nome ai controlli

Non è sempre possibile o auspicabile avere un'etichetta visibile per ogni controllo. Ad esempio, a volte l'aggiunta di etichette può causare modifiche indesiderate nell'aspetto dell'interfaccia utente. In questo caso, è possibile usare etichette invisibili. Microsoft Active Accessibility il testo associato a un'etichetta invisibile, ma l'etichetta non verrà visualizzata nell'interfaccia utente dell'oggetto visivo né interferirà.

Come per le etichette visibili, un'etichetta invisibile deve precedere immediatamente il controllo nell'ordine di tabulazione. Per rendere invisibile un'etichetta in un file di risorse (RC), aggiungere `NOT WS_VISIBLE` o alla parte di stile del controllo testo `|~WS_VISIBLE` statico. Se si usa l'Editor risorse in Visual Studio, è possibile impostare la proprietà Visible su False.

## <a name="how-to-use-direct-annotation-to-specify-the-name-property"></a>Come usare l'annotazione diretta per specificare la proprietà Name

I proxy predefiniti inclusi nel componente di runtime Microsoft Active Accessibility, Oleacc.dll, forniscono automaticamente un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per tutti i controlli Windows standard. Se si personalizza un controllo Windows standard, i proxy predefiniti fanno del loro meglio per fornire in modo accurato tutte le proprietà **IAccessible** per il controllo personalizzato. È consigliabile testare accuratamente un controllo personalizzato per assicurarsi che i proxy predefiniti fornino valori di proprietà accurati e completi. Se il test rivela valori di proprietà non accurati o incompleti, è possibile usare la tecnica di annotazione dinamica denominata annotazione diretta per fornire valori di proprietà corretti e aggiungere quelli mancanti.

Si noti che l'annotazione dinamica non è solo per i controlli supportati Microsoft Active Accessibility proxy. È anche possibile usarlo per modificare o fornire proprietà per qualsiasi controllo che fornisce la propria [**implementazione di IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

Questa sezione è incentrata sull'uso dell'annotazione diretta per fornire un valore corretto per la [proprietà Name](name-property.md) dell'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un controllo. È possibile usare l'annotazione diretta per fornire anche altri valori di proprietà. Sono inoltre disponibili altre tecniche di annotazione dinamica accanto all'annotazione diretta e le funzionalità e le funzionalità dell'API Di annotazione dinamica si estendono ben oltre quanto descritto in questa sezione. Per altre informazioni sull'annotazione dinamica, vedere [DYNAMIC Annotation API](dynamic-annotation-api.md).

### <a name="steps-for-annotating-the-name-property"></a>Passaggi per l'annotazione della proprietà Name

L'uso dell'annotazione diretta per modificare [la proprietà Name](name-property.md) di un controllo prevede i passaggi seguenti.

1.  Includere i file di intestazione seguenti:
    -   Initguid.h
    -   Oleacc.h

    > [!Note]  
    > Per definire i GUID, è necessario includere Initguid.h prima di Oleacc.h nello stesso file.

     

2.  Inizializzare la Component Object Model (COM) chiamando la [funzione CoInitializeEx,](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in genere durante il processo di inizializzazione dell'applicazione.
3.  Subito dopo la creazione del controllo di destinazione (in genere durante il messaggio [WM \_ INITDIALOG),](../dlgbox/wm-initdialog.md) creare un'istanza del gestore delle annotazioni e ottenere un puntatore al puntatore [**IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
4.  Annotare [la proprietà Name](name-property.md) del controllo di destinazione usando il metodo [**IAccPropServices::SetHwndPropStr.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr)

5.  Rilasciare [**il puntatore IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
6.  Prima che il controllo di destinazione venga eliminato (in genere quando si gestisce il messaggio [WM \_ DESTROY),](../winmsg/wm-destroy.md) creare un'istanza del gestore delle annotazioni e ottenere un puntatore alla relativa [**interfaccia IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
7.  Usare il [**metodo IAccPropServices::ClearHwndProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearhwndprops) per cancellare le annotazioni della proprietà [Name](name-property.md) dal controllo di destinazione.
8.  Rilasciare [**il puntatore IAccPropServices.**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices)
9.  Prima che l'applicazione venga chiusa (in genere durante l'elaborazione del messaggio [WM \_ DESTROY),](../winmsg/wm-destroy.md) rilasciare la libreria COM chiamando la [funzione CoUninitialize.](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)

La [**funzione IAccPropServices::SetHwndPropStr**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropstr) accetta cinque parametri. I primi tre,*hwnd,* *idObject* e *idChild,* si combinano per identificare il controllo. Il quarto parametro, *idProp*, specifica l'identificatore della proprietà da modificare. Per modificare la [proprietà Name](name-property.md), impostare *idProp* su **PROPID ACC \_ \_ NAME**. Per un elenco di altre proprietà che è possibile impostare tramite annotazione diretta, vedere [Uso dell'annotazione diretta.](using-direct-annotation.md) L'ultimo **parametro di SetHwndPropStr**, *str* è la nuova stringa da usare come proprietà Name.

### <a name="example-of-annotating-the-name-property"></a>Esempio di annotazione della proprietà Name

Il codice di esempio seguente illustra come usare l'annotazione diretta per modificare la [proprietà Name](name-property.md) dell'oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un controllo . Per semplicità, nell'esempio viene utilizzata una stringa hard-coded ("Nuovo nome controllo") per impostare la proprietà Name. Le stringhe hard-coded non devono essere usate nella versione finale dell'applicazione perché non possono essere localizzate. Al contrario, caricare sempre le stringhe dal file di risorse. Nell'esempio non vengono inoltre mostrate le chiamate alle [funzioni CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) [e CoUninitialize.](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)


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

 

 