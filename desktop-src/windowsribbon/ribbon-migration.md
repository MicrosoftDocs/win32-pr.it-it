---
title: Migrazione al framework Windows ribbon
description: È possibile eseguire la migrazione di un'applicazione basata su menu, barre degli strumenti e finestre di dialogo tradizionali all'interfaccia utente ricca, dinamica e basata sul contesto del sistema di comandi del framework della barra multifunzione Windows.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Windows Barra multifunzione, migrazione a
- Barra multifunzione, migrazione a
- migrazione alla barra multifunzione Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a011e9b5dad52f6f71fab272f0fded39ec59eb71cc7311ab9cf5ffccb4dfbca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841121"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a>Migrazione al framework Windows ribbon

È possibile eseguire la migrazione di un'applicazione basata su menu, barre degli strumenti e finestre di dialogo tradizionali all'interfaccia utente ricca, dinamica e basata sul contesto del sistema di comandi del framework della barra multifunzione Windows. Si tratta di un modo semplice ed efficace per modernizzare e rivitalizzare l'applicazione, migliorando al tempo stesso l'accessibilità, l'usabilità e l'individuabilità delle funzionalità.

## <a name="introduction"></a>Introduzione

In generale, la migrazione di un'applicazione esistente al framework della barra multifunzione comporta quanto segue:

-   Progettazione di un'organizzazione di layout e controllo della barra multifunzione che espone le funzionalità dell'applicazione esistente ed è sufficientemente flessibile da supportare nuove funzionalità.
-   Adattamento del codice dell'applicazione esistente.
-   Migrazione delle risorse dell'applicazione esistenti (stringhe e immagini) al framework della barra multifunzione.

