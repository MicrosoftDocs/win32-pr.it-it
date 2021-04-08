---
title: Finestre delle proprietà Active Directory utenti e computer
description: Lo snap-in MMC utenti e computer Active Directory è progettato per visualizzare una finestra delle proprietà per vari oggetti in un server Active Directory.
ms.assetid: 38032d89-9549-475c-90aa-dac5cfe11084
ms.tgt_platform: multiple
keywords:
- Active Directory finestre delle proprietà utenti e computer AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ea24f34e86f21af178e975852accb667bb69e4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724666"
---
# <a name="active-directory-users-and-computers-property-sheets"></a>Finestre delle proprietà Active Directory utenti e computer

Lo snap-in MMC utenti e computer Active Directory è progettato per visualizzare una finestra delle proprietà per vari oggetti in un server Active Directory. La finestra delle proprietà contiene una o più pagine utilizzate per visualizzare e modificare i dati degli oggetti. Per i diversi tipi di oggetto sono visualizzati diversi set di pagine. Lo snap-in MMC utenti e computer Active Directory consente inoltre ai fornitori di terze parti di aggiungere pagine personalizzate alla finestra delle proprietà per un tipo specifico di oggetto. Per altre informazioni, vedere [pagine delle proprietà da usare con gli identificatori di visualizzazione](property-pages-for-use-with-display-specifiers.md).

Alcune applicazioni, diverse dallo snap-in MMC Active Directory utenti e computer, devono fornire all'utente la possibilità di visualizzare e modificare gli attributi per un oggetto in un server Active Directory. L'applicazione può implementare le proprie finestre delle proprietà, ma è preferibile offrire un'interfaccia utente coerente per ridurre la confusione e i tempi di apprendimento. Fortunatamente, lo snap-in MMC Active Directory utenti e computer consente a qualsiasi applicazione COM OLE di visualizzare una finestra delle proprietà per un oggetto identico alla finestra delle proprietà visualizzata dallo snap-in MMC utenti e computer Active Directory per lo stesso oggetto.

Per ulteriori informazioni e un esempio di codice che ospita una finestra delle proprietà Active Directory utenti e computer, vedere l'esempio PropSheetHost in Platform Software Development Kit (SDK).

## <a name="developer-audience"></a>Sviluppatori

In questa documentazione si presuppone che il lettore abbia familiarità con l'operazione COM e lo sviluppo di componenti con C++. Attualmente, non è possibile creare un'estensione della finestra delle proprietà Active Directory utilizzando Visual Basic.

## <a name="hosting-an-active-directory-users-and-computers-property-sheet"></a>Hosting di una finestra delle proprietà di utenti e computer Active Directory

**Per visualizzare una finestra delle proprietà per un oggetto in un server Active Directory**

