---
title: Finestre delle proprietà e pagine delle proprietà
description: Finestre delle proprietà e pagine delle proprietà
ms.assetid: 6bcd1c1c-9b66-4422-bb07-67a856b3295d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cc61d1e1ed0cb833632b6b627a0c683a3cb0e4
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "103885887"
---
# <a name="property-sheets-and-property-pages"></a>Finestre delle proprietà e pagine delle proprietà

Le proprietà di un oggetto sono esposte ai client come metodi tramite interfacce COM o l'implementazione **IDispatch** dell'oggetto, consentendo la modifica delle proprietà da parte di programmi che chiamano questi metodi. La tecnologia OLE delle pagine delle proprietà fornisce i mezzi per compilare un'interfaccia utente per le proprietà di un oggetto in base agli standard dell'interfaccia utente di Windows. Pertanto, le proprietà vengono esposte agli utenti finali. La finestra delle proprietà di un oggetto è una finestra di dialogo a schede in cui ogni scheda corrisponde a una pagina delle proprietà specifica. Il modello OLE per l'utilizzo delle pagine delle proprietà è costituito da queste funzionalità:

-   Ogni pagina delle proprietà è gestita da un oggetto in-process che implementa [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) o [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2). Ogni pagina viene identificata con il proprio CLSID univoco.
-   Un oggetto specifica il supporto per le pagine delle proprietà implementando [**ISpecifyPropertyPages**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages). Tramite questa interfaccia il chiamante può ottenere un elenco di CLSID che identificano le pagine delle proprietà specifiche supportate dall'oggetto. Se l'oggetto specifica un CLSID della pagina delle proprietà, l'oggetto deve essere in grado di ricevere le modifiche apportate alle proprietà dalla pagina delle proprietà.
-   Qualsiasi parte di codice (client o oggetto) che desidera visualizzare la finestra delle proprietà di un oggetto passa il puntatore [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) dell'oggetto (o una matrice se sono interessati più oggetti) insieme a una matrice di CLSID di pagina a [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) o [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), che crea la finestra di dialogo a schede.
-   La finestra di dialogo frame proprietà crea un'istanza di una singola istanza di ogni pagina delle proprietà, utilizzando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in ogni CLSID. Il frame della proprietà ottiene almeno un puntatore [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) per ogni pagina. Inoltre, tramite il frame viene creato un oggetto sito della pagina delle proprietà per ogni pagina. Ogni sito implementa [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) e questo puntatore viene passato a ogni pagina. La pagina comunica quindi con il sito tramite questo puntatore a interfaccia.
-   Ogni pagina viene inoltre resa nota dell'oggetto o degli oggetti per i quali è stato richiamato. ovvero il frame di proprietà passa i puntatori [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)degli oggetti a ogni pagina. Quando viene richiesto di applicare modifiche agli oggetti, ogni pagina esegue una query per il puntatore di interfaccia appropriato e passa nuovi valori di proprietà agli oggetti nel modo desiderato. Non esistono disposizioni sulla modalità di comunicazione.
-   Un oggetto può inoltre supportare l'esplorazione per proprietà tramite l'interfaccia [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) che consente all'oggetto di specificare quale proprietà deve ricevere lo stato attivo iniziale quando viene visualizzata la pagina delle proprietà e specificare le stringhe e i valori che possono essere visualizzati dal client nella propria interfaccia utente.

Queste funzionalità sono illustrate nel diagramma seguente:

![Diagramma che mostra le funzionalità delle finestre delle proprietà e delle pagine delle proprietà.](images/7ea02938-c2fc-4ad0-a8b1-25222ca890ea.png)

Queste interfacce sono definite come segue:

``` syntax
interface ISpecifyPropertyPages : IUnknown 
  { 
    HRESULT GetPages([out] CAUUID *pPages); 
  }; 
 
 
interface IPropertyPage : IUnknown 
  { 
    HRESULT SetPageSite([in] IPropertyPageSite *pPageSite); 
    HRESULT Activate([in] HWND hWndParent, [in] LPCRECT prc 
        , [in] BOOL bModal); 
    HRESULT Deactivate(void); 
    HRESULT GetPageInfo([out] PROPPAGEINFO *pPageInfo); 
    HRESULT SetObjects([in] ULONG cObjects 
        , [in, max_is(cObjects)] IUnknown **ppunk); 
    HRESULT Show([in] UINT nCmdShow); 
    HRESULT Move([in] LPCRECT prc); 
    HRESULT IsPageDirty(void); 
    HRESULT Apply(void); 
    HRESULT Help([in] LPCOLESTR pszHelpDir); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
interface IPropertyPageSite : IUnknown 
  { 
    HRESULT OnStatusChange([in] DWORD dwFlags); 
    HRESULT GetLocaleID([out] LCID *pLocaleID); 
    HRESULT GetPageContainer([out] IUnknown **ppUnk); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg); 
  } 
 
```

Il metodo [**ISpecifyPropertyPages:: GetPages**](/windows/desktop/api/OCIdl/nf-ocidl-ispecifypropertypages-getpages) restituisce una matrice conteggiata di valori UUID (Guid), ognuno dei quali descrive il CLSID di una pagina delle proprietà che l'oggetto desidera visualizzare. Chiunque richiama la finestra delle proprietà con [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) o [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) passa questa matrice alla funzione. Si noti che se il chiamante desidera visualizzare le pagine delle proprietà per più oggetti, deve passare solo l'intersezione degli elenchi CLSID di tutti gli oggetti a queste funzioni. In altre parole, il chiamante deve richiamare solo pagine delle proprietà comuni a tutti gli oggetti.

Inoltre, il chiamante passa anche i puntatori [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) agli oggetti interessati alle funzioni dell'API. Entrambe le funzioni API creano una finestra di dialogo del frame delle proprietà e creano un'istanza di un sito di pagina con [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) per ogni pagina che verrà caricata. Tramite questa interfaccia una pagina delle proprietà può:

-   Recuperare la lingua corrente utilizzata nella finestra delle proprietà tramite [**GetLocaleID**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getlocaleid).
-   Porre il frame per elaborare le sequenze di tasti tramite [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-translateaccelerator).
-   Inviare una notifica al frame delle modifiche nella pagina tramite [**OnStatusChange**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-onstatuschange).
-   Ottenere un puntatore a interfaccia per il frame stesso tramite [**GetPageContainer**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getpagecontainer), anche se al momento non sono state definite interfacce per il frame per questa funzione restituisce sempre E \_ NOTIMPL.

Il frame di proprietà crea un'istanza di ogni oggetto pagina delle proprietà e ottiene l'interfaccia [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) di ogni pagina. Tramite questa interfaccia il frame informa la pagina del sito della pagina ([**SetPageSite**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setpagesite)), recupera le dimensioni e le stringhe di pagina ([**GetPageInfo**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-getpageinfo)), passa i puntatori di interfaccia agli oggetti interessati [**(oggetti oggetti),**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setobjects)indica alla pagina quando creare ed eliminare definitivamente i controlli ([**attivare**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-activate) e [**disattivare**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-deactivate)), indica alla pagina di visualizzare o riposizionare se stesso ([**Mostra**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-show) e [**Sposta**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-move)), indicare alla pagina di applicare i valori correnti agli oggetti interessati ([**Apply**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-apply)), controllare lo stato dirty della pagina ([**IsPageDirty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-ispagedirty)), richiamare la guida ([**Guida**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-help)) e passare le sequenze di tasti alla pagina ([**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-translateaccelerator)).

Un oggetto può supportare anche l'esplorazione per proprietà, che fornisce:

1.  Un modo (tramite [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) e [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)) per specificare la proprietà sulla quale deve essere assegnata lo stato attivo iniziale quando una finestra delle proprietà viene visualizzata per la prima volta
2.  Un metodo (tramite [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)) per l'oggetto per specificare i valori predefiniti e le stringhe descrittive corrispondenti che possono essere visualizzate nell'interfaccia utente del client per le proprietà.

Un oggetto può scegliere di supportare (2) senza supportare (1), ad esempio quando l'oggetto non dispone di una finestra delle proprietà.

Le interfacce [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) e [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) sono definite come segue:

``` syntax
interface IPerPropertyBrowsing : IUnknown 
  { 
    HRESULT GetDisplayString([in] DISPID dispID, [out] BSTR *pbstr); 
    HRESULT MapPropertyToPage([in] DISPID dispID, [out] CLSID *pclsid); 
    HRESULT GetPredefinedStrings([in] DISPID dispID, [out] CALPOLESTR *pcaStringsOut, [out] CADWORD *pcaCookiesOut); 
    HRESULT GetPredefinedValue([in] DISPID dispID, [in] DWORD dwCookie, [out] VARIANT *pvarOut); 
  } 
 
interface IPropertyPage2 : IPropertyPage 
  { 
    HRESULT EditProperty([in] DISPID dispID); 
  } 
 
```

Per specificare il supporto per tali funzionalità, l'oggetto implementa [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing). Tramite questa interfaccia, il chiamante può richiedere le informazioni necessarie per ottenere l'esplorazione, ad esempio stringhe predefinite ([**GetPredefinedStrings**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings)) e valori ([**GetPredefinedValue**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue)), nonché una stringa di visualizzazione per una determinata proprietà ([**GetDisplayString**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getdisplaystring)).

Inoltre, il client può ottenere il CLSID della pagina delle proprietà che consente all'utente di modificare una determinata proprietà identificata con un DISPID ([**MapPropertyToPage**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-mappropertytopage)). Il client indica quindi al frame della proprietà di attivare inizialmente tale pagina passando il CLSID e il DISPID a [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect). Il frame attiva prima di tutto la pagina e passa il DISPID alla pagina tramite [**IPropertyPage2:: EditProperty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage2-editproperty). La pagina imposta quindi lo stato attivo sul campo di modifica della proprietà. In questo modo, un client può passare dal nome di una proprietà all'interno della propria interfaccia utente alla pagina delle proprietà in grado di modificare la proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pagine delle proprietà e finestre delle proprietà](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




