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
ms.openlocfilehash: 2504c27bcf4703bb49a3e8620c287c30ae9017ab6e65345d003f2acb6c9b544e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187612"
---
# <a name="implementing-the-property-page-com-object"></a>Implementazione dell'oggetto COM della pagina delle proprietà

Un'estensione della finestra delle proprietà è un oggetto COM implementato come server in-process. L'estensione della finestra delle proprietà deve implementare le interfacce [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) e [**IShellPropSheetExt.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) Viene creata un'istanza di un'estensione della finestra delle proprietà quando l'utente visualizza la finestra delle proprietà per un oggetto di una classe per cui l'estensione della finestra delle proprietà è stata registrata nell'identificatore di visualizzazione della classe .

-   [Implementazione di IShellExtInit](#implementing-ishellextinit)
-   [Implementazione di IShellPropSheetExt](#implementing-ishellpropsheetext)
-   [Passaggio dell'oggetto estensione alla pagina delle proprietà](#passing-the-extension-object-to-the-property-page)
-   [Utilizzo dell'oggetto Notification](#working-with-the-notification-object)
-   [Varie](#miscellaneous)
-   [Finestre delle proprietà a selezione multipla](#multiple-selection-property-sheets)
-   [Novità di Windows Server 2003](#new-with-windows-server-2003)
-   [Argomenti correlati](#related-topics)

## <a name="implementing-ishellextinit"></a>Implementazione di IShellExtInit

Dopo aver creato un'istanza dell'oggetto COM di estensione della finestra delle proprietà, viene chiamato il metodo [**IShellExtInit::Initialize.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) **IShellExtInit::Initialize** fornisce l'estensione della finestra delle proprietà con un oggetto [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) che contiene i dati relativi all'oggetto directory applicato dalla finestra delle proprietà.

[**L'oggetto IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contiene dati nel [**formato \_ CFSTR DSOBJECTNAMES.**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) Il **formato dati \_ CFSTR DSOBJECTNAMES** è **un HGLOBAL** che contiene una [**struttura DSOBJECTNAMES.**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) La **struttura DSOBJECTNAMES contiene i** dati dell'oggetto directory a cui si applica l'estensione della finestra delle proprietà.

[**L'oggetto IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) contiene anche dati nel formato [**CFSTR \_ DS \_ DISPLAY SPEC \_ \_ OPTIONS.**](cfstr-ds-display-spec-options.md) Il **formato dati CFSTR \_ DS DISPLAY SPEC \_ \_ \_ OPTIONS** è un **formato HGLOBAL** che contiene una struttura [**DSDISPLAYSPECOPTIONS.**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) **DSDISPLAYSPECOPTIONS contiene i** dati di configurazione per l'uso da parte dell'estensione.

Se un valore diverso da **S \_ OK** viene restituito da [**IShellExtInit::Initialize,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)la finestra delle proprietà non viene visualizzata.

I *parametri pidlFolder* *e hkeyProgID* del metodo [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) non vengono usati.

Il [**puntatore IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) può essere salvato dall'estensione incrementando il conteggio dei riferimenti di **IDataObject**. Questa interfaccia deve essere rilasciata quando non è più necessaria.

## <a name="implementing-ishellpropsheetext"></a>Implementazione di IShellPropSheetExt

Al [**termine dell'esecuzione di IShellExtInit::Initialize,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) viene chiamato il metodo [**IShellPropSheetExt::AddPages.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) L'estensione della finestra delle proprietà deve aggiungere la pagina o le pagine durante questo metodo. Una pagina delle proprietà viene creata compilando una [**struttura PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) e quindi passando questa struttura alla [**funzione CreatePropertySheetPage.**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) La pagina delle proprietà viene quindi aggiunta alla finestra delle proprietà chiamando la funzione di callback passata a **IShellPropSheetExt::AddPages** nel *parametro lpfnAddPage.*

Se un valore diverso da **S \_ OK** viene restituito da [**IShellPropSheetExt::AddPages,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)la finestra delle proprietà non viene visualizzata.

Se l'estensione della finestra delle proprietà non è necessaria per aggiungere pagine alla finestra delle proprietà, non deve chiamare la funzione di callback passata a [**IShellPropSheetExt::AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) nel parametro *lpfnAddPage.*

Il [**metodo IShellPropSheetExt::ReplacePage**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) non viene usato.

## <a name="passing-the-extension-object-to-the-property-page"></a>Passaggio dell'oggetto estensione alla pagina delle proprietà

L'oggetto estensione della finestra delle proprietà è indipendente dalla pagina delle proprietà. In molti casi, è consigliabile poter usare l'oggetto estensione o un altro oggetto dalla pagina delle proprietà. A tale scopo, impostare il **membro lParam** della [**struttura PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) sul puntatore all'oggetto. La pagina delle proprietà può quindi recuperare questo valore quando elabora il [**messaggio \_ WM INITDIALOG.**](../dlgbox/wm-initdialog.md) Per una pagina delle proprietà, *il parametro lParam* del messaggio **WM \_ INITDIALOG** è un puntatore alla **struttura PROPSHEETPAGE.** Recuperare il puntatore all'oggetto eseguendo il cast dell'oggetto *lParam* del messaggio **WM \_ INITDIALOG** a un **puntatore PROPSHEETPAGE** e quindi recuperando il membro **lParam** della **struttura PROPSHEETPAGE.**

Nell'esempio di codice C++ seguente viene illustrato come passare un oggetto a una pagina delle proprietà.


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



Tenere presente che dopo la chiamata a [**IShellPropSheetExt::AddPages,**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) la finestra delle proprietà rilascerà l'oggetto estensione della finestra delle proprietà e non lo userà mai più. Ciò significa che l'oggetto estensione verrà eliminato prima che venga visualizzata la pagina delle proprietà. Quando la pagina tenta di accedere al puntatore all'oggetto, la memoria sarà stata liberata e il puntatore non sarà valido. Per risolvere il problema, incrementare il conteggio dei riferimenti per l'oggetto estensione quando viene aggiunta la pagina e quindi rilasciare l'oggetto quando la finestra di dialogo della pagina delle proprietà viene distrutta. Ciò crea un altro problema perché la finestra di dialogo della pagina delle proprietà non viene creata fino alla prima visualizzazione della pagina. Se l'utente non seleziona mai la pagina dell'estensione, la pagina non viene mai creata ed distrutta. In questo modo l'oggetto estensione non viene mai rilasciato, quindi si verifica una perdita di memoria. Per evitare questo problema, implementare una funzione di callback della pagina delle proprietà. A tale scopo, aggiungere il flag **\_ PSP USECALLBACK** al membro **dwFlags** della struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) e impostare il membro **pfnCallback** della **struttura PROPSHEETPAGE** sull'indirizzo della funzione [**PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) implementata. Quando la **funzione PropSheetPageProc** riceve la notifica **PSPCB \_ RELEASE,** il parametro *ppsp* di **PropSheetPageProc** contiene un puntatore alla **struttura PROPSHEETPAGE.** Il **membro lParam** della struttura **PROPSHEETPAGE** contiene il puntatore di estensione che può essere usato per rilasciare l'oggetto.

Nell'esempio di codice C++ seguente viene illustrato come rilasciare un oggetto estensione.


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

Poiché le pagine di estensione della finestra delle proprietà vengono visualizzate all'interno di una finestra delle proprietà creata da un componente sconosciuto all'estensione, è necessario usare un "gestore" per gestire il trasferimento dei dati tra le pagine dell'estensione e la finestra delle proprietà. Questo "manager" viene chiamato oggetto notifica. L'oggetto notifica opera come moderatore tra le singole pagine e la finestra delle proprietà.

Quando l'oggetto estensione della finestra delle proprietà viene inizializzato, l'estensione deve creare un oggetto notifica chiamando [**ADsPropCreateNotifyObj,**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)passando [**l'oggetto IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) ottenuto da [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) e il nome dell'oggetto directory. Non è necessario incrementare il conteggio dei riferimenti dell'interfaccia **IDataObject,** perché l'oggetto notifica creato dalla funzione **ADsPropCreateNotifyObj** lo farà. L'handle dell'oggetto notifica fornito da **ADsPropCreateNotifyObj** deve essere salvato per un uso successivo. **ADsPropCreateNotifyObj** può essere chiamato durante **IShellExtInit::Initialize** o [**IShellPropSheetExt::AddPages.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) Quando l'estensione della finestra delle proprietà viene arrestata, deve inviare un messaggio [**WM \_ ADSPROP \_ NOTIFY \_ EXIT**](wm-adsprop-notify-exit.md) all'oggetto notifica. In questo modo l'oggetto notifica viene eliminato automaticamente. Questa operazione è ottimale quando la [**funzione PropSheetPageProc**](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) riceve la **notifica PSPCB \_ RELEASE.**

L'estensione della finestra delle proprietà può ottenere dati oltre a quello fornito dal formato degli Appunti [**\_ CFSTR DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) chiamando [**ADsPropGetInitInfo.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) Uno dei vantaggi dell'uso di **ADsPropGetInitInfo** è che fornisce un [**oggetto IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) usato per lavorare a livello di codice con l'oggetto directory.

> [!Note]  
> A differenza della maggior parte dei metodi e delle funzioni COM, [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) non incrementa il conteggio dei riferimenti per [**l'oggetto IDirectoryObject.**](/windows/desktop/api/iads/nn-iads-idirectoryobject) **L'oggetto IDirectoryObject** non deve essere rilasciato a meno che il conteggio dei riferimenti non venga incrementato manualmente per primo.

 

Quando la pagina delle proprietà viene creata per la prima volta, l'estensione deve registrare la pagina con l'oggetto notifica chiamando [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) con l'handle della finestra della pagina.

[**ADsPropCheckIfWritable**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcheckifwritable) è una funzione di utilità che l'estensione della finestra delle proprietà può usare per determinare se è possibile scrivere una proprietà.

## <a name="miscellaneous"></a>Varie

L'handle della pagina delle proprietà viene passato alla routine della finestra di dialogo della pagina. La finestra delle proprietà è l'elemento padre diretto della pagina delle proprietà, quindi l'handle della finestra delle proprietà può essere ottenuto chiamando la [**funzione GetParent**](/windows/win32/api/winuser/nf-winuser-getparent) con l'handle della pagina delle proprietà.

Quando il contenuto della pagina dell'estensione cambia, l'estensione deve usare la macro [**PropSheet \_ Changed**](/windows/win32/api/prsht/nf-prsht-propsheet_changed) per notificare le modifiche alla finestra delle proprietà. La finestra delle proprietà abiliterà quindi il pulsante Applica.

## <a name="multiple-selection-property-sheets"></a>Multiple-Selection proprietà

Con Windows Server 2003 e versioni successive, gli snap-in MMC amministrativi di Active Directory supportano le estensioni della finestra delle proprietà per più oggetti directory. Queste finestre delle proprietà vengono visualizzate quando le proprietà vengono visualizzate per più di un elemento alla volta. La differenza principale tra un'estensione della finestra delle proprietà a selezione singola e un'estensione della finestra delle proprietà a selezione multipla è che la struttura [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) fornita dal formato degli Appunti [**\_ CFSTR DSOBJECTNAMES**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) in [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) conterrà più di una struttura [**DSOBJECT.**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)

Quando viene creato l'oggetto notifica, un'estensione della finestra delle proprietà a selezione multipla deve passare un nome univoco fornito dallo snap-in anziché un nome creato dall'estensione. Per ottenere il nome univoco, richiedere il formato degli Appunti [**CFSTR \_ DS \_ MULTISELECTPROPPAGE**](cfstr-ds-multiselectproppage.md) dall'oggetto [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) ottenuto da [**IShellExtInit::Initialize.**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) Questi dati sono **HGLOBAL** che contiene una stringa Unicode con terminazione Null che rappresenta il nome univoco. Questo nome univoco viene quindi passato alla [**funzione ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) per creare l'oggetto notifica. La funzione di esempio **CreateADsNotificationObject** nel codice di esempio per l'implementazione dell'oggetto [COM](example-code-for-implementation-of-the-property-sheet-com-object.md) della finestra delle proprietà illustra come eseguire correttamente questa operazione, oltre a essere compatibile con le versioni precedenti dello snap-in che non supportano le finestre delle proprietà a selezione multipla.

Per le finestre delle proprietà a selezione multipla, il sistema esegue l'associazione solo al primo oggetto nella [**matrice DSOBJECT.**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) Per questo problema, [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) fornisce solo gli attributi [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) e di scrittura per il primo oggetto nella matrice. Gli altri oggetti nella matrice non sono associati.

Un'estensione della finestra delle proprietà a selezione multipla viene registrata con [**l'attributo adminMultiselectPropertyPages.**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages)

## <a name="new-with-windows-server-2003"></a>Novità di Windows Server 2003

Le funzionalità seguenti sono nuove di Windows Server 2003.

Se la pagina delle proprietà rileva un errore, è possibile chiamare [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) con i dati di errore appropriati. **ADsPropSendErrorMessage** archivierà tutti i messaggi di errore in una coda. Questi messaggi verranno visualizzati alla successiva chiamata [**di ADsPropShowErrorDialog.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) Quando **ADsPropShowErrorDialog** restituisce il controllo, i messaggi in coda vengono eliminati.

Windows Server 2003 introduce la [**funzione ADsPropSetHwndWithTitle.**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwndwithtitle) Questa funzione è simile ad [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd), ma include il titolo della pagina. Ciò consente alla finestra di dialogo di errore visualizzata da [**ADsPropShowErrorDialog di**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) fornire dati più utili all'utente. Se l'estensione della finestra delle proprietà usa la funzione **ADsPropShowErrorDialog,** l'estensione deve usare **ADsPropSetHwndWithTitle** anziché **ADsPropSetHwnd**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio per l'implementazione dell'oggetto COM della finestra delle proprietà](example-code-for-implementation-of-the-property-sheet-com-object.md)
</dt> </dl>

 

 