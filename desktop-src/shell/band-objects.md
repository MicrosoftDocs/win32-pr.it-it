---
description: La barra di Explorer è stata introdotta con Microsoft Internet Explorer 4.0 per fornire un'area di visualizzazione adiacente al riquadro del browser.
title: Creare barre di Explorer, barre degli strumenti e barre desktop personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9a57cc5bc8afa3e973c6d4d99b8bcee186287a6c9278407b900f84500d7d0e51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118461742"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a>Creazione di barre di esplorazione personalizzate, bande degli strumenti e gruppi di supporto

La barra di Explorer è stata introdotta con Microsoft Internet Explorer 4.0 per fornire un'area di visualizzazione adiacente al riquadro del browser. Si tratta fondamentalmente di una finestra figlio all'interno della finestra Windows Internet Explorer e può essere usata per visualizzare informazioni e interagire con l'utente nello stesso modo. Le barre di Explorer vengono in genere visualizzate come riquadro verticale sul lato sinistro del riquadro del browser. Tuttavia, una barra di Explorer può essere visualizzata anche orizzontalmente, sotto il riquadro del browser.

![Screenshot che mostra le barre verticali e orizzontali di Explorer.](images/expl1.jpg)

È disponibile un'ampia gamma di usi possibili per la barra di Explorer. Gli utenti possono selezionare l'opzione da visualizzare in diversi modi, ad esempio selezionandola dal sottomenu Barra di **Explorer** del **menu** Visualizza o facendo clic su un pulsante della barra degli strumenti. Internet Explorer offre diverse barre di Explorer standard, tra cui Preferiti e Ricerca.

Uno dei modi in cui è possibile personalizzare Internet Explorer è l'aggiunta di una barra di Explorer personalizzata. Una volta implementato e registrato, verrà aggiunto al sottomenu **Barra** di Explorer **del** menu Visualizza. Se selezionata dall'utente, l'area di visualizzazione della barra di Explorer può essere usata per visualizzare le informazioni e ottenere l'input dell'utente in modo molto identico a una finestra normale.

![Screenshot delle barre di Explorer](images/expl2.jpg)

Per creare una barra di Explorer personalizzata, è necessario implementare e registrare un *oggetto banda*. Gli oggetti banda sono stati introdotti con la versione 4.71 della shell e offrono funzionalità simili a quelle delle finestre normali. Tuttavia, poiché sono oggetti Component Object Model (COM) e contenuti in Internet Explorer o shell, vengono implementati in modo leggermente diverso. Per creare le barre di explorer di esempio visualizzate nel primo grafico sono stati usati oggetti banda semplici. L'implementazione dell'esempio di barra verticale di Explorer verrà illustrata in dettaglio in una sezione successiva.

## <a name="tool-bands"></a>Bande degli strumenti

Una *banda strumenti* è un oggetto banda introdotto con Microsoft Internet Explorer 5 per supportare la funzionalità Windows della barra degli strumenti radio. La barra Internet Explorer barra degli strumenti è in realtà un [controllo Rebar](../controls/rebar-controls.md) che contiene diversi controlli [della barra degli strumenti](../controls/toolbar-control-reference.md). Creando una banda degli strumenti, è possibile aggiungere una banda al controllo Rebar. Tuttavia, come le barre di Explorer, una barra degli strumenti è una finestra per utilizzo generico.

![Screenshot delle bande degli strumenti](images/toolband1.jpg)

Gli utenti visualizzano una  barra degli strumenti selezionandola dal sottomenu Barre degli strumenti del **menu** Visualizza o dal menu di scelta rapida visualizzato facendo clic con il pulsante destro del mouse sull'area della barra degli strumenti.

## <a name="desk-bands"></a>Desk Bands

Gli oggetti banda possono essere usati anche per creare *gruppi di supporto*. Anche se l'implementazione di base è simile alle barre di Explorer, i gruppi di supporto non sono correlati Internet Explorer. Un gruppo di desk è fondamentalmente un modo per creare una finestra ancorabile sul desktop. L'utente la seleziona facendo clic con il pulsante destro del mouse sulla barra delle applicazioni e selezionandola dal sottomenu **Barre degli** strumenti.

![Screenshot che mostra un gruppo di desk di esempio.](images/desk2.png)

Inizialmente, i gruppi di supporto sono ancorati alla barra delle applicazioni.