> [!Note]  
> Le [linee guida per l'esperienza utente](https://msdn.microsoft.com/library/cc872782.aspx) della barra multifunzione devono essere esaminate per determinare se l'applicazione è un candidato adatto per un'interfaccia utente della barra multifunzione.

 

## <a name="design-the-ribbon-layout"></a>Progettare il layout della barra multifunzione

Le potenziali progettazioni dell'interfaccia utente della barra multifunzione e i layout dei controlli possono essere identificati eseguendo questa procedura:

1.  Inventario di tutte le funzionalità esistenti.
2.  Traduzione di questa funzionalità in comandi della barra multifunzione.
3.  Organizzazione dei comandi in gruppi logici.

### <a name="take-inventory"></a>Eseguire l'inventario

Nel framework della barra multifunzione la funzionalità esposta da un'applicazione che modifica lo stato o la visualizzazione di un'area di lavoro o di un documento è considerata un comando. Ciò che costituisce un comando può variare e dipende dalla natura e dal dominio dell'applicazione esistente.

La tabella seguente elenca un set di comandi di base per un'ipotetica applicazione di modifica del testo:



| Simbolo           | ID     | Descrizione               |
|------------------|--------|---------------------------|
| FILE \_ ID \_ NUOVO    | 0xE100 | Nuovo documento              |
| SALVATAGGIO \_ FILE \_ ID   | 0xE103 | Salvare il documento             |
| ID \_ FILE \_ SAVEAS | 0xE104 | Salva con nome... (finestra di dialogo)       |
| FILE \_ ID \_ APERTO   | 0xE101 | Aperto... (finestra di dialogo)          |
| USCITA \_ DEL FILE \_ ID   | 0xE102 | Uscire dall'applicazione      |
| MODIFICA ID \_ \_ ANNULLA   | 0xE12B | Annulla                      |
| ID \_ EDIT \_ CUT    | 0xE123 | Tagliare il testo selezionato         |
| MODIFICA \_ COPIA \_ ID   | 0xE122 | Copiare il testo selezionato        |
| MODIFICA ID \_ \_ INCOLLA  | 0xE125 | Incollare testo dagli Appunti |
| ID \_ EDIT \_ CLEAR  | 0xE120 | Eliminare il testo selezionato      |
| ZOOM \_ VISUALIZZAZIONE \_ ID   | 1242   | Zoom... (finestra di dialogo)          |



 

Esaminare oltre i menu e le barre degli strumenti esistenti quando si compila un inventario dei comandi. Considerare tutti i modi in cui un utente può interagire con l'area di lavoro. Anche se non tutti i comandi sono adatti per l'inclusione nella barra multifunzione, questo esercizio potrebbe esporre molto bene i comandi precedentemente nascosti dai livelli dell'interfaccia utente.

### <a name="translate"></a>Traduci

Non tutti i comandi devono essere rappresentati nell'interfaccia utente della barra multifunzione. Ad esempio, l'immissione di testo, la modifica di una selezione, lo scorrimento o lo spostamento del punto di inserimento con il mouse sono tutti idonei come comandi nell'ipotetico editor di testo, ma non sono adatti per essere esposti in una barra dei comandi, in quanto ognuno comporta un'interazione diretta con l'interfaccia utente dell'applicazione.

Al contrario, alcune funzionalità potrebbero non essere ritenute come un comando nel senso tradizionale. Ad esempio, invece di essere nascosto in una finestra di dialogo, le regolazioni del margine pagina della stampante possono essere rappresentate nella barra multifunzione come un gruppo di controlli Casella di selezione in una scheda contestuale o in modalità [applicazione.](ribbon-applicationmodes.md)

> [!Note]  
> Prendere nota dell'ID numerico che può essere assegnato a ogni comando. Alcuni framework dell'interfaccia utente, ad esempio Microsoft Foundation Classes (MFC), definiscono gli ID per i comandi, ad esempio il menu file e di modifica (0xE100 per 0xE200).

 

### <a name="organize"></a>Organizzazione

Prima di tentare di organizzare [](https://msdn.microsoft.com/library/cc872782.aspx) l'inventario dei comandi, è consigliabile esaminare le linee guida per l'esperienza utente della barra multifunzione per le procedure consigliate durante l'implementazione di un'interfaccia utente della barra multifunzione.

In generale, le regole seguenti possono essere applicate all'organizzazione Comando barra multifunzione:

-   I comandi che operano sul file o sull'applicazione complessiva appartengono molto probabilmente al [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).
-   I comandi usati di frequente, ad esempio Taglia, Copia e Incolla (come nell'esempio dell'editor di testo), vengono in genere inseriti in una scheda home predefinita. Nelle applicazioni più complesse, possono essere duplicate altrove nell'interfaccia utente della barra multifunzione.
-   I comandi importanti o usati di frequente possono richiedere l'inclusione predefinita nella barra [di accesso rapido.](windowsribbon-controls-quickaccesstoolbar.md)

Il framework della barra multifunzione fornisce anche i controlli ContextMenu e MiniToolbar tramite la visualizzazione ContextPopup. Queste funzionalità non sono obbligatorie, ma se l'applicazione ha uno o più menu di scelta rapida esistenti, la migrazione dei comandi che contengono può consentire il riutilizzo della codebase esistente con l'associazione automatica alle risorse esistenti.

Poiché ogni applicazione è diversa, leggere le linee guida e provare ad applicarle nel modo più completo possibile. Uno degli obiettivi del framework della barra multifunzione è offrire un'esperienza utente familiare e coerente e questo obiettivo sarà più raggiungibile se le progettazioni per le nuove applicazioni rispecchiano il più possibile le applicazioni della barra multifunzione esistenti.

## <a name="adapt-your-code"></a>Adattare il codice

Dopo aver identificato e organizzato i comandi della barra multifunzione in raggruppamenti logici, il numero di passaggi necessari per incorporare il framework della barra multifunzione nel codice dell'applicazione esistente dipende dalla complessità dell'applicazione originale. In generale, sono disponibili tre passaggi di base:

-   Creare il markup della barra multifunzione in base alla specifica dell'organizzazione e del layout dei comandi.
-   Sostituire la funzionalità di menu e barra degli strumenti legacy con la funzionalità barra multifunzione.
-   Implementare un adattatore IUICommandHandler.

### <a name="create-the-markup"></a>Creare il markup

L'elenco di comandi, l'organizzazione e il layout vengono dichiarati tramite il file di markup della barra multifunzione utilizzato dal compilatore [di markup della barra multifunzione](windowsribbon-intentcl.md).

> [!Note]  
> Molti dei passaggi necessari per adattare un'applicazione esistente sono simili a quelli necessari per avviare una nuova applicazione barra multifunzione. Per altre informazioni, vedere l'esercitazione [Creazione di un'applicazione barra](windowsribbon-stepbystep.md) multifunzione per una nuova procedura dettagliata dell'applicazione barra multifunzione.

 

Il markup della barra multifunzione è in due sezioni principali. La prima sezione è un manifesto dei comandi e delle risorse associate (stringhe e immagini). La seconda sezione specifica la struttura e la posizione dei controlli sulla barra multifunzione.

Il markup per l'editor di testo semplice potrebbe essere simile all'esempio seguente:

> [!Note]  
> Le risorse immagine e stringa sono trattate più avanti in questo articolo.

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



Per evitare di ridefinire i simboli definiti da un framework dell'interfaccia utente come MFC, nell'esempio precedente vengono utilizzati nomi di simboli leggermente diversi per ogni comando (ID FILE NEW e \_ \_ ID CMD \_ \_ NEW). Tuttavia, l'ID numerico assegnato a ogni comando deve rimanere invariato.

Per integrare il file di markup in un'applicazione, configurare un'istruzione di compilazione personalizzata per eseguire il compilatore di markup della barra multifunzione, UICC.exe. L'intestazione risultante e i file di risorse vengono quindi incorporati nel progetto esistente. Se l'applicazione barra multifunzione dell'editor di testo di esempio è denominata "RibbonPad", è necessaria una riga di comando di compilazione personalizzata simile alla seguente:


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



Il compilatore di markup crea un file binario, un file di intestazione (H) e un file di risorse (RC). Poiché è probabile che l'applicazione esistente abbia un file RC esistente, includere i file H e RC generati in tale file RC, come illustrato nell'esempio seguente:


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a>Sostituire menu e barre degli strumenti legacy

La sostituzione di menu e barre degli strumenti standard con una barra multifunzione in un'applicazione legacy richiede quanto segue:

1.  Rimuovere i riferimenti alle risorse della barra degli strumenti e del menu dal file di risorse dell'applicazione.
2.  Eliminare tutto il codice di inizializzazione della barra degli strumenti e della barra dei menu.
3.  Eliminare il codice usato per collegare una barra degli strumenti o una barra dei menu alla finestra di primo livello dell'applicazione.
4.  Creare un'istanza del framework della barra multifunzione.
5.  Collegare la barra multifunzione alla finestra di primo livello dell'applicazione.
6.  Caricare il markup compilato.

> [!IMPORTANT]
> Le tabelle esistenti della barra di stato e dei tasti di scelta rapida devono essere mantenute perché il framework della barra multifunzione non sostituisce queste funzionalità.

 

L'esempio seguente illustra come inizializzare il framework [**usando IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



L'esempio seguente illustra come usare [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) per caricare il markup compilato:


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



La classe CApplication, a cui si fa riferimento in precedenza, deve implementare una coppia di interfacce Component Object Model (COM) definite dal framework della barra multifunzione: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) e [**IUICommandHandler.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)

[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) fornisce l'interfaccia di callback principale tra il framework e l'applicazione (ad esempio, l'altezza della barra multifunzione viene comunicata tramite [**IUIApplication::OnViewChanged)**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)mentre i callback per i singoli comandi vengono forniti in risposta a [**IUIApplication::OnCreateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)

**Suggerimento:** Alcuni framework applicazioni, ad esempio MFC, richiedono che l'altezza della barra multifunzione sia presa in considerazione quando si esegue il rendering dello spazio documento dell'applicazione. In questi casi, è necessaria l'aggiunta di una finestra nascosta per sovrapporre la barra multifunzione e forzare lo spazio del documento all'altezza desiderata. Per un esempio di questo approccio, in cui viene chiamata una funzione di layout in base all'altezza della barra multifunzione restituita dal metodo [**IUIRibbon::GetHeight,**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) vedere l'esempio [HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).

L'esempio di codice seguente illustra [**un'implementazione di IUIApplication::OnViewChanged:**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a>Implementare un adapter IUICommandHandler

A seconda della progettazione dell'applicazione originale, può essere più semplice avere più implementazioni del gestore command o un singolo gestore command di bridging che richiama la logica di comando dell'applicazione esistente. Molte applicazioni usano messaggi WM COMMAND a questo scopo, in cui è sufficiente fornire un unico gestore comandi per tutti gli scopi che inoltra semplicemente i messaggi WM COMMAND alla finestra \_ \_ di primo livello.

Tuttavia, questo approccio richiede una gestione speciale per comandi come **Exit o** **Close.** Poiché la barra multifunzione non può essere distrutta durante l'elaborazione di un messaggio di finestra, il messaggio WM CLOSE deve essere inviato al thread dell'interfaccia utente dell'applicazione e non deve essere elaborato in modo sincrono, come illustrato \_ nell'esempio seguente:


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a>Migrazione delle risorse

Dopo aver definito il manifesto dei comandi, la struttura della barra multifunzione è stata dichiarata e il codice dell'applicazione è stato adattato per ospitare il framework della barra multifunzione, il passaggio finale è la specifica delle risorse stringa e immagine per ogni comando.

> [!Note]  
> Le risorse di tipo stringa e immagine vengono in genere fornite nel file di markup. Tuttavia, possono essere generati o sostituiti a livello di codice implementando il metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

 

### <a name="string-resources"></a>Risorse di tipo stringa

[**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) è la proprietà stringa più comune definita per un oggetto Command. Il rendering viene eseguito come etichette di testo per schede, gruppi e singoli controlli. Una stringa di etichetta da una voce di menu legacy può in genere essere usata di nuovo per **Command.LabelTitle** senza modifiche.

Tuttavia, le convenzioni seguenti sono cambiate con l'avvento della barra multifunzione:

-   Il suffisso con i puntini di sospensione (...) usato per indicare un comando di avvio della finestra di dialogo non è più necessario.
-   La e commerciale (&) può ancora essere usata per indicare un tasto di scelta rapida per un comando visualizzato in un menu, ma la proprietà [**Command.Keytip**](windowsribbon-element-command-keytip.md) supportata dal framework soddisfa uno scopo simile.

Facendo riferimento all'esempio dell'editor di testo, è possibile che siano specificate le stringhe seguenti per LabelTitle e Keytip:



| Simbolo           | Stringa originale | Stringa LabelTitle | Stringa del suggerimento tasto di scelta |
|------------------|-----------------|-------------------|---------------|
| ID \_ FILE \_ NEW    | &Nuovo            | &Nuovo              | N             |
| SALVATAGGIO \_ FILE \_ ID   | &Salva           | &Salva             | S             |
| ID \_ FILE \_ SAVEAS | Salva &con nome...       | Salva &con nome          | A             |
| FILE \_ ID \_ APERTO   | &Apri...          | &amp;Open             | O             |
| USCITA \_ FILE \_ ID   | &Esci           | &Esci             | X             |
| ANNULLAMENTO \_ MODIFICA \_ ID   | &annulla           | Annulla              | Z             |
| ID \_ EDIT \_ CUT    | Cu&t            | Cu&t              | X             |
| MODIFICA \_ \_ COPIA ID   | &copia           | &copia             | C             |
| ID \_ MODIFICA \_ INCOLLA  | &Incolla          | &Incolla            | V             |
| ID \_ EDIT \_ CLEAR  | &elimina         | &elimina           | D             |
| ZOOM \_ VISUALIZZAZIONE \_ ID   | &Zoom...          | Zoom              | Z             |



 

Di seguito è riportato un elenco di altre proprietà stringa che devono essere impostate nella maggior parte dei comandi:

-   [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md)
-   [**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
-   [**Command.TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)

Schede, gruppi e altre funzionalità dell'interfaccia utente della barra multifunzione possono ora essere dichiarati con tutte le risorse stringa e immagine specificate.

L'esempio di markup della barra multifunzione seguente illustra varie risorse stringa:


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a>Risorse immagine

Il framework della barra multifunzione supporta formati di immagine che offrono un aspetto molto più ricco rispetto ai formati di immagine supportati dai componenti di menu e barra degli strumenti precedenti.

Per Windows 8 e versioni successive, il framework della barra multifunzione supporta i formati grafici seguenti: file bitmap ARGB (BMP) a 32 bit e file Portable Network Graphics (PNG) con trasparenza.

Per Windows 7 e versioni precedenti, le risorse immagine devono essere conformi al formato grafico BMP standard usato in Windows.

> [!Note]  
> I file di immagine esistenti possono essere convertiti in entrambi i formati. Tuttavia, i risultati possono essere meno soddisfacenti se i file di immagine non supportano l'anti-aliasing e la trasparenza.

 

Non è possibile specificare una singola dimensione predefinita per le risorse immagine nel framework della barra multifunzione. Tuttavia, per supportare [il layout adattivo](windowsribbon-templates.md) dei controlli, le immagini possono essere specificate in due dimensioni (grande e piccola). Tutte le immagini nel framework della barra multifunzione vengono ridimensionate in base alla risoluzione dei punti per pollice (dpi) dello schermo con le dimensioni di rendering esatte in base a questa impostazione dpi. Per [altre informazioni, vedere Specifica delle risorse immagine](windowsribbon-imageformats.md) della barra multifunzione.

L'esempio seguente illustra come viene fatto riferimento a un set di immagini specifiche di dpi nel markup:


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica delle risorse immagine della barra multifunzione](windowsribbon-imageformats.md)
</dt> </dl>

 

 