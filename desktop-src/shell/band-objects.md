---
description: La barra di Explorer è stata introdotta con Microsoft Internet Explorer 4,0 per fornire un'area di visualizzazione adiacente al riquadro del browser.
title: Creare barre di Explorer, barre degli strumenti e barre desktop personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b4adeaaf089c22bd3e1db3d60d552ccc3252545a
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104565045"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a>Creazione di barre di esplorazione personalizzate, bande di strumenti e bande da scrivania

La barra di Explorer è stata introdotta con Microsoft Internet Explorer 4,0 per fornire un'area di visualizzazione adiacente al riquadro del browser. Si tratta fondamentalmente di una finestra figlio all'interno della finestra di Windows Internet Explorer, che può essere utilizzata per visualizzare le informazioni e interagire con l'utente nello stesso modo. Le barre di Explorer vengono in genere visualizzate come riquadro verticale sul lato sinistro del riquadro del browser. Tuttavia, una barra di Explorer può essere visualizzata anche orizzontalmente, sotto il riquadro del browser.

![Screenshot che mostra le barre di Explorer verticali e orizzontali.](images/expl1.jpg)

Per la barra di Explorer è disponibile un'ampia gamma di possibili utilizzi. Gli utenti possono selezionare l'opzione che desidera visualizzare in diversi modi, inclusa la selezione dal sottomenu **barra di Explorer** del menu **Visualizza** oppure facendo clic su un pulsante della barra degli strumenti. Internet Explorer offre diverse barre di Explorer standard, tra cui Preferiti e ricerca.

Uno dei modi in cui è possibile personalizzare Internet Explorer consiste nell'aggiungere una barra di Explorer personalizzata. Quando viene implementato e registrato, viene aggiunto al sottomenu **barra di Explorer** del menu **Visualizza** . Quando viene selezionata dall'utente, l'area di visualizzazione della barra di Explorer può essere usata per visualizzare le informazioni e ottenere l'input dell'utente in modo molto simile a una normale finestra.

![screenshot delle barre di Explorer](images/expl2.jpg)

Per creare una barra di Explorer personalizzata, è necessario implementare e registrare un *oggetto band*. Gli oggetti band sono stati introdotti con la versione 4,71 della shell e forniscono funzionalità simili a quelle delle finestre normali. Tuttavia, poiché si tratta di oggetti Component Object Model (COM) e contenuti da Internet Explorer o dalla shell, vengono implementati in modo diverso. Per creare le barre di Esplora esempi visualizzate nella prima immagine, sono stati usati oggetti banda semplici. L'implementazione dell'esempio della barra di Explorer verticale verrà descritta in dettaglio in una sezione successiva.

## <a name="tool-bands"></a>Bande degli strumenti

Una *banda di strumenti* è un oggetto banda introdotto con Microsoft Internet Explorer 5 per supportare la funzionalità della barra degli strumenti di Windows radio. La barra degli strumenti di Internet Explorer è in realtà un [controllo Rebar](../controls/rebar-controls.md) che contiene diversi [controlli della barra degli strumenti](../controls/toolbar-control-reference.md). Creando una banda di strumenti, è possibile aggiungere una banda a tale controllo Rebar. Tuttavia, come le barre di Explorer, una fascia di strumenti è una finestra di utilizzo generico.

![screenshot delle bande degli strumenti](images/toolband1.jpg)

Gli utenti visualizzano una barra degli strumenti selezionandola dal sottomenu **barra degli strumenti** del menu **Visualizza** o dal menu di scelta rapida visualizzato facendo clic con il pulsante destro del mouse sull'area della barra degli strumenti.

## <a name="desk-bands"></a>Bande della scrivania

Gli oggetti banda possono essere usati anche per creare *bande del desk*. Sebbene l'implementazione di base sia simile a quella delle barre di Explorer, le bande della scrivania non sono correlate a Internet Explorer. Un gruppo di uffici è fondamentalmente un modo per creare una finestra ancorabile sul desktop. L'utente lo seleziona facendo clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliendo dal sottomenu **barre degli strumenti** .

![Screenshot che mostra un esempio di gruppo di scrivanie.](images/desk2.png)

Inizialmente, le bande della scrivania sono ancorate sulla barra delle applicazioni.

