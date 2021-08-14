---
title: Finestre delle proprietà e pagine delle proprietà
description: Finestre delle proprietà e pagine delle proprietà
ms.assetid: 6bcd1c1c-9b66-4422-bb07-67a856b3295d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7991ea650838e9980292257c14d26909e9476f0f35422fa21deab2b0b5ecbbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104935"
---
# <a name="property-sheets-and-property-pages"></a>Finestre delle proprietà e pagine delle proprietà

Le proprietà di un oggetto vengono esposte ai client come i metodi tramite le interfacce COM o l'implementazione **IDispatch** dell'oggetto, consentendo la modifica delle proprietà da parte dei programmi che chiamano questi metodi. La tecnologia OLE delle pagine delle proprietà fornisce i mezzi per compilare un'interfaccia utente per le proprietà di un oggetto in base Windows standard dell'interfaccia utente. Di conseguenza, le proprietà vengono esposte agli utenti finali. La finestra delle proprietà di un oggetto è una finestra di dialogo a schede in cui ogni scheda corrisponde a una pagina delle proprietà specifica. Il modello OLE per l'utilizzo delle pagine delle proprietà è costituito da queste funzionalità:

-   Ogni pagina delle proprietà è gestita da un oggetto in-process che implementa [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) o [**IPropertyPage2.**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) Ogni pagina viene identificata con il proprio CLSID univoco.
-   Un oggetto specifica il supporto per le pagine delle proprietà implementando [**ISpecifyPropertyPages.**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages) Tramite questa interfaccia il chiamante può ottenere un elenco di CLSID che identificano le pagine delle proprietà specifiche supportate dall'oggetto. Se l'oggetto specifica un CLSID della pagina delle proprietà, l'oggetto deve essere in grado di ricevere le modifiche delle proprietà dalla pagina delle proprietà.
-   Qualsiasi parte di codice (client o oggetto) che vuole visualizzare la finestra delle proprietà di un oggetto passa il puntatore [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) dell'oggetto (o una matrice se sono interessati più oggetti) insieme a una matrice di CLSID di pagina a [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) o [**OleCreatePropertyFrameIndirect,**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect)che crea la finestra di dialogo a schede.
-   La finestra di dialogo dei frame di proprietà crea un'istanza singola di ogni pagina delle proprietà, usando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in ogni CLSID. Il frame di proprietà ottiene almeno un puntatore [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) per ogni pagina. Inoltre, il frame crea un oggetto sito della pagina delle proprietà per ogni pagina. Ogni sito implementa [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) e questo puntatore viene passato a ogni pagina. La pagina comunica quindi con il sito tramite questo puntatore di interfaccia.
-   Ogni pagina viene inoltre resa a conoscenza dell'oggetto o degli oggetti per i quali è stata richiamata; ciò significa che il frame di proprietà passa i puntatori [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)degli oggetti a ogni pagina. Quando viene richiesto di applicare le modifiche agli oggetti, ogni pagina esegue una query per il puntatore di interfaccia appropriato e passa i nuovi valori delle proprietà agli oggetti nel modo desiderato. Non sono presenti condizioni su come deve avvenire tale comunicazione.
-   Un oggetto può anche supportare l'esplorazione per proprietà tramite l'interfaccia [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) che consente all'oggetto di specificare quale proprietà deve ricevere lo stato attivo iniziale quando viene visualizzata la pagina delle proprietà e di specificare stringhe e valori che possono essere visualizzati dal client nella propria interfaccia utente.

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

Il [**metodo ISpecifyPropertyPages::GetPages**](/windows/desktop/api/OCIdl/nf-ocidl-ispecifypropertypages-getpages) restituisce una matrice conteggiata di valori UUID (GUID), ognuno dei quali descrive il CLSID di una pagina delle proprietà che l'oggetto deve visualizzare. Chiunque richiama la finestra delle proprietà con [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) o [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) passa questa matrice alla funzione . Si noti che se il chiamante vuole visualizzare le pagine delle proprietà per più oggetti, deve passare solo l'intersezione degli elenchi CLSID di tutti gli oggetti a queste funzioni. In altre parole, il chiamante deve richiamare solo pagine delle proprietà comuni a tutti gli oggetti.

Inoltre, il chiamante passa [**i puntatori IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) anche agli oggetti interessati alle funzioni API. Entrambe le funzioni API creano una finestra di dialogo con frame di proprietà e creano un'istanza di un sito di pagina [**con IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) per ogni pagina che verrà caricata. Tramite questa interfaccia una pagina delle proprietà può:

-   Recuperare la lingua corrente usata nella finestra delle proprietà tramite [**GetLocaleID**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getlocaleid).
-   Chiedere al fotogramma di elaborare le sequenze di tasti [**tramite TranslateAccelerator.**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-translateaccelerator)
-   Notificare al frame le modifiche nella pagina tramite [**OnStatusChange.**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-onstatuschange)
-   Ottenere un puntatore a interfaccia per il frame stesso tramite [**GetPageContainer,**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypagesite-getpagecontainer)anche se non sono presenti interfacce definite per il frame in questo momento per questa funzione restituisce sempre E \_ NOTIMPL.

Il frame di proprietà crea un'istanza di ogni oggetto pagina delle proprietà e ottiene [**l'interfaccia IPropertyPage di**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) ogni pagina. Tramite questa interfaccia il frame informa la pagina del sito della pagina ([**SetPageSite**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setpagesite)), recupera le dimensioni e le stringhe della pagina ([**GetPageInfo**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-getpageinfo)), passa i puntatori di interfaccia agli oggetti interessati ([**SetObjects**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-setobjects)), indica alla pagina quando creare ed eliminare i relativi controlli ([**Activate**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-activate) e [**Deactivate**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-deactivate)), indica alla pagina di show o reposition ([**Show**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-show) and [**Move**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-move)), indica alla pagina di applicare i valori correnti agli oggetti interessati ([**Apply**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-apply)), controlla lo stato dirty della pagina ([**IsPageDirty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-ispagedirty)), richiama la Guida ([**Help**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-help)) e passa le sequenze di tasti alla pagina ([**TranslateAccelerator).**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage-translateaccelerator)

Un oggetto può anche supportare l'esplorazione per proprietà, che fornisce:

1.  Un modo (tramite [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) e [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)) per specificare la proprietà in cui deve essere assegnato lo stato attivo iniziale alla prima visualizzazione di una finestra delle proprietà
2.  Un modo (tramite [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)) per l'oggetto per specificare i valori predefiniti e le stringhe descrittive corrispondenti che possono essere visualizzate nell'interfaccia utente di un client per le proprietà.

Un oggetto può scegliere di supportare (2) senza supportare (1), ad esempio quando l'oggetto non ha una finestra delle proprietà.

Le [**interfacce IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2) [**e IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) sono definite come segue:

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

Per specificare il supporto per tali funzionalità, l'oggetto implementa [**IPerPropertyBrowsing.**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing) Tramite questa interfaccia, il chiamante può richiedere le informazioni necessarie per ottenere l'esplorazione, ad esempio stringhe predefinite ([**GetPredefinedStrings**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings)) e valori ([**GetPredefinedValue**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue)) nonché una stringa di visualizzazione per una determinata proprietà ([**GetDisplayString**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-getdisplaystring)).

Inoltre, il client può ottenere il CLSID della pagina delle proprietà che consente all'utente di modificare una determinata proprietà identificata con un DISPID ([**MapPropertyToPage**](/windows/desktop/api/OCIdl/nf-ocidl-iperpropertybrowsing-mappropertytopage)). Il client indica quindi al frame della proprietà di attivare inizialmente la pagina passando il CLSID e il DISPID a [**OleCreatePropertyFrameIndirect.**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect) Il frame attiva prima la pagina e passa il DISPID alla pagina tramite [**IPropertyPage2::EditProperty**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertypage2-editproperty). La pagina imposta quindi lo stato attivo sul campo di modifica della proprietà. In questo modo, un client può passare dal nome di una proprietà nella propria interfaccia utente alla pagina delle proprietà in grado di modificare tale proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pagine delle proprietà e finestre delle proprietà](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




