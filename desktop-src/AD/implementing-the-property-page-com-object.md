---
title: Implementazione dell'oggetto COM della pagina delle proprietà
description: Un'estensione della finestra delle proprietà è un oggetto COM implementato come server in-process.
ms.assetid: 77a71086-1949-4828-801e-073ea5a6838b
ms.tgt_platform: multiple
keywords:
- Implementazione dell'oggetto COM della pagina delle proprietà
- Oggetto COM della pagina delle proprietà, implementazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55962002ca059ad6e9c137925d1ba21ba9adc513
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872298"
---
# <a name="implementing-the-property-page-com-object"></a>Implementazione dell'oggetto COM della pagina delle proprietà

Un'estensione della finestra delle proprietà è un oggetto COM implementato come server in-process. L'estensione della finestra delle proprietà deve implementare le interfacce [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) . Viene creata un'istanza di un'estensione della finestra delle proprietà quando l'utente Visualizza la finestra delle proprietà per un oggetto di una classe per la quale l'estensione della finestra delle proprietà è stata registrata nell'identificatore di visualizzazione della classe.

-   [Implementazione di IShellExtInit](#implementing-ishellextinit)
-   [Implementazione di IShellPropSheetExt](#implementing-ishellpropsheetext)
-   [Passaggio dell'oggetto estensione alla pagina delle proprietà](#passing-the-extension-object-to-the-property-page)
-   [Utilizzo dell'oggetto Notification](#working-with-the-notification-object)
-   [Varie](#miscellaneous)
-   [Finestre delle proprietà a selezione multipla](#multiple-selection-property-sheets)
-   [Novità con Windows Server 2003](#new-with-windows-server-2003)
-   [Argomenti correlati](#related-topics)

## <a name="implementing-ishellextinit"></a>Implementazione di IShellExtInit

Quando viene creata un'istanza dell'oggetto COM dell'estensione della finestra delle proprietà, viene chiamato il metodo [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . **IShellExtInit:: Initialize** fornisce l'estensione della finestra delle proprietà con un oggetto [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) che contiene i dati relativi all'oggetto directory a cui viene applicata la finestra delle proprietà.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contiene i dati nel formato [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) . Il formato dati **CFSTR \_ DSOBJECTNAMES** è un **HGLOBAL** che contiene una struttura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) . La struttura **DSOBJECTNAMES** contiene i dati dell'oggetto directory a cui viene applicata l'estensione della finestra delle proprietà.

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contiene inoltre dati nel formato delle [**Opzioni di \_ visualizzazione delle \_ \_ specifiche \_ di CFSTR DS**](cfstr-ds-display-spec-options.md) . Il formato dei dati delle **\_ \_ \_ \_ Opzioni di visualizzazione di CFSTR DS** è un **HGLOBAL** che contiene una struttura [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) . **DSDISPLAYSPECOPTIONS** contiene i dati di configurazione per l'utilizzo da parte dell'estensione.

Se un valore diverso da **S \_ OK** viene restituito da [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), la finestra delle proprietà non viene visualizzata.

I parametri *pidlFolder* e *HkeyProgID* del metodo [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) non vengono usati.

Il puntatore [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) può essere salvato dall'estensione incrementando il conteggio dei riferimenti di **IDataObject**. Questa interfaccia deve essere rilasciata quando non è più necessaria.

## <a name="implementing-ishellpropsheetext"></a>Implementazione di IShellPropSheetExt

Dopo che [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) restituisce, viene chiamato il metodo [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) . L'estensione della finestra delle proprietà deve aggiungere la pagina o le pagine durante questo metodo. Una pagina delle proprietà viene creata riempiendo una struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) e quindi passando la struttura alla funzione [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . La pagina delle proprietà viene quindi aggiunta alla finestra delle proprietà chiamando la funzione di callback passata a **IShellPropSheetExt:: AddPages** nel parametro *lpfnAddPage* .

Se un valore diverso da **S \_ OK** viene restituito da [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages), la finestra delle proprietà non viene visualizzata.

Se l'estensione della finestra delle proprietà non è necessaria per aggiungere pagine alla finestra delle proprietà, non deve chiamare la funzione di callback passata a [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) nel parametro *lpfnAddPage* .

Il metodo [**IShellPropSheetExt:: ReplacePage**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) non viene utilizzato.

## <a name="passing-the-extension-object-to-the-property-page"></a>Passaggio dell'oggetto estensione alla pagina delle proprietà

L'oggetto estensione della finestra delle proprietà è indipendente dalla pagina delle proprietà. In molti casi, è preferibile poter usare l'oggetto di estensione, o un altro oggetto, dalla pagina delle proprietà. A tale scopo, impostare il membro **lParam** della struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) sul puntatore all'oggetto. La pagina delle proprietà può quindi recuperare questo valore quando elabora il messaggio [**WM \_ INITDIALOG**](../dlgbox/wm-initdialog.md) . Per una pagina delle proprietà, il parametro *lParam* del messaggio **WM \_ INITDIALOG** è un puntatore alla struttura **PROPSHEETPAGE** . Recuperare il puntatore all'oggetto eseguendo il cast del valore *lParam* del messaggio **WM \_ INITDIALOG** a un puntatore **PROPSHEETPAGE** e quindi recuperando il membro **lParam** della struttura **PROPSHEETPAGE** .

Nell'esempio di codice C++ riportato di seguito viene illustrato come passare un oggetto a una pagina delle proprietà.


```C++
case WM_INITDIALOG:
    {
        LPPROPSHEETPAGE pPage = (LPPROPSHEETPAGE)lParam;

        if(NULL != pPage)
        {
            CPropSheetExt *pPropSheetExt;
            pPropSheetExt = (CPropSheetExt*)pPage->lParam;

            if(pPropSheetExt)
            {
                return pPropSheetExt>OnInitDialog(wParam, lParam);
            }
        }
    }
    break;
```



Tenere presente che, dopo la chiamata di [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) , la finestra delle proprietà rilascerà l'oggetto estensione della finestra delle proprietà e non verrà mai riutilizzato. Questo significa che l'oggetto di estensione verrebbe eliminato prima della visualizzazione della pagina delle proprietà. Quando la pagina tenta di accedere al puntatore all'oggetto, la memoria viene liberata e il puntatore non sarà valido. Per risolvere il problema, incrementare il conteggio dei riferimenti per l'oggetto estensione quando viene aggiunta la pagina e quindi rilasciare l'oggetto quando la finestra di dialogo della pagina delle proprietà viene distrutta. Viene creato un altro problema perché la finestra di dialogo della pagina delle proprietà non viene creata fino alla prima visualizzazione della pagina. Se l'utente non seleziona mai la pagina di estensione, la pagina non viene mai creata ed eliminata definitivamente. In questo modo l'oggetto di estensione non verrà mai rilasciato, quindi si verificherà una perdita di memoria. Per evitare questo problema, implementare una funzione di callback della pagina delle proprietà. A tale scopo, aggiungere il **flag \_ USECALLBACK di PSP** al **membro dwFlags** della struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) e impostare il membro **PfnCallback** della struttura **PROPSHEETPAGE** sull'indirizzo della funzione [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) implementata. Quando la funzione **PropSheetPageProc** riceve la notifica di **\_ rilascio PSPCB** , il parametro *ppSP* di **PropSheetPageProc** contiene un puntatore alla struttura **PROPSHEETPAGE** . Il membro **lParam** della struttura **PROPSHEETPAGE** contiene il puntatore di estensione che può essere utilizzato per rilasciare l'oggetto.

Nell'esempio di codice C++ riportato di seguito viene illustrato come rilasciare un oggetto di estensione.


```C++
UINT CALLBACK CPropSheetExt::PageCallbackProc(  HWND hWnd,
                                                UINT uMsg,
                                                LPPROPSHEETPAGE ppsp)
{
    switch(uMsg)
    {
    case PSPCB_CREATE:
        // Must return TRUE to enable the page to be created.
        return TRUE;

    case PSPCB_RELEASE:
        {
            /*
            Release the object. This is called even if the page dialog box was 
            never actually created.
            */
            CPropSheetExt *pPropSheetExt = (CPropSheetExt*)ppsp->lParam;

            if(pPropSheetExt)
            {
                pPropSheetExt->Release();
            }
        }
        break;
    }

    return FALSE;
}
```



## <a name="working-with-the-notification-object"></a>Utilizzo dell'oggetto Notification

Poiché le pagine di estensione della finestra delle proprietà vengono visualizzate all'interno di una finestra delle proprietà creata da un componente sconosciuto all'estensione, è necessario utilizzare un "Manager" per gestire il trasferimento dei dati tra le pagine di estensione e la finestra delle proprietà. Questo "Manager" è denominato oggetto notifica. L'oggetto notifica funge da moderatore tra le singole pagine e la finestra delle proprietà.

Quando viene inizializzato l'oggetto estensione della finestra delle proprietà, l'estensione deve creare un oggetto notifica chiamando [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj), passando il [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) ottenuto da [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) e il nome dell'oggetto directory. Non è necessario incrementare il conteggio dei riferimenti dell'interfaccia **IDataObject** , perché l'oggetto notifica creato dalla funzione **ADsPropCreateNotifyObj** eseguirà questa operazione. L'handle dell'oggetto notifica fornito da **ADsPropCreateNotifyObj** deve essere salvato per un uso successivo. **ADsPropCreateNotifyObj** può essere chiamato durante **IShellExtInit:: Initialize** o [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages). Quando l'estensione della finestra delle proprietà viene arrestata, deve inviare un messaggio di [**\_ uscita di \_ notifica \_ di WM ADSPROP**](wm-adsprop-notify-exit.md) all'oggetto notifica. In questo modo l'oggetto notifica si distrugge automaticamente. Questa operazione viene eseguita meglio quando la funzione [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) riceve la notifica di **\_ rilascio di PSPCB** .

L'estensione della finestra delle proprietà può ottenere dati oltre a quelli forniti dal formato degli Appunti [**CFSTR \_ DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) chiamando [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo). Uno dei vantaggi dell'uso di **ADsPropGetInitInfo** è che fornisce un oggetto [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) usato per lavorare a livello di codice con l'oggetto directory.

> [!Note]  
> A differenza della maggior parte dei metodi e delle funzioni COM, [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) non incrementa il conteggio dei riferimenti per l'oggetto [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) . Il **IDirectoryObject** non deve essere rilasciato se il conteggio dei riferimenti viene incrementato manualmente.

 

Quando la pagina delle proprietà viene creata per la prima volta, l'estensione deve registrare la pagina con l'oggetto notifica chiamando [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) con l'handle di finestra della pagina.

[**ADsPropCheckIfWritable**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcheckifwritable) è una funzione di utilità che può essere utilizzata dall'estensione della finestra delle proprietà per determinare se è possibile scrivere una proprietà.

## <a name="miscellaneous"></a>Varie

L'handle della pagina delle proprietà viene passato alla routine della finestra di dialogo della pagina. La finestra delle proprietà è l'elemento padre diretto della pagina delle proprietà, quindi l'handle della finestra delle proprietà può essere ottenuto chiamando la funzione [**GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) con l'handle della pagina delle proprietà.

Quando viene modificato il contenuto della pagina di estensione, l'estensione deve usare la macro [**PropSheet \_ modificata**](/windows/win32/api/prsht/nf-prsht-propsheet_changed) per inviare una notifica alla finestra delle proprietà delle modifiche. Il pulsante Applica verrà abilitato dalla finestra delle proprietà.

## <a name="multiple-selection-property-sheets"></a>Finestre delle proprietà Multiple-Selection

Con i sistemi operativi Windows Server 2003 e versioni successive, i Active Directory snap-in MMC amministrativi supportano le estensioni della finestra delle proprietà per più oggetti directory. Queste finestre delle proprietà vengono visualizzate quando le proprietà vengono visualizzate per più di un elemento alla volta. La differenza principale tra un'estensione della finestra delle proprietà a selezione singola e un'estensione della finestra delle proprietà a selezione multipla è che la struttura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) fornita dal formato degli Appunti [**\_ DSOBJECTNAMES CFSTR**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) in [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) conterrà più di una struttura [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .

Quando viene creato l'oggetto notifica, un'estensione della finestra delle proprietà per più selezioni deve passare un nome univoco fornito dallo snap-in anziché un nome creato dall'estensione. Per ottenere il nome univoco, richiedere il formato degli Appunti [**\_ \_ MULTISELECTPROPPAGE di CFSTR DS**](cfstr-ds-multiselectproppage.md) dall' [**interfaccia IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) ottenuta da [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize). Questi dati sono **HGLOBAL** che contengono una stringa Unicode con terminazione null che rappresenta il nome univoco. Questo nome univoco viene quindi passato alla funzione [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) per creare l'oggetto notifica. La funzione di esempio **CreateADsNotificationObject** nel [codice di esempio per l'implementazione dell'oggetto com della finestra delle proprietà](example-code-for-implementation-of-the-property-sheet-com-object.md) illustra come eseguire questa operazione in modo corretto, oltre che essere compatibile con le versioni precedenti dello snap-in che non supportano le finestre delle proprietà a selezione multifunzione.

Per le finestre delle proprietà a selezione multipla, il sistema viene associato solo al primo oggetto nella matrice [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) . Per questo motivo, [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) fornisce solo gli attributi [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) e Write-able per il primo oggetto nella matrice. Gli altri oggetti nella matrice non sono associati a.

Un'estensione della finestra delle proprietà a selezione multipla è registrata nell'attributo [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .

## <a name="new-with-windows-server-2003"></a>Novità con Windows Server 2003

Di seguito sono riportate le nuove funzionalità di Windows Server 2003.

Se la pagina delle proprietà rileva un errore, è possibile chiamare [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) con i dati di errore appropriati. In **ADsPropSendErrorMessage** vengono archiviati tutti i messaggi di errore in una coda. Questi messaggi verranno visualizzati la volta successiva che viene chiamato [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) . Quando **ADsPropShowErrorDialog** restituisce, i messaggi in coda vengono eliminati.

Windows Server 2003 introduce la funzione [**ADsPropSetHwndWithTitle**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwndwithtitle) . Questa funzione è simile a [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd), ma include il titolo della pagina. In questo modo viene abilitata la finestra di dialogo di errore visualizzata da [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) per fornire dati più utili all'utente. Se l'estensione della finestra delle proprietà utilizza la funzione **ADsPropShowErrorDialog** , l'estensione deve utilizzare **ADsPropSetHwndWithTitle** anziché **ADsPropSetHwnd**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio per l'implementazione dell'oggetto COM della finestra delle proprietà](example-code-for-implementation-of-the-property-sheet-com-object.md)
</dt> </dl>

 

 