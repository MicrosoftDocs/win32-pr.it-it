---
title: Migrazione al framework della barra multifunzione di Windows
description: È possibile eseguire la migrazione di un'applicazione che si basa su menu tradizionali, barre degli strumenti e finestre di dialogo nell'interfaccia utente avanzata, dinamica e basata sul contesto del sistema di comandi della barra multifunzione di Windows.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Barra multifunzione di Windows, migrazione a
- Barra multifunzione, migrazione a
- migrazione alla barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74822781f891815c6eb30d9e15a7f7efaa983fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473595"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a>Migrazione al framework della barra multifunzione di Windows

È possibile eseguire la migrazione di un'applicazione che si basa su menu tradizionali, barre degli strumenti e finestre di dialogo nell'interfaccia utente avanzata, dinamica e basata sul contesto del sistema di comandi della barra multifunzione di Windows. Si tratta di un modo semplice ed efficace per modernizzare e rivitalizzare l'applicazione, migliorando al tempo stesso l'accessibilità, l'usabilità e l'individuabilità delle relative funzionalità.

## <a name="introduction"></a>Introduzione

In generale, la migrazione di un'applicazione esistente al framework della barra multifunzione prevede quanto segue:

-   Progettazione di un'organizzazione di controllo e layout della barra multifunzione che espone la funzionalità dell'applicazione esistente ed è sufficientemente flessibile per supportare nuove funzionalità.
-   Adattamento del codice dell'applicazione esistente.
-   Migrazione delle risorse dell'applicazione esistenti (stringhe e immagini) al framework della barra multifunzione.

> [!Note]  
> Le [linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx) devono essere esaminate per determinare se l'applicazione è un candidato adatto per un'interfaccia utente della barra multifunzione.

 

## <a name="design-the-ribbon-layout"></a>Progettare il layout della barra multifunzione

È possibile identificare le possibili progettazioni dell'interfaccia utente della barra multifunzione e i layout dei controlli eseguendo questi passaggi:

1.  Esecuzione dell'inventario di tutte le funzionalità esistenti.
2.  Conversione di questa funzionalità in comandi della barra multifunzione.
3.  Organizzare i comandi in gruppi logici.

### <a name="take-inventory"></a>Eseguire l'inventario

Nel framework della barra multifunzione, la funzionalità esposta da un'applicazione che modifica lo stato o la visualizzazione di un'area di lavoro o di un documento è considerata un comando. Ciò che costituisce un comando può variare e dipende dalla natura e dal dominio dell'applicazione esistente.

La tabella seguente elenca un set di comandi di base per un'applicazione di modifica del testo ipotetica:



| Simbolo           | ID     | Descrizione               |
|------------------|--------|---------------------------|
| \_nuovo file \_ ID    | 0xE100 | Nuovo documento              |
| \_Salva file \_ ID   | 0xE103 | Salva documento             |
| \_SaveAs file \_ ID | 0xE104 | Salva con nome... dialogo       |
| ID \_ file \_ aperto   | 0xE101 | Apri... dialogo          |
| \_uscita file \_ ID   | 0xE102 | Uscire dall'applicazione      |
| \_Annulla modifica \_ ID   | 0xE12B | Annulla                      |
| \_taglia ID modifica \_    | 0xE123 | Taglia il testo selezionato         |
| \_Copia ID modifica \_   | 0xE122 | Copia testo selezionato        |
| \_modifica ID \_ Incolla  | 0xE125 | Incolla testo dagli Appunti |
| \_modifica ID \_ Cancella  | 0xE120 | Elimina testo selezionato      |
| \_Zoom visualizzazione \_ ID   | 1242   | Ingrandisci... dialogo          |



 

Per la compilazione di un inventario dei comandi, vedere oltre i menu e le barre degli strumenti esistenti. Prendere in considerazione tutti i modi in cui un utente può interagire con l'area di lavoro. Anche se non tutti i comandi sono idonei per l'inclusione nella barra multifunzione, questo esercizio può esporre in modo molto efficace i comandi precedentemente nascosti dai livelli dell'interfaccia utente.

### <a name="translate"></a>Traduci

Non tutti i comandi devono essere rappresentati nell'interfaccia utente della barra multifunzione. Ad esempio, l'immissione di testo, la modifica di una selezione, lo scorrimento o lo spostamento del punto di inserimento con il mouse vengono tutti qualificati come comandi nell'editor di testo ipotetico, tuttavia, questi non sono idonei per esporre in una barra dei comandi perché ognuno implica un'interazione diretta con l'interfaccia utente dell'applicazione.