![Screenshot che mostra i gruppi di supporto ancorati sulla barra delle applicazioni.](images/desk1.jpg)

L'utente può quindi trascinare la banda della postazione sul desktop e verrà visualizzata come finestra normale.

![screenshot dei gruppi di lavoro della postazione](images/desk3.png)

## <a name="implementing-band-objects"></a>Implementazione di oggetti banda

Vengono illustrati gli argomenti seguenti.

-   [Nozioni di base sull'oggetto Band](#band-object-basics)
-   [Registrazione di banda](#band-registration)
-   [Esempio semplice di una barra di Explorer personalizzata](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a>Nozioni di base sull'oggetto Band

Sebbene possano essere usati in modo molto simile alle normali finestre, gli oggetti banda sono oggetti COM presenti all'interno di un contenitore. Le barre di Explorer sono contenute Internet Explorer e i gruppi di supporto sono contenuti nella shell. Anche se servono funzioni diverse, l'implementazione di base è molto simile. La differenza principale consiste nel modo in cui viene registrato l'oggetto banda, che a sua volta controlla il tipo di oggetto e il relativo contenitore. In questa sezione vengono illustrati gli aspetti dell'implementazione comuni a tutti gli oggetti banda. Per [altri dettagli sull'implementazione,](#a-simple-example-of-a-custom-explorer-bar) vedere Un semplice esempio di barra di Explorer personalizzata.

Oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IClassFactory,**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)tutti gli oggetti banda devono implementare le interfacce seguenti.

-   [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**Ipersiststream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)

Oltre a registrare l'identificatore di classe (CLSID), è necessario registrare anche gli oggetti barra di Explorer e desk band per la categoria di componenti appropriata. La registrazione della categoria di componenti determina il tipo di oggetto e il relativo contenitore. Le bande degli strumenti usano una procedura di registrazione diversa e non dispongono di un identificatore di categoria (CATID). I CATID per i tre oggetti banda che li richiedono sono:



| Tipo di banda               | Categoria del componente |
|-------------------------|--------------------|
| Barra di Explorer verticale   | CATID \_ InfoBand    |
| Barra orizzontale di Explorer | CATID \_ CommBand    |
| Desk Band               | CATID \_ DeskBand    |



 

Per [altre informazioni su](#band-registration) come registrare gli oggetti banda, vedere Registrazione di banda.

Se l'oggetto banda deve accettare l'input dell'utente, deve implementare anche [**IInputObject.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) Per aggiungere elementi al menu di scelta rapida per la barra di Explorer o i gruppi di supporto, l'oggetto banda deve esportare [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). Le bande degli strumenti non supportano i menu di scelta rapida.

Poiché gli oggetti banda implementano una finestra figlio, devono implementare anche una routine della finestra per gestire la Windows messaggistica.

Gli oggetti banda possono inviare comandi al contenitore tramite [**l'interfaccia IOleCommandTarget del**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) contenitore. Per ottenere il puntatore a interfaccia, chiamare il metodo [**IInputObjectSite::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del contenitore e richiedere \_ l'IID IOleCommandTarget. È quindi possibile inviare comandi al contenitore [**con IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec). Il gruppo di comandi è CGID \_ DeskBand. Quando viene chiamato il metodo [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) di un oggetto banda, il contenitore usa il *parametro dwBandID* per assegnare all'oggetto banda un identificatore usato per tre dei comandi. Sono supportati quattro ID di **comando IOleCommandTarget::Exec.**

-   DBID \_ BANDINFOCHANGED

    Le informazioni della banda sono state modificate. Impostare il *parametro pvaIn* sull'identificatore di banda ricevuto nella chiamata più recente a [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). Il contenitore chiamerà il metodo **IDeskBand::GetBandInfo** dell'oggetto banda per richiedere le informazioni aggiornate.

-   DBID \_ MAXIMIZEBAND

    Ingrandire la banda. Impostare il *parametro pvaIn* sull'identificatore di banda ricevuto nella chiamata più recente a [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).

-   DBID \_ SHOWONLY

    Attivare o disattivare altre bande nel contenitore. Impostare il *parametro pvaIn* sul tipo VT \_ UNKNOWN con uno dei valori seguenti:

    

    | Valore | Descrizione                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | Punk  | Puntatore all'interfaccia [**IUnknown dell'oggetto**](/windows/win32/api/unknwn/nn-unknwn-iunknown) banda. Tutti gli altri gruppi di supporto verranno nascosti. |
    | 0     | Nascondere tutti i gruppi di supporto.                                                                                        |
    | 1     | Mostra tutti i gruppi di supporto.                                                                                        |

    

     

-   DBID \_ PUSHCHEVRON

    [Versione 5.](versions.md) Consente di visualizzare un menu con la barra di controllo. Il contenitore invia un messaggio [**RB \_ PUSHCHEVRON**](../controls/rb-pushchevron.md) e l'oggetto banda riceve una notifica [RBN \_ CHEVRONPUSHED](../controls/rbn-chevronpushed.md) che richiede di visualizzare il menu di sincronizzazione. Impostare il parametro *nCmdExecOpt* del metodo [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) sull'identificatore di banda ricevuto nella chiamata più recente a [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband). Impostare il parametro *pvaIn* del metodo **IOleCommandTarget::Exec** sul tipo VT \_ I4 con un valore definito dall'applicazione. Passa di nuovo all'oggetto banda come valore *lAppValue* della notifica RBN \_ CHEVRONPUSHED.

### <a name="band-registration"></a>Registrazione banda

Un oggetto banda deve essere registrato come server OLE in-process che supporta il threading apartment. Il valore predefinito per il server è una stringa di testo del menu. Per le barre di Explorer, verrà visualizzato nel sottomenu **Barra** di Explorer del **menu** Internet Explorer Visualizza. Per le bande degli strumenti, verrà visualizzato **nel** sottomenu Barre degli strumenti Internet Explorer **menu Visualizza.** Per le bande da tavolo, verrà visualizzato **nel** sottomenu Barre degli strumenti del menu di scelta rapida della barra delle applicazioni. Come per le risorse di menu, l'inserimento di una e commerciale (&) davanti a una lettera ne determina la sottolineatura e l'abilitazione dei tasti di scelta rapida. Ad esempio, la stringa di menu per la barra verticale di Explorer visualizzata nel primo elemento grafico è "Esempio &barra di Esplora risorse verticale".

Inizialmente, Internet Explorer un'enumerazione degli oggetti barra di Explorer registrati dal Registro di sistema usando le categorie di componenti. Per migliorare le prestazioni, questa enumerazione viene quindi memorizzata nella cache, facendo in modo che le barre di Explorer aggiunte successivamente siano ignorate. Per forzare Windows Internet Explorer ricompilare la cache e riconoscere una nuova barra di Explorer, eliminare le chiavi del Registro di sistema seguenti durante la registrazione della nuova barra di Explorer:

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **Discardable** \\ **PostSetup** \\ **Component Categories** \\ **{00021493-0000-0000-C000-000000000046}** \\ **Enum**

**HKEY \_ CURRENT \_ USER** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **Discardable** \\ **PostSetup** \\ **Component Categories** \\ **{00021494-0000-0000-C000-000000000046}** \\ **Enum**

> [!Note]  
> Poiché viene creata una cache della barra di Explorer per ogni utente, l'applicazione di installazione potrebbe dover enumerare tutti gli hive del Registro di sistema degli utenti o aggiungere uno stub per utente da eseguire al primo accesso dell'utente.

 

In generale, la voce del Registro di sistema di base per un oggetto banda verrà visualizzata come segue.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

Le bande degli strumenti devono anche avere il CLSID dell'oggetto registrato con Internet Explorer. A tale scopo, assegnare un valore in **HKEY \_ LOCAL \_ MACHINE** Software Microsoft Internet Explorer Toolbar denominato con il \\  \\  \\  \\  GUID CLSID dell'oggetto della banda di strumenti, come illustrato di seguito. Il valore dei dati viene ignorato, quindi il tipo di valore non è importante.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

Esistono diversi valori facoltativi che possono essere aggiunti anche al Registro di sistema. Ad esempio, il valore seguente è necessario se si vuole usare la barra di Explorer per visualizzare HTML Il valore visualizzato non è un esempio, ma il valore effettivo che deve essere usato.

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

Usato in combinazione con il valore illustrato in precedenza, è necessario anche il valore facoltativo seguente se si vuole usare la barra di Explorer per visualizzare il codice HTML. Questo valore deve essere impostato sul percorso del file che contiene il contenuto HTML per la barra di Explorer.

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

Il valore BarSize deve essere impostato sulla larghezza o sull'altezza della barra. Il valore richiede otto byte e viene inserito nel Registro di sistema come valore binario. I primi quattro byte specificano le dimensioni in pixel, in formato esadecimale, a partire dal byte più a sinistra. Gli ultimi quattro byte sono riservati e devono essere impostati su zero.

Ad esempio, le voci del Registro di sistema complete per una barra di Explorer con supporto HTML con una larghezza predefinita di 291 (0x123) pixel sono mostrate qui.

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

È possibile gestire la registrazione del CATID di un oggetto banda a livello di codice. Creare un oggetto di gestione delle categorie di componenti (CLSID \_ StdComponentCategoriesMgr) e richiedere un puntatore alla relativa [**interfaccia ICatRegister.**](/windows/win32/api/comcat/nn-comcat-icatregister) Passare il CLSID e il CATID dell'oggetto banda a [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).

### <a name="a-simple-example-of-a-custom-explorer-bar"></a>Esempio semplice di una barra di Esplora risorse personalizzata

Questo esempio illustra l'implementazione della barra di Explorer verticale di esempio illustrata nell'introduzione.

La procedura di base per la creazione di una barra di Explorer personalizzata è la seguente.

1.  [Implementare le funzioni necessarie per la DLL](#dll-functions).
2.  [Implementare le interfacce COM necessarie.](#required-interface-implementations)
3.  [Implementare le interfacce COM facoltative desiderate.](#optional-interface-implementations)
4.  [Registrare il CLSID dell'oggetto e, se necessario, la categoria di componenti.](#clsid-registration)
5.  Creare una finestra figlio di Internet Explorer ridimensionata in base all'area di visualizzazione della barra di Explorer.
6.  [Usare la finestra figlio per visualizzare le informazioni e interagire con l'utente.](#the-window-procedure)

L'implementazione molto semplice usata nell'esempio di barra di Explorer può essere effettivamente usata per un tipo di barra di Explorer o per una banda da tavolo, semplicemente registrando la barra per la categoria di componenti appropriata. Le implementazioni più sofisticate dovranno essere personalizzate per l'area di visualizzazione e il contenitore di ogni tipo di oggetto. Tuttavia, gran parte di questa personalizzazione può essere eseguita prendendo il codice di esempio ed estendendo il codice applicando tecniche di programmazione Windows familiari alla finestra figlio. Ad esempio, è possibile aggiungere controlli per l'interazione dell'utente o grafica per una visualizzazione più avanzata.

### <a name="dll-functions"></a>Funzioni DLL

Tutti e tre gli oggetti sono in pacchetto in una singola DLL, che espone le funzioni seguenti.

-   [**DllMain**](../dlls/dllmain.md)
-   [**Dllcanunloadnow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [**Dllgetclassobject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [**Dllregisterserver**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

Le prime tre funzioni sono implementazioni standard e non verranno illustrate qui. Anche l'implementazione di Class Factory è standard.

### <a name="required-interface-implementations"></a>Implementazioni dell'interfaccia necessarie

L'esempio di barra di Explorer verticale implementa le quattro interfacce necessarie: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)e [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) come parte della classe CExplorerBar. Le implementazioni del costruttore, del distruttore e **di IUnknown** sono semplici e non verranno discusse qui. Vedere il codice di esempio per i dettagli.

Le interfacce seguenti sono descritte in dettaglio.

-   [IObjectWithSite](#iobjectwithsite)
-   [Ipersiststream](#ipersiststream)
-   [IDeskBand](#ideskband)

### <a name="iobjectwithsite"></a>IObjectWithSite

Quando l'utente seleziona una barra di Explorer, il contenitore chiama il metodo [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) dell'oggetto banda corrispondente. Il *parametro punkSite* verrà impostato sul puntatore [**IUnknown del**](/windows/win32/api/unknwn/nn-unknwn-iunknown) sito.

In generale, [**un'implementazione di SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) deve eseguire la procedura seguente:

1.  Rilasciare qualsiasi puntatore del sito attualmente in uso.
2.  Se il puntatore passato a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) è impostato su **NULL,** la banda viene rimossa. **SetSite** può restituire S \_ OK.
3.  Se il puntatore passato a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) non è **NULL,** viene impostato un nuovo sito. **SetSite** deve eseguire le operazioni seguenti:
    1.  Chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) nel sito per [**l'interfaccia IOleWindow.**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)
    2.  Chiamare [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) per ottenere l'handle della finestra padre. Salvare l'handle per usarlo in un secondo momento. Rilasciare [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) se non è più necessario.
    3.  Creare la finestra dell'oggetto banda come figlio della finestra ottenuta nel passaggio precedente. Non crearlo come finestra visibile.
    4.  Se l'oggetto banda implementa [**IInputObject,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject)chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) nel sito per l'interfaccia [**IInputObjectSite.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) Archiviare il puntatore a questa interfaccia per usarlo in un secondo momento.
    5.  Se tutti i passaggi hanno esito positivo, restituire S \_ OK. In caso contrario, restituire il codice di errore definito da OLE che indica l'errore non riuscito.

L'esempio di barra di Explorer implementa [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) nel modo seguente. Nel codice seguente *m \_ pSite* è una variabile membro privata che contiene il puntatore [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) e *m \_ hwndParent* contiene l'handle della finestra padre. In questo esempio viene gestita anche la creazione di finestre. Se la finestra non esiste, questo metodo crea la finestra della barra di Explorer come elemento figlio di dimensioni appropriate della finestra padre ottenuta da **SetSite**. L'handle della finestra figlio viene archiviato in *m \_ hwnd*.


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



L'implementazione [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) dell'esempio esegue semplicemente il wrapping di una chiamata al metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del sito usando il puntatore del sito salvato [**da SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).


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



### <a name="ipersiststream"></a>Ipersiststream

Internet Explorer chiama l'interfaccia [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) della barra di Explorer per consentire alla barra di Explorer di caricare o salvare dati persistenti. Se non sono presenti dati persistenti, i metodi devono comunque restituire un codice di esito positivo. **L'interfaccia IPersistStream** eredita da [**IPersist,**](/windows/win32/api/objidl/nn-objidl-ipersist)quindi è necessario che siano implementati cinque metodi.

-   [**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [**IPersistStream::IsDirty**](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [**IPersistStream::Load**](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [**IPersistStream::Save**](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [**IPersistStream::GetSizeMax**](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

L'esempio di barra di Explorer non usa dati persistenti e ha solo un'implementazione minima [**di IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream). [**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) restituisce il CLSID dell'oggetto (CLSID SampleExplorerBar) e il resto restituisce S OK, S FALSE o \_ E \_ \_ \_ NOTIMPL.

### <a name="ideskband"></a>IDeskBand

[**L'interfaccia IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) è specifica per gli oggetti banda. Oltre al metodo , eredita da [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), che a sua volta eredita da [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).

Esistono due [**metodi IOleWindow:**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) e [**IOleWindow::ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp). L'implementazione di **GetWindow** dell'esempio di barra di Explorer restituisce l'handle della finestra figlio della barra di Explorer, *m \_ hwnd*. La Guida sensibile al contesto non viene implementata, quindi **ContextSensitiveHelp** restituisce **E \_ NOTIMPL**.

[**L'interfaccia IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) ha tre metodi.

-   [**IDockingWindow::ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [**IDockingWindow::CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [**IDockingWindow::ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

Il [**metodo ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) non viene usato con alcun tipo di oggetto banda e deve sempre restituire E \_ NOTIMPL. Il [**metodo ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) mostra o nasconde la finestra della barra di Explorer, a seconda del valore del relativo parametro.


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



Il [**metodo CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) elimina la finestra della barra di Explorer.


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



Il metodo rimanente, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), è specifico di **IDeskBand**. Internet Explorer usa per specificare l'identificatore e la modalità di visualizzazione della barra di Explorer. Internet Explorer richiedere una o più informazioni dalla barra di Explorer compilando il membro **dwMask** della struttura [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) passato come terzo parametro. **GetBandInfo deve** archiviare l'identificatore e la modalità di visualizzazione e riempire la **struttura DESKBANDINFO** con i dati richiesti. L'esempio di barra di Explorer implementa **GetBandInfo,** come illustrato nell'esempio di codice seguente.


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



### <a name="optional-interface-implementations"></a>Implementazioni facoltative dell'interfaccia

Esistono due interfacce che non sono necessarie, ma che possono essere utili per implementare: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) [**e IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu). L'esempio di barra di Explorer implementa **IInputObject**. Per informazioni su come implementare **IContextMenu,** vedere la documentazione .

### <a name="iinputobject"></a>IInputObject

[**L'interfaccia IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) deve essere implementata se un oggetto banda accetta l'input dell'utente. Internet Explorer implementa [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) e usa **IInputObject** per mantenere lo stato attivo dell'input utente appropriato quando ha più finestre contenute. Esistono tre metodi che devono essere implementati da una barra di Explorer.

-   [**IInputObject::UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [**IInputObject::HasFocusIo**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [**IInputObject::TranslateAcceleratorIo**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

Internet Explorer chiama [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) per informare la barra di Explorer che è in corso l'attivazione o la disattivazione. Quando è attivato, l'esempio di barra di Explorer chiama [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) per impostare lo stato attivo sulla relativa finestra.

Internet Explorer chiama [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) quando tenta di determinare quale finestra ha lo stato attivo. Se la finestra della barra di Explorer o uno dei relativi discendenti ha lo stato attivo, **HasFocusIO** deve restituire S \_ OK. In caso contrario, deve restituire S \_ FALSE.

[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) consente all'oggetto di elaborare i tasti di scelta rapida. L'esempio di barra di Explorer non implementa questo metodo, quindi restituisce S \_ FALSE.

L'implementazione di [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) della barra di esempio è la seguente.


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

Come per tutti gli oggetti COM, è necessario registrare il CLSID della barra di Explorer. Perché l'oggetto funzioni correttamente con Internet Explorer, deve essere registrato anche per la categoria di componenti appropriata (CATID \_ InfoBand). La sezione di codice pertinente per la barra di Explorer è illustrata nell'esempio di codice seguente.


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



La registrazione degli oggetti banda nell'esempio usa normali procedure COM.

Oltre al CLSID, il server oggetti banda deve essere registrato anche per una o più categorie di componenti. Questa è in realtà la differenza principale nell'implementazione tra gli esempi di barra di Explorer verticale e orizzontale. Questo processo viene gestito creando un oggetto di gestione delle categorie di componenti (CLSID \_ StdComponentCategoriesMgr) e usando il metodo [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) per registrare il server oggetti banda. In questo esempio la registrazione della categoria di componenti viene gestita passando il CLSID e il CATID dell'esempio di barra di Explorer a una funzione privata,**RegisterComCat,** come illustrato nell'esempio di codice seguente.


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



### <a name="the-window-procedure"></a>Procedura della finestra

Poiché un oggetto banda usa una finestra figlio per la relativa visualizzazione, deve implementare una routine della finestra per gestire la Windows messaggistica. L'esempio di banda ha funzionalità minime, quindi la routine della finestra gestisce solo cinque messaggi:

-   [**WM \_ NCCREATE**](../winmsg/wm-nccreate.md)
-   [**WM \_ PAINT**](../gdi/wm-paint.md)
-   [**COMANDO \_ WM**](../menurc/wm-command.md)
-   [**WM \_ SETFOCUS**](../inputdev/wm-setfocus.md)
-   [**WM \_ KILLFOCUS**](../inputdev/wm-killfocus.md)

La procedura può essere facilmente espansa per supportare messaggi aggiuntivi per supportare più funzionalità.


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



Il gestore WM \_ COMMAND restituisce semplicemente zero. Il gestore \_ WM PAINT crea la semplice visualizzazione del testo visualizzata nell'esempio barra di Explorer nell'introduzione.


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



I gestori WM SETFOCUS e WM KILLFOCUS informano il sito di una modifica dello stato attivo chiamando il metodo \_ \_ [**IInputObjectSite::OnFocusChangeIS del**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) sito.


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



Gli oggetti banda offrono un modo flessibile e potente per estendere le funzionalità di Internet Explorer creando barre di Explorer personalizzate. L'implementazione di una banda da tavolo consente di estendere le funzionalità delle finestre normali. Anche se è necessaria una certa programmazione COM, in definitiva serve a fornire una finestra figlio per l'interfaccia utente. Da qui, la maggior parte dell'implementazione può usare tecniche Windows di programmazione. Sebbene l'esempio qui illustrato abbia solo funzionalità limitate, illustra tutte le funzionalità necessarie di un oggetto banda e può essere facilmente esteso per creare un'interfaccia utente univoca e potente.

 

 