![Screenshot che mostra le bande della scrivania ancorate sulla barra delle applicazioni.](images/desk1.jpg)

L'utente può quindi trascinare la banda della scrivania sul desktop e verrà visualizzata come finestra normale.

![screenshot delle bande della scrivania](images/desk3.png)

## <a name="implementing-band-objects"></a>Implementazione di oggetti banda

Vengono illustrati gli argomenti seguenti.

-   [Nozioni fondamentali sugli oggetti band](#band-object-basics)
-   [Registrazione banda](#band-registration)
-   [Un semplice esempio di una barra di Explorer personalizzata](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a>Nozioni fondamentali sugli oggetti band

Sebbene possano essere utilizzati in modo molto simile alle normali finestre, gli oggetti band sono oggetti COM presenti all'interno di un contenitore. Le barre di Explorer sono contenute in Internet Explorer e le bande della scrivania sono contenute nella shell. Anche se svolgono funzioni diverse, l'implementazione di base è molto simile. La differenza principale consiste nel modo in cui l'oggetto banda viene registrato, che a sua volta controlla il tipo di oggetto e il relativo contenitore. In questa sezione vengono illustrati gli aspetti dell'implementazione comuni a tutti gli oggetti band. Per ulteriori dettagli sull'implementazione, vedere [un semplice esempio di una barra di Explorer personalizzata](#a-simple-example-of-a-custom-explorer-bar) .

Oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), tutti gli oggetti banda devono implementare le interfacce seguenti.

-   [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)

Oltre alla registrazione del relativo identificatore di classe (CLSID), è necessario registrare anche gli oggetti barra di esplorazione e banda scrivania per la categoria di componenti appropriata. La registrazione della categoria Component determina il tipo di oggetto e il relativo contenitore. Le bande degli strumenti usano una procedura di registrazione diversa e non hanno un identificatore di categoria (CATId). CATID per gli oggetti a tre bande che lo richiedono sono:



| Tipo di banda               | Categoria del componente |
|-------------------------|--------------------|
| Barra di esplorazione verticale   | InfoBand CATId \_    |
| Barra di esplorazione orizzontale | CommBand CATId \_    |
| Banda della scrivania               | DeskBand CATId \_    |



 

Per ulteriori informazioni su come registrare gli oggetti band, vedere [registrazione della banda](#band-registration) .

Se l'oggetto banda deve accettare l'input dell'utente, deve implementare anche [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject). Per aggiungere elementi al menu di scelta rapida per le bande della barra o della scrivania di Explorer, è necessario che l'oggetto banda esporti [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). Le bande degli strumenti non supportano i menu di scelta rapida.

Poiché gli oggetti band implementano una finestra figlio, devono implementare anche una routine della finestra per gestire la messaggistica di Windows.

Gli oggetti banda possono inviare comandi al contenitore tramite l'interfaccia [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) del contenitore. Per ottenere il puntatore all'interfaccia, chiamare il metodo [**IInputObjectSite:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del contenitore e richiedere l'IID di \_ IOleCommandTarget. Inviare quindi i comandi al contenitore con [**IOleCommandTarget:: Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec). Il gruppo di comandi è CGID \_ deskband. Quando viene chiamato il metodo [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) di un oggetto della banda, il contenitore usa il parametro *dwBandID* per assegnare all'oggetto banda un identificatore usato per tre dei comandi. Sono supportati quattro ID comando **IOleCommandTarget:: Exec** .

-   \_BANDINFOCHANGED dbid

    Le informazioni sulla banda sono state modificate. Impostare il parametro *pvaIn* sull'identificatore della banda ricevuto nella chiamata più recente a [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). Il contenitore chiamerà il metodo **IDeskBand:: GetBandInfo** dell'oggetto banda per richiedere le informazioni aggiornate.

-   \_MAXIMIZEBAND dbid

    Ingrandire la banda. Impostare il parametro *pvaIn* sull'identificatore della banda ricevuto nella chiamata più recente a [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).

-   \_SHOWONLY dbid

    Attivare o disattivare altre bande nel contenitore. Impostare il parametro *pvaIn* sul \_ tipo sconosciuto VT con uno dei valori seguenti:

    

    | Valore | Descrizione                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | pUnk  | Puntatore all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) dell'oggetto della banda. Tutte le altre bande della scrivania saranno nascoste. |
    | 0     | Nascondi tutte le bande della scrivania.                                                                                        |
    | 1     | Mostra tutte le bande della scrivania.                                                                                        |

    

     

-   \_PUSHCHEVRON dbid

    [Versione 5](versions.md). Visualizzare un menu con virgolette. Il contenitore Invia un messaggio [**RB \_ PUSHCHEVRON**](../controls/rb-pushchevron.md) e l'oggetto band riceve una notifica [RBN \_ CHEVRONPUSHED](../controls/rbn-chevronpushed.md) che richiede di visualizzare il menu della freccia di espansione. Impostare il parametro *nCmdexecopt* del metodo [**IOleCommandTarget:: Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) sull'identificatore della banda ricevuta nella chiamata più recente a [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). Impostare il parametro *pvaIn* del metodo **IOleCommandTarget:: Exec** sul tipo VT \_ I4 con un valore definito dall'applicazione. Viene passato nuovamente all'oggetto band come valore *lAppValue* della \_ notifica CHEVRONPUSHED RBN.

### <a name="band-registration"></a>Registrazione banda

Un oggetto banda deve essere registrato come server OLE in-process che supporta il threading dell'Apartment. Il valore predefinito per il server è una stringa di testo del menu. Per le barre di Explorer, questo verrà visualizzato nel sottomenu **barra di Explorer** del menu **visualizzazione** di Internet Explorer. Per le bande degli strumenti, verrà visualizzato nel sottomenu **barre degli strumenti** del menu **visualizzazione** di Internet Explorer. Per le bande della scrivania, questo verrà visualizzato nel sottomenu **barre degli strumenti** del menu di scelta rapida della barra delle applicazioni. Come per le risorse di menu, il posizionamento di una e commerciale (&) davanti a una lettera ne comporterà la sottolineatura e l'abilitazione delle scelte rapide da tastiera. Ad esempio, la stringa di menu per la barra di Explorer verticale mostrata nel primo grafico è "Sample &barra di esplorazione verticale".

Inizialmente, Internet Explorer recupera un'enumerazione degli oggetti barra di esplorazione registrati dal registro di sistema utilizzando le categorie di componenti. Per migliorare le prestazioni, l'enumerazione viene quindi memorizzata nella cache, causando la trascurazione delle barre di Explorer aggiunte successivamente. Per forzare la ricompilazione della cache da parte di Windows Internet Explorer e riconoscere una nuova barra di Explorer, eliminare le chiavi del registro di sistema seguenti durante la registrazione della nuova barra di Explorer:

**HKEY \_ Software \_ utente corrente** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** rimozione delle \\  \\ categorie di componenti per la **postinstallazione** \\  \\ **{00021493-0000-0000-C000-000000000046}** \\ **enum**

**HKEY \_ Software \_ utente corrente** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** rimozione delle \\  \\ categorie di componenti per la **postinstallazione** \\  \\ **{00021494-0000-0000-C000-000000000046}** \\ **enum**

> [!Note]  
> Poiché viene creata una cache della barra di Explorer per ogni utente, è possibile che l'applicazione di installazione debba enumerare tutti gli hive del registro di sistema utente o aggiungere uno stub per utente da eseguire quando l'utente accede per la prima volta.

 

In generale, la voce del registro di sistema di base per un oggetto banda verrà visualizzata come indicato di seguito.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

Le bande degli strumenti devono avere anche il CLSID dell'oggetto registrato in Internet Explorer. A tale scopo, assegnare un valore in **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Toolbar** denominato con il GUID CLSID dell'oggetto della banda di strumenti, come illustrato qui. Il valore dei dati viene ignorato, quindi il tipo di valore non è importante.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

Sono disponibili diversi valori facoltativi che possono essere aggiunti anche al registro di sistema. Ad esempio, il valore seguente è necessario se si desidera utilizzare la barra di Explorer per visualizzare il codice HTML. il valore visualizzato non è un esempio, ma il valore effettivo da utilizzare.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

Usato in combinazione con il valore riportato sopra, è necessario anche il seguente valore facoltativo se si vuole usare la barra di Explorer per visualizzare il codice HTML. Questo valore deve essere impostato sul percorso del file che contiene il contenuto HTML per la barra di Explorer.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

Un altro valore facoltativo definisce la larghezza o l'altezza predefinita della barra di Explorer, a seconda che sia rispettivamente verticale o orizzontale.

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

Il valore BarSize deve essere impostato sulla larghezza o sull'altezza della barra. Il valore richiede otto byte e viene inserito nel registro di sistema come valore binario. I primi quattro byte specificano le dimensioni in pixel, in formato esadecimale, a partire dal byte più a sinistra. Gli ultimi quattro byte sono riservati e devono essere impostati su zero.

Ad esempio, le voci del registro di sistema complete per una barra di Explorer con supporto HTML con una larghezza predefinita di 291 pixel (0x123) sono visualizzate qui.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

È possibile gestire la registrazione del CATId di un oggetto della banda a livello di codice. Creare un oggetto di gestione delle categorie di componenti (CLSID \_ StdComponentCategoriesMgr) e richiedere un puntatore alla relativa interfaccia [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) . Passare il CLSID dell'oggetto banda e il CATId a [**ICatRegister:: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).

### <a name="a-simple-example-of-a-custom-explorer-bar"></a>Un semplice esempio di una barra di Explorer personalizzata

In questo esempio viene illustrata l'implementazione della barra di esplorazione verticale di esempio illustrata nell'introduzione.

Di seguito è riportata la procedura di base per la creazione di una barra di Explorer personalizzata.

1.  [Implementare le funzioni necessarie per la dll](#dll-functions).
2.  [Implementare le interfacce COM richieste.](#required-interface-implementations)
3.  [Implementare le interfacce COM facoltative desiderate.](#optional-interface-implementations)
4.  [Registrare il CLSID dell'oggetto e, se necessario, la categoria Component.](#clsid-registration)
5.  Creare una finestra figlio di Internet Explorer, ridimensionata in base all'area di visualizzazione della barra di Explorer.
6.  [Utilizzare la finestra figlio per visualizzare le informazioni e interagire con l'utente.](#the-window-procedure)

L'implementazione molto semplice usata nell'esempio della barra di Explorer può essere effettivamente usata per entrambi i tipi di barra di Explorer o per un gruppo di uffici, semplicemente eseguendo la registrazione per la categoria di componenti appropriata. Le implementazioni più sofisticate dovranno essere personalizzate per il contenitore e l'area di visualizzazione del tipo di oggetto. Tuttavia, la maggior parte di questa personalizzazione può essere eseguita prendendo il codice di esempio ed estendendo il codice applicando tecniche di programmazione Windows Note alla finestra figlio. Ad esempio, è possibile aggiungere controlli per l'interazione dell'utente o grafica per una visualizzazione più dettagliata.

### <a name="dll-functions"></a>Funzioni DLL

Tutti e tre gli oggetti vengono inclusi in un pacchetto in una singola DLL, che espone le funzioni seguenti.

-   [**DllMain**](../dlls/dllmain.md)
-   [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

Le prime tre funzioni sono implementazioni standard e non verranno discusse qui. Anche l'implementazione della class factory è standard.

### <a name="required-interface-implementations"></a>Implementazioni dell'interfaccia obbligatorie

L'esempio della barra di Explorer verticale implementa le quattro interfacce necessarie: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)e [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) come parte della classe CExplorerBar. Le implementazioni del costruttore, del distruttore e di **IUnknown** sono semplici e non verranno discusse qui. Vedere il codice di esempio per i dettagli.

Le interfacce seguenti sono descritte in dettaglio.

-   [IObjectWithSite](#iobjectwithsite)
-   [IPersistStream](#ipersiststream)
-   [IDeskBand](#ideskband)

### <a name="iobjectwithsite"></a>IObjectWithSite

Quando l'utente seleziona una barra di Explorer, il contenitore chiama il metodo [**IObjectWithSite:: SESITE**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) dell'oggetto banda corrispondente. Il parametro *punkSite* verrà impostato sul puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del sito.

In generale, un'implementazione di [**sito Web**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) deve eseguire i passaggi seguenti:

1.  Rilascia qualsiasi puntatore al sito attualmente mantenuto.
2.  Se il puntatore passato a [**SESITE**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) è impostato su **null**, la banda viene rimossa. Il **sito** può restituire S \_ OK.
3.  Se il puntatore passato a [**SESITE**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) è diverso da **null**, viene impostato un nuovo sito. Il **sito** deve eseguire le operazioni seguenti:
    1.  Chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul sito per la relativa interfaccia [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) .
    2.  Chiamare [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) per ottenere l'handle della finestra padre. Salvare l'handle per un uso successivo. Rilasciare [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) se non è più necessario.
    3.  Creare la finestra dell'oggetto banda come elemento figlio della finestra ottenuta nel passaggio precedente. Non crearlo come finestra visibile.
    4.  Se l'oggetto band implementa [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul sito per la relativa interfaccia [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) . Archiviare il puntatore a questa interfaccia per utilizzarlo in un secondo momento.
    5.  Se tutti i passaggi hanno esito positivo, restituire S \_ OK. In caso contrario, restituisce il codice di errore definito da OLE che indica l'esito negativo.

L'esempio della barra di Explorer implementa il [**sito**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) nel modo seguente. Nel codice seguente *m \_ pSite* è una variabile membro privata che include il puntatore [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) e *m \_ hwndParent* include l'handle della finestra padre. In questo esempio viene gestita anche la creazione di finestre. Se la finestra non esiste, questo metodo crea la finestra della barra di Explorer come elemento figlio di dimensioni appropriate della finestra padre ottenuta da **SESITE**. L'handle della finestra figlio viene archiviato in *\_ HWND m*.


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



L'implementazione [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) dell'esempio esegue semplicemente il wrapping di una chiamata al metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del sito, usando il puntatore del sito salvato da [**SESITE**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a>IPersistStream

Internet Explorer chiamerà l'interfaccia [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) della barra di Explorer per consentire alla barra di Explorer di caricare o salvare i dati persistenti. Se non sono presenti dati persistenti, i metodi devono comunque restituire un codice di esito positivo. L'interfaccia **IPersistStream** eredita da [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), pertanto è necessario implementare cinque metodi.

-   [**IPersist:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [**IPersistStream:: IsDirty**](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [**IPersistStream:: Load**](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [**IPersistStream:: Save**](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [**IPersistStream:: GetSizeMax**](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

L'esempio della barra di Explorer non usa dati persistenti e ha solo un'implementazione minima di [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream). [**IPersist:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) restituisce il CLSID dell'oggetto (CLSID \_ SampleExplorerBar) e il resto restituisce S \_ OK, s \_ false o e \_ NOTIMPL.

### <a name="ideskband"></a>IDeskBand

L'interfaccia [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) è specifica per gli oggetti band. Oltre all'unico metodo, eredita da [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), che a sua volta eredita da [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).

Sono disponibili due metodi [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) : [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) e [**IOleWindow:: ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp). L'implementazione dell'esempio della barra di Explorer di **GetWindow** restituisce l'handle della finestra figlio della barra di Explorer, *\_ HWND m*. La Guida sensibile al contesto non è implementata, quindi **ContextSensitiveHelp** restituisce **E \_ NOTIMPL**.

L'interfaccia [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) ha tre metodi.

-   [**IDockingWindow::ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [**IDockingWindow::CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [**IDockingWindow::ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

Il metodo [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) non viene usato con alcun tipo di oggetto banda e deve sempre restituire e \_ NOTIMPL. Il metodo [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) Mostra o nasconde la finestra della barra di Explorer, a seconda del valore del parametro.


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



Il metodo [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) Elimina la finestra della barra di Explorer.


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



Il metodo rimanente, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), è specifico di **IDeskBand**. Internet Explorer lo usa per specificare l'identificatore e la modalità di visualizzazione della barra di Explorer. Internet Explorer può anche richiedere una o più informazioni dalla barra di Explorer riempiendo il membro **dwMask** della struttura [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) che viene passato come terzo parametro. **GetBandInfo** deve archiviare l'identificatore e la modalità di visualizzazione e compilare la struttura **DESKBANDINFO** con i dati richiesti. L'esempio della barra di Explorer implementa **GetBandInfo** , come illustrato nell'esempio di codice seguente.


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a>Implementazioni di interfaccia facoltative

Sono disponibili due interfacce che non sono necessarie, ma che possono essere utili per implementare: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) e [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). L'esempio della barra di Explorer implementa **IInputObject**. Per informazioni su come implementare **IContextMenu**, vedere la documentazione.

### <a name="iinputobject"></a>IInputObject

L'interfaccia [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) deve essere implementata se un oggetto banda accetta l'input dell'utente. Internet Explorer implementa [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) e utilizza **IInputObject** per mantenere lo stato attivo per l'input dell'utente quando dispone di più di una finestra contenuta. Sono disponibili tre metodi che devono essere implementati da una barra di Explorer.

-   [**IInputObject::UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [**IInputObject::HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [**IInputObject::TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

Internet Explorer chiama [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) per informare la barra di Explorer che viene attivata o disattivata. Quando attivato, l'esempio della barra di Explorer chiama [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) per impostare lo stato attivo sulla finestra.

Internet Explorer chiama [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) quando tenta di determinare la finestra con lo stato attivo. Se la finestra della barra di Explorer o uno dei relativi discendenti ha lo stato attivo, **HasFocusIO** deve restituire s \_ OK. In caso contrario, deve restituire S \_ false.

[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) consente all'oggetto di elaborare i tasti di scelta rapida. L'esempio della barra di Explorer non implementa questo metodo, pertanto restituisce S \_ false.

Di seguito è riportata l'implementazione della barra di esempio di [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) .


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a>Registrazione CLSID

Come per tutti gli oggetti COM, il CLSID della barra di Explorer deve essere registrato. Per il corretto funzionamento dell'oggetto con Internet Explorer, è necessario registrarlo anche per la categoria di componenti appropriata (CATId \_ InfoBand). La sezione di codice pertinente per la barra di Explorer è illustrata nell'esempio di codice seguente.


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



Per la registrazione degli oggetti band nell'esempio vengono utilizzate le normali procedure COM.

Oltre al CLSID, è necessario registrare anche il server dell'oggetto banda per una o più categorie di componenti. Si tratta in realtà della differenza principale nell'implementazione tra gli esempi di barre di Explorer verticali e orizzontali. Questo processo viene gestito creando un oggetto di gestione delle categorie di componenti (CLSID \_ StdComponentCategoriesMgr) e usando il metodo [**ICatRegister:: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) per registrare il server di oggetti della banda. In questo esempio, la registrazione della categoria Component viene gestita passando il CLSID dell'esempio della barra di Explorer e il CATId a una funzione privata,**RegisterComCat**, come illustrato nell'esempio di codice seguente.


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a>Routine della finestra

Poiché un oggetto band usa una finestra figlio per la visualizzazione, deve implementare una routine della finestra per gestire la messaggistica di Windows. L'esempio di band ha una funzionalità minima, quindi la routine della finestra gestisce solo cinque messaggi:

-   [**\_NCCREATE WM**](../winmsg/wm-nccreate.md)
-   [**\_disegno WM**](../gdi/wm-paint.md)
-   [**\_comando WM**](../menurc/wm-command.md)
-   [**\_stato attivo WM**](../inputdev/wm-setfocus.md)
-   [**\_KILLFOCUS WM**](../inputdev/wm-killfocus.md)

La procedura può essere facilmente espansa per ospitare messaggi aggiuntivi per supportare altre funzionalità.


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



Il \_ gestore di comandi WM restituisce semplicemente zero. Il \_ gestore di disegno WM crea la visualizzazione di testo semplice mostrata nell'esempio della barra di Explorer nell'introduzione.


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



I \_ gestori WM SetFocus e WM \_ KILLFOCUS indicano al sito una modifica dello stato attivo chiamando il metodo [**IInputObjectSite:: OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) del sito.


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



Gli oggetti band forniscono una soluzione flessibile e potente per estendere le funzionalità di Internet Explorer creando barre di esplorazione personalizzate. L'implementazione di un gruppo di scrivanie consente di estendere le funzionalità delle finestre normali. Sebbene sia necessaria una programmazione COM, viene in definitiva utilizzata per fornire una finestra figlio per l'interfaccia utente. Da qui, la maggior parte dell'implementazione può utilizzare tecniche di programmazione Windows note. Sebbene l'esempio illustrato in questo articolo abbia solo funzionalità limitate, illustra tutte le funzionalità necessarie di un oggetto banda e può essere prontamente esteso per creare un'interfaccia utente univoca e potente.

 

 