Viceversa, alcune funzionalità potrebbero non essere considerate come un comando nel senso tradizionale. Ad esempio, anziché essere seppelliti in una finestra di dialogo, le regolazioni dei margini della pagina della stampante possono essere rappresentate nella barra multifunzione come un gruppo di controlli casella di selezione in una scheda contestuale o in una [modalità di applicazione](ribbon-applicationmodes.md).

> [!Note]  
> Prendere nota dell'ID numerico che può essere assegnato a ogni comando. Alcuni framework dell'interfaccia utente, ad esempio Microsoft Foundation Classes (MFC), definiscono gli ID per i comandi come il menu file e modifica (da 0xE100 a 0xE200).

 

### <a name="organize"></a>Organizzazione

Prima di provare a organizzare l'inventario dei comandi, è necessario esaminare le [linee guida sull'esperienza utente della barra multifunzione](https://msdn.microsoft.com/library/cc872782.aspx) per le procedure consigliate per l'implementazione di un'interfaccia utente della barra

In generale, le regole seguenti possono essere applicate all'organizzazione dei comandi della barra multifunzione:

-   I comandi che operano sul file o sull'applicazione complessiva più probabilmente appartengono al [menu dell'applicazione](windowsribbon-controls-applicationmenu.md).
-   I comandi usati di frequente, ad esempio taglia, copia e incolla, come nell'esempio di editor di testo, vengono in genere inseriti in una scheda Home predefinita. Nelle applicazioni più complesse possono essere duplicate altrove nell'interfaccia utente della barra multifunzione.
-   I comandi importanti o di uso frequente possono garantire l'inclusione predefinita nella [barra di accesso rapido](windowsribbon-controls-quickaccesstoolbar.md).

Il Framework Ribbon fornisce anche controlli ContextMenu e MiniToolbar tramite la vista ContextPopup. Queste funzionalità non sono obbligatorie, ma se l'applicazione dispone di uno o più menu di scelta rapida esistenti, la migrazione dei comandi che contengono potrebbe consentire il riutilizzo della codebase esistente con binding automatico alle risorse esistenti.

Poiché ogni applicazione è diversa, leggere le linee guida e provare ad applicarle alla massima misura possibile. Uno degli obiettivi del Framework della barra multifunzione è fornire un'esperienza utente familiare e coerente e questo obiettivo sarà più realizzabile se le soluzioni per le nuove applicazioni rispecchiano il più possibile le applicazioni Ribbon esistenti.

## <a name="adapt-your-code"></a>Adattare il codice

Una volta identificati e organizzati i comandi della barra multifunzione in raggruppamenti logici, il numero di passaggi necessari per incorporare il Framework della barra multifunzione nel codice dell'applicazione esistente dipende dalla complessità dell'applicazione originale. In generale, sono disponibili tre passaggi di base:

-   Creare il markup della barra multifunzione in base all'organizzazione dei comandi e alla specifica del layout.
-   Sostituisci funzionalità di menu e barre degli strumenti legacy con funzionalità della barra multifunzione.
-   Implementare una scheda IUICommandHandler.

### <a name="create-the-markup"></a>Creare il markup

L'elenco di comandi, nonché l'organizzazione e il layout vengono dichiarati tramite il file di markup della barra multifunzione utilizzato dal [compilatore di markup della barra multifunzione](windowsribbon-intentcl.md).