1.  Creare una finestra che può essere utilizzata per elaborare i messaggi. Può trattarsi di una finestra esistente o di una finestra a scopo speciale. Questa operazione è nota come *finestra nascosta*.
2.  Creare un oggetto OLE COM derivato da [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject). Questo oggetto dati deve supportare i formati di dati seguenti:

    -   [**CFSTR \_ DSOBJECTNAMES**](cfstr-dsobjectnames.md) questo formato dati contiene un [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) che identifica l'oggetto a cui si applica la finestra delle proprietà. Quando si ospita una finestra delle proprietà, nell'elenco seguente vengono mostrati i membri più significativi della struttura **DSOBJECTNAMES** .

        **clsidNamespace** Riservati. Impostare questo valore su un GUID per l'applicazione nel caso in cui venga usato in futuro.
        
        **aObjects** Contiene una matrice di strutture [**DSBOJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) . Ogni struttura **DSBOJECT** rappresenta un singolo oggetto directory. Il membro **cItems** contiene il numero di elementi nella matrice. Viene utilizzato solo il primo oggetto in questa matrice. Gli altri oggetti vengono ignorati.

    -   [**CFSTR \_ DSDISPLAYSPECOPTIONS**](cfstr-ds-display-spec-options.md) questo formato dati contiene una struttura [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) che contiene i dati che verranno utilizzati dalle pagine delle proprietà, ad esempio la posizione in cui caricare le pagine delle proprietà, il server e le credenziali da utilizzare e così via. I membri più significativi di **DSDISPLAYSPECOPTIONS** sono indicati nell'elenco seguente.

        **offsetAttribPrefix** La stringa del prefisso dell'attributo determina la posizione in cui viene ottenuto l'elenco di pagine delle proprietà. Deve contenere una delle stringhe seguenti.

        

        | Stringa prefisso attributo | Descrizione                                              |
        |-------------------------|----------------------------------------------------------------------------------------------------------------------|
        | admin<br/>      | Le pagine delle proprietà vengono caricate dall'attributo [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) .<br/> |
        | Shell<br/>      | Le pagine delle proprietà vengono caricate dall'attributo [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) .<br/> |

        


    -   [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) questo formato dati contiene una struttura [**PROPSHEETCFG**](propsheetcfg.md) che contiene i dati dell'host della finestra delle proprietà. Quando si ospita una finestra delle proprietà, i membri più significativi della struttura **PROPSHEETCFG** contengono i dati mostrati nell'elenco seguente.

        **lNotifyHandle** Deve essere zero.
        **hwndParentSheet**  Contiene l'handle della finestra per ricevere i messaggi di notifica delle modifiche di [**WM \_ ADSPROP \_ \_**](wm-adsprop-notify-change.md) quando qualcosa in una delle pagine cambia e viene applicato. Può essere **null** se questo messaggio non è necessario.

        **hwndHidden** Contiene l'handle della finestra per la ricezione [**del \_ foglio DSA WM \_ \_ creare \_**](wm-dsa-sheet-create-notify.md) una notifica e la [**chiusura del foglio DSA WM messaggi di \_ \_ \_ \_ notifica**](wm-dsa-sheet-close-notify.md) . Impostarlo sull'handle della finestra nascosta.

        **wParamSheetClose** Contiene un identificatore definito dall'applicazione restituito in *wParam* nel messaggio di notifica di [**\_ chiusura del \_ foglio \_ \_ DSA WM**](wm-dsa-sheet-close-notify.md) . Se questo membro è zero, il messaggio di **\_ \_ \_ chiusura \_ del foglio DSA WM** non verrà inserito nella finestra nascosta.


3.  Creare un'istanza dell'oggetto [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) e ottenere l'interfaccia [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) per l'oggetto. È anche possibile duplicare il comportamento dell'oggetto **CLSID \_ DsPropertyPages** . Per ulteriori informazioni, vedere duplicazione del comportamento dell'oggetto CLSID \_ DsPropertyPages.
4.  Inizializzare l'oggetto [**\_ DsPropertyPages CLSID**](guids-of-user-interface-elements.md) chiamando il metodo [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . I parametri *pidlFolder* e *hkeyProgID* non vengono utilizzati in questo metodo. Il parametro *pdtobj* è il puntatore all'oggetto dati creato nel passaggio 2. Quando viene chiamato il metodo **IShellExtInit:: Initialize** , l' **oggetto \_ DsPropertyPages CLSID** salverà un riferimento all'oggetto dati.
5.  Ottenere l'interfaccia [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) per l'oggetto [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) e chiamare il metodo [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) . Il parametro *lpfnAddPage* è l'indirizzo di una funzione di callback che è necessario implementare. Il formato di questa funzione è illustrato di seguito. Se la funzione di callback viene dichiarata come membro di una classe C++, la funzione di callback deve essere dichiarata come **statica**. Il parametro *lParam* è un valore definito dall'applicazione che può essere utilizzato per identificare l'oggetto che implementa la funzione di callback. Quando viene chiamato il metodo **IShellPropSheetExt:: AddPages** , l'oggetto **CLSID \_ DsPropertyPages** otterrà i dati dall'oggetto dati ed enumera le pagine delle proprietà registrate per gli identificatori di visualizzazione dell'oggetto. L'oggetto **CLSID \_ DsPropertyPages** enumera quindi gli oggetti della pagina delle proprietà, chiamando il metodo **IShellPropSheetExt:: AddPages** di ciascun oggetto.

    ```C++
    BOOL CALLBACK AddPagesCallback(HPROPSHEETPAGE, LPARAM)
    ```

    

6.  Ogni pagina aggiunta dagli oggetti della pagina delle proprietà comporterà la chiamata della funzione di callback con l'handle per la pagina delle proprietà e il valore definito dall'applicazione. La funzione di callback deve archiviare ogni handle di pagina delle proprietà passato. Quando il metodo [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) dell'oggetto [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) restituisce, tutte le pagine sono state aggiunte tramite la funzione di callback.
7.  Compilare una struttura [**PROPSHEETHEADER**](/windows/win32/api/prsht/ns-prsht-propsheetheadera_v2) per visualizzare la finestra delle proprietà. Il membro **phpage** riceve un puntatore a una matrice di handle di pagina raccolti dalla funzione di callback. Il membro **nPages** riceve il numero di pagine nella matrice di handle di pagina.
8.  Consente di visualizzare la finestra delle proprietà chiamando la funzione [**PropertySheet**](/windows/win32/api/prsht/nf-prsht-propertysheeta) .

Se i dati in una pagina vengono modificati e si fa clic sui pulsanti **OK** o **applica** , la finestra identificata dal **membro hwndParentSheet** della struttura [**PROPSHEETCFG**](propsheetcfg.md) riceverà un messaggio di [**notifica di \_ \_ \_ modifica di WM ADSPROP**](wm-adsprop-notify-change.md) . Questo messaggio è esclusivamente una notifica e non richiede alcuna azione specifica.

Quando la pagina viene chiusa, la finestra identificata dal membro **hwndHidden** della struttura [**PROPSHEETCFG**](propsheetcfg.md) riceverà un messaggio [**di \_ \_ notifica di \_ chiusura \_ del foglio DSA WM**](wm-dsa-sheet-close-notify.md) . Questo messaggio è esclusivamente una notifica e non richiede l'esecuzione di un'azione specifica.

In alcuni casi, è necessario che nelle finestre delle proprietà esistenti venga visualizzata una finestra delle proprietà secondaria. Se, ad esempio, si visualizza la finestra delle proprietà per un oggetto utente e si seleziona il **membro della** pagina, verrà visualizzato un elenco di gruppi di cui l'utente è membro. Se si fa doppio clic su uno di questi gruppi nell'elenco, verrà visualizzata la finestra delle proprietà per tale gruppo. La finestra delle proprietà primaria non Visualizza il foglio secondario da solo. Richiede che l'host visualizzi il foglio secondario inviando il messaggio di  [**\_ \_ \_ \_ notifica di un foglio DSA WM**](wm-dsa-sheet-create-notify.md) alla finestra identificata dal membro hwndHidden della struttura [**PROPSHEETCFG**](propsheetcfg.md) . Il *wParam* del **\_ foglio DSA WM \_ \_ Crea \_ notifica** messaggio è un puntatore a una struttura [**di \_ \_ \_ informazioni della pagina DSA sec**](dsa-sec-page-info.md) che contiene informazioni sulla finestra delle proprietà secondaria e sull'oggetto che rappresenta. In risposta a questo messaggio, l'host della finestra delle proprietà deve visualizzare la finestra delle proprietà secondaria nello stesso modo illustrato in precedenza. Al termine dell'elaborazione del messaggio **WM \_ DSA \_ \_ Create \_ Notify** , il destinatario del messaggio deve liberare la struttura di **\_ informazioni della \_ pagina \_ DSA sec** passando il valore *wParam* alla funzione [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) .

## <a name="duplicating-the-behavior-of-the-clsid_dspropertypages-object"></a>Duplicazione del comportamento dell' \_ oggetto DSPROPERTYPAGES CLSID

**Per duplicare il comportamento dell' \_ oggetto DSPROPERTYPAGES CLSID**

1.  Enumerare i valori nell'attributo [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) o [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) per l'identificatore di visualizzazione per la classe di oggetti. Ogni valore è una stringa che contiene un numero, seguito da una virgola, seguita dalla rappresentazione di stringa dell'identificatore di classe dell'estensione della pagina delle proprietà. Per ulteriori informazioni sul formato delle pagine delle proprietà, vedere la pagina relativa alla [registrazione dell'oggetto com della pagina delle proprietà in un identificatore di visualizzazione](registering-the-property-page-com-object-in-a-display-specifier.md).
2.  Converte ogni stringa dell'identificatore di classe in un **CLSID** usando la funzione [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .
3.  Ordinare gli identificatori della classe di estensione in base al numero che precede ogni stringa dell'identificatore di classe nel valore dell'attributo. Se due numeri sono identici, ordinare gli identificatori di classe nell'ordine in cui i valori degli attributi vengono ottenuti dal server Active Directory.
4.  Enumerare gli identificatori della classe di estensione, creando un'istanza di ogni estensione.
5.  Per ogni estensione, nell'ordine ordinato in precedenza, chiamare l'estensione [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) con le stesse informazioni descritte nel passaggio 4 della procedura relativa alla finestra delle proprietà Hosting a Active Directory Users and Computers.
6.  Per ogni estensione, nell'ordine ordinato sopra, chiamare [**IShellPropSheetExt:: AddPages**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) dell'estensione con le stesse informazioni descritte nel passaggio 5 della procedura relativa alla finestra delle proprietà hosting di un Active Directory utenti e computer.

Se possibile, utilizzare l'oggetto [**CLSID \_ DsPropertyPages**](guids-of-user-interface-elements.md) per creare le pagine, anziché eseguire manualmente questa operazione. Il **CLSID \_ DsPropertyPages** è stato ottimizzato e gestirà correttamente i casi di errore, ad esempio quando non è disponibile alcun identificatore di visualizzazione per le impostazioni locali correnti. Inoltre, l' **oggetto \_ DsPropertyPages CLSID** potrebbe cambiare in futuro, il che significa che le finestre delle proprietà potrebbero non corrispondere esattamente a quelle visualizzate dallo snap-in MMC utenti e computer Active Directory.

## <a name="special-programming-elements"></a>Particolari elementi di programmazione

Attualmente, gli elementi di programmazione seguenti non sono definiti in un file di intestazione pubblicato. Per usare questi elementi, è necessario definirli nel formato esatto indicato nella pagina di riferimento specifica.

-   [**\_PROPSHEETCONFIG DS \_ CFSTR**](cfstr-ds-propsheetconfig.md)
-   [**PROPSHEETCFG**](propsheetcfg.md)
-   [**\_notifica di \_ chiusura del foglio DSA \_ WM \_**](wm-dsa-sheet-close-notify.md)
-   [**\_ \_ \_ creazione \_ notifica foglio DSA WM**](wm-dsa-sheet-create-notify.md)
-   [**\_ \_ informazioni pagina di DSA sec \_**](dsa-sec-page-info.md)

## <a name="example-code"></a>Codice di esempio

Nell'esempio di codice C++ riportato di seguito viene illustrato un modo sicuro per definire questi elementi che continueranno a funzionare anche se questi elementi sono definiti in un file di intestazione pubblicato in futuro.


```C++
#ifndef CFSTR_DS_PROPSHEETCONFIG
    #define CFSTR_DS_PROPSHEETCONFIG_W L"DsPropSheetCfgClipFormat"
    #define CFSTR_DS_PROPSHEETCONFIG_A "DsPropSheetCfgClipFormat"

    #ifdef UNICODE
        #define CFSTR_DS_PROPSHEETCONFIG CFSTR_DS_PROPSHEETCONFIG_W
    #else
        #define CFSTR_DS_PROPSHEETCONFIG CFSTR_DS_PROPSHEETCONFIG_A
    #endif //UNICODE
#endif //CFSTR_DS_PROPSHEETCONFIG


#ifndef WM_ADSPROP_SHEET_CREATE
    #define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
#endif


#ifndef WM_DSA_SHEET_CREATE_NOTIFY
    #define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
#endif


#ifndef WM_DSA_SHEET_CLOSE_NOTIFY
    #define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5) 
#endif


#ifndef DSA_SEC_PAGE_INFO
    typedef struct _DSA_SEC_PAGE_INFO
    {
        HWND    hwndParentSheet;
        DWORD   offsetTitle;
        DSOBJECTNAMES dsObjectNames;
    } DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
#endif //DSA_SEC_PAGE_INFO

#ifndef PROPSHEETCFG
    typedef struct _PROPSHEETCFG
    {  
        LONG_PTR lNotifyHandle;  
        HWND hwndParentSheet;  
        HWND hwndHidden;  
        WPARAM wParamSheetClose;
    } PROPSHEETCFG, *PPROPSHEETCFG;
#endif //PROPSHEETCFG
```



 