> [!Note]  
> Molti dei passaggi necessari per adattare un'applicazione esistente sono simili a quelli necessari per avviare una nuova applicazione Ribbon. Per ulteriori informazioni, vedere l'esercitazione relativa alla [creazione di un'applicazione barra multifunzione](windowsribbon-stepbystep.md) per una nuova applicazione della barra multifunzione.

 

Il markup della barra multifunzione è suddiviso in due sezioni principali. La prima sezione è un manifesto di comandi e delle risorse associate (stringhe e immagini). La seconda sezione specifica la struttura e il posizionamento dei controlli sulla barra multifunzione.

Il markup per l'editor di testo semplice potrebbe avere un aspetto simile all'esempio seguente:

> [!Note]  
> Le risorse di immagine e stringa sono descritte più avanti in questo articolo.

 


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



Per evitare di ridefinire i simboli definiti da un Framework dell'interfaccia utente, ad esempio MFC, nell'esempio precedente vengono usati nomi di simboli leggermente diversi per ogni comando (ID \_ file \_ nuovo rispetto all'ID \_ cmd \_ nuovo). Tuttavia, l'ID numerico assegnato a ogni comando deve rimanere invariato.

Per integrare il file di markup in un'applicazione, configurare un'istruzione di compilazione personalizzata per eseguire il compilatore di markup della barra multifunzione UICC.exe. I file di intestazione e di risorse risultanti vengono quindi incorporati nel progetto esistente. Se l'applicazione della barra multifunzione Editor di testo di esempio è denominata "RibbonPad", è necessaria una riga di comando di compilazione personalizzata simile alla seguente:


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



Il compilatore di markup crea un file binario, un file di intestazione (H) e un file di risorse (RC). Poiché è probabile che l'applicazione esistente disponga di un file RC esistente, includere i file H e RC generati nel file RC, come illustrato nell'esempio seguente:


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



### <a name="replace-legacy-menus-and-toolbars"></a>Sostituire i menu e le barre degli strumenti legacy

Per sostituire i menu e le barre degli strumenti standard con una barra multifunzione in un'applicazione legacy è necessario quanto segue:

1.  Rimuovere la barra degli strumenti e i riferimenti alle risorse di menu dal file di risorse dell'applicazione.
2.  Elimina tutti i codici di inizializzazione della barra degli strumenti e dei menu.
3.  Eliminare qualsiasi codice utilizzato per aggiungere una barra degli strumenti o una barra dei menu alla finestra di primo livello dell'applicazione.
4.  Creare un'istanza del Framework della barra multifunzione.
5.  Alleghi la barra multifunzione alla finestra di primo livello dell'applicazione.
6.  Caricare il markup compilato.

> [!IMPORTANT]
> La barra di stato esistente e le tabelle dei tasti di scelta rapida devono essere mantenute perché il Framework della barra multifunzione non sostituisce queste funzionalità.

 

Nell'esempio seguente viene illustrato come inizializzare il Framework utilizzando [**IUIFramework:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):


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



Nell'esempio seguente viene illustrato come utilizzare [**IUIFramework:: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) per caricare il markup compilato:


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



La classe CApplication, a cui si fa riferimento, deve implementare una coppia di interfacce di Component Object Model (COM) definite dal framework della barra multifunzione: [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) e [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).

[**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) fornisce l'interfaccia di callback principale tra il Framework e l'applicazione (ad esempio, l'altezza della barra multifunzione viene comunicata tramite [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)), mentre i callback per i singoli comandi vengono forniti in risposta a [**IUIApplication:: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).

**Suggerimento:** Alcuni framework applicazione, ad esempio MFC, richiedono che l'altezza della barra multifunzione venga presa in considerazione durante il rendering dello spazio del documento dell'applicazione. In questi casi, l'aggiunta di una finestra nascosta per sovrapporre la barra multifunzione e forzare lo spazio del documento sull'altezza desiderata è necessaria. Per un esempio di questo approccio, in cui viene chiamata una funzione di layout basata sull'altezza della barra multifunzione restituita dal metodo [**IUIRibbon:: GetHeight**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) , vedere l' [esempio HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).

L'esempio di codice seguente illustra un'implementazione di [**IUIApplication:: OnViewChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) :


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



### <a name="implement-an-iuicommandhandler-adapter"></a>Implementare un adattatore IUICommandHandler

A seconda della progettazione dell'applicazione originale, può risultare più semplice avere più implementazioni del gestore comandi o un singolo gestore dei comandi di bridging che richiama la logica del comando dell'applicazione esistente. Molte applicazioni usano \_ i messaggi di comando WM a questo scopo, dove è sufficiente fornire un singolo gestore di comandi per tutti gli scopi che inoltri semplicemente \_ i messaggi di comando WM alla finestra di primo livello.

Tuttavia, questo approccio richiede una gestione speciale per i comandi, ad esempio **Exit** o **Close**. Poiché la barra multifunzione non può essere distrutta durante l'elaborazione di un messaggio di finestra, il \_ messaggio WM Close deve essere inviato al thread dell'interfaccia utente dell'applicazione e non deve essere elaborato in modo sincrono, come illustrato nell'esempio seguente:


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



## <a name="migrating-resources"></a>Migrazione di risorse

Quando è stato definito il manifesto dei comandi, la struttura della barra multifunzione è stata dichiarata e il codice dell'applicazione è stato adattato per ospitare il Framework della barra multifunzione, il passaggio finale è la specifica delle risorse stringa e immagine per ogni comando.

> [!Note]  
> Le risorse stringa e immagine vengono in genere fornite nel file di markup. Tuttavia, possono essere generati o sostituiti a livello di codice implementando il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

 

### <a name="string-resources"></a>Risorse di stringa

[**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) è la proprietà di stringa più comune definita per un comando. Il rendering viene eseguito come etichette di testo per schede, gruppi e singoli controlli. Una stringa di etichetta da una voce di menu legacy può in genere essere riutilizzata per un **comando. LabelTitle** senza alcuna modifica.

Tuttavia, le convenzioni seguenti sono state modificate con l'avvento della barra multifunzione:

-   Il suffisso con i puntini di sospensione (...), utilizzato per indicare un comando di avvio della finestra di dialogo, non è più necessario.
-   La e commerciale (&) può ancora essere usata per indicare un tasto di scelta rapida per un comando che viene visualizzato in un menu, ma la proprietà [**Command. suggerimentod**](windowsribbon-element-command-keytip.md) supportata dal Framework soddisfa uno scopo simile.

Facendo riferimento all'esempio di editor di testo, è possibile specificare le seguenti stringhe per LabelTitle e suggerimento tasto di risposta:



| Simbolo           | Stringa originale | Stringa LabelTitle | Stringa suggerimento |
|------------------|-----------------|-------------------|---------------|
| \_nuovo file \_ ID    | &nuovo            | &nuovo              | N             |
| \_Salva file \_ ID   | &Salva           | &Salva             | S             |
| \_SaveAs file \_ ID | Salva &con nome...       | Salva &          | A             |
| ID \_ file \_ aperto   | &Apri...          | &amp;Open             | O             |
| \_uscita file \_ ID   | &Esci           | &Esci             | X             |
| \_Annulla modifica \_ ID   | Annulla &           | Annulla              | Z             |
| \_taglia ID modifica \_    | Cu&t            | Cu&t              | X             |
| \_Copia ID modifica \_   | Copia &           | Copia &             | C             |
| \_modifica ID \_ Incolla  | Incolla &          | Incolla &            | V             |
| \_modifica ID \_ Cancella  | Eliminazione &         | Eliminazione &           | D             |
| \_Zoom visualizzazione \_ ID   | Zoom &...          | Zoom              | Z             |



 

Di seguito è riportato un elenco di altre proprietà di stringa che devono essere impostate nella maggior parte dei comandi:

-   [**Comando. LabelDescription**](windowsribbon-element-command-labeldescription.md)
-   [**Comando. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
-   [**Comando. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)

Le schede, i gruppi e altre funzionalità dell'interfaccia utente della barra multifunzione possono ora essere dichiarate con tutte le risorse stringa e immagine specificate.

Nell'esempio di markup della barra multifunzione seguente sono illustrate varie risorse di stringa:


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

Il Framework della barra multifunzione supporta formati di immagini che forniscono un aspetto molto più completo rispetto ai formati di immagine supportati dai componenti dei menu e delle barre degli strumenti precedenti.

Per Windows 8 e versioni successive, il Framework della barra multifunzione supporta i formati grafici seguenti: file di bitmap (BMP) a 32 bit ARGB (BMP) e file Portable Network Graphics (PNG) con trasparenza.

Per Windows 7 e versioni precedenti, le risorse di immagine devono essere conformi al formato di grafica BMP standard usato in Windows.

> [!Note]  
> I file di immagine esistenti possono essere convertiti in uno dei due formati. Tuttavia, i risultati potrebbero essere meno soddisfacenti se i file di immagine non supportano l'anti-aliasing e la trasparenza.

 

Non è possibile specificare una singola dimensione predefinita per le risorse immagine nel framework della barra multifunzione. Tuttavia, per supportare il [layout adattivo](windowsribbon-templates.md) dei controlli, le immagini possono essere specificate in due dimensioni (grandi e piccole). Tutte le immagini nel framework della barra multifunzione vengono ridimensionate in base alla risoluzione dpi (punti per pollice) dello schermo con le dimensioni esatte che dipendono da questa impostazione dpi. Per ulteriori informazioni, vedere [specifica delle risorse dell'immagine della barra multifunzione](windowsribbon-imageformats.md) .

Nell'esempio seguente viene illustrato come viene fatto riferimento a un set di immagini specifiche di dpi nel markup:


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

[Specifica delle risorse dell'immagine della barra multifunzione](windowsribbon-imageformats.md)
</dt> </dl>

 

 