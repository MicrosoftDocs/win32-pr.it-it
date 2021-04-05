---
title: Barra di accesso rapido
description: La barra di accesso rapido (QAT) è una piccola barra degli strumenti personalizzabile che espone un set di comandi specificati dall'applicazione o selezionati dall'utente.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a50d562477e5c626d2d2bffa8ee5e0ecc84919
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046761"
---
# <a name="quick-access-toolbar"></a><span data-ttu-id="41e4d-103">Barra di accesso rapido</span><span class="sxs-lookup"><span data-stu-id="41e4d-103">Quick Access Toolbar</span></span>

<span data-ttu-id="41e4d-104">La barra di accesso rapido (QAT) è una piccola barra degli strumenti personalizzabile che espone un set di comandi specificati dall'applicazione o selezionati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="41e4d-104">The Quick Access Toolbar (QAT) is a small, customizable toolbar that exposes a set of Commands that are specified by the application or selected by the user.</span></span>

- [<span data-ttu-id="41e4d-105">Introduzione</span><span class="sxs-lookup"><span data-stu-id="41e4d-105">Introduction</span></span>](#introduction)
- [<span data-ttu-id="41e4d-106">Implementare la barra di accesso rapido</span><span class="sxs-lookup"><span data-stu-id="41e4d-106">Implement the Quick Access Toolbar</span></span>](#implement-the-quick-access-toolbar)
  - [<span data-ttu-id="41e4d-107">markup</span><span class="sxs-lookup"><span data-stu-id="41e4d-107">Markup</span></span>](#markup)
  - [<span data-ttu-id="41e4d-108">Codice</span><span class="sxs-lookup"><span data-stu-id="41e4d-108">Code</span></span>](#code)
- [<span data-ttu-id="41e4d-109">Persistenza QAT</span><span class="sxs-lookup"><span data-stu-id="41e4d-109">QAT Persistence</span></span>](#qat-persistence)
- [<span data-ttu-id="41e4d-110">Proprietà della barra di accesso rapido</span><span class="sxs-lookup"><span data-stu-id="41e4d-110">Quick Access Toolbar Properties</span></span>](#quick-access-toolbar-properties)
- [<span data-ttu-id="41e4d-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41e4d-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="41e4d-112">Introduzione</span><span class="sxs-lookup"><span data-stu-id="41e4d-112">Introduction</span></span>

<span data-ttu-id="41e4d-113">Per impostazione predefinita, la barra di accesso rapido (QAT) si trova nella barra del titolo della finestra dell'applicazione, ma può essere configurata per la visualizzazione sotto la barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="41e4d-113">By default, the Quick Access Toolbar (QAT) is located in the title bar of the application window but can be configured to display below the ribbon.</span></span> <span data-ttu-id="41e4d-114">Oltre a esporre i comandi, la barra di accesso rapido (QAT) include anche un menu a discesa personalizzabile che contiene il set completo di comandi QAT (default Quick Access Toolbar), sia nascosti che visualizzati nella barra di accesso rapido (QAT), e un set di barre di accesso rapido (QAT) e opzioni della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="41e4d-114">In addition to exposing Commands, the Quick Access Toolbar (QAT) also includes a customizable drop-down menu that contains the complete set of default Quick Access Toolbar (QAT) Commands (whether hidden or displayed in the Quick Access Toolbar (QAT)) and a set of Quick Access Toolbar (QAT) and ribbon options.</span></span>

<span data-ttu-id="41e4d-115">Lo screenshot seguente mostra un esempio della barra di accesso rapido della barra multifunzione (QAT).</span><span class="sxs-lookup"><span data-stu-id="41e4d-115">The following screen shot shows an example of the Ribbon Quick Access Toolbar (QAT).</span></span>

![Screenshot di QAT nella barra multifunzione di Microsoft Paint.](images/markup/qat-and-menu.png)

<span data-ttu-id="41e4d-117">La barra di accesso rapido (QAT) è costituita da una combinazione di un massimo di 20 comandi specificati dall'applicazione, noti come elenco di impostazioni predefinite dell'applicazione, o selezionati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="41e4d-117">The Quick Access Toolbar (QAT) consists of a combination of up to 20 Commands either specified by the application (known as the application defaults list) or selected by the user.</span></span> <span data-ttu-id="41e4d-118">La barra di accesso rapido (QAT) può contenere comandi univoci che non sono disponibili altrove nell'interfaccia utente della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="41e4d-118">The Quick Access Toolbar (QAT) can contain unique Commands that are not available elsewhere in the ribbon UI.</span></span>

> [!Note]
> <span data-ttu-id="41e4d-119">Sebbene quasi tutti i controlli della barra multifunzione consentano l'aggiunta del comando associato alla barra di accesso rapido (QAT) tramite il menu di scelta rapida illustrato nello screenshot seguente, i comandi esposti in una [finestra popup del contesto](windowsribbon-controls-contextpopup.md) non forniscono questo menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="41e4d-119">While almost all ribbon controls allow their associated Command to be added to the Quick Access Toolbar (QAT) through the context menu shown in the following screen shot, Commands exposed in a [Context Popup](windowsribbon-controls-contextpopup.md) do not provide this context menu.</span></span>
>
> ![screenshot del menu di scelta rapida del comando sulla barra multifunzione di Microsoft Paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a><span data-ttu-id="41e4d-121">Implementare la barra di accesso rapido</span><span class="sxs-lookup"><span data-stu-id="41e4d-121">Implement the Quick Access Toolbar</span></span>

<span data-ttu-id="41e4d-122">Come per tutti i controlli del Framework della barra multifunzione di Windows, per sfruttare appieno la barra di accesso rapido (QAT) è necessario un componente di markup che controlla la presentazione all'interno della barra multifunzione e un componente di codice che ne governa la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="41e4d-122">As with all Windows Ribbon framework controls, taking full advantage of the Quick Access Toolbar (QAT) requires both a markup component that controls its presentation within the ribbon and a code component that governs its functionality.</span></span>

### <a name="markup"></a><span data-ttu-id="41e4d-123">markup</span><span class="sxs-lookup"><span data-stu-id="41e4d-123">Markup</span></span>

<span data-ttu-id="41e4d-124">Il controllo barra di accesso rapido (QAT) viene dichiarato e associato a un ID di comando nel markup tramite l'elemento [QuickAccessToolBar](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="41e4d-124">The Quick Access Toolbar (QAT) control is declared, and associated with a Command ID, in markup through the [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span> <span data-ttu-id="41e4d-125">L'ID di comando viene usato per identificare e associare la barra di accesso rapido (QAT) a un gestore di comando definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="41e4d-125">The Command ID is used to identify and bind the Quick Access Toolbar (QAT) to a Command handler defined by the application.</span></span>

<span data-ttu-id="41e4d-126">Oltre al gestore dei comandi di base per la funzionalità della barra di accesso rapido principale (QAT), la dichiarazione dell'attributo facoltativo *CustomizeCommandName* [QuickAccessToolBar](windowsribbon-element-quickaccesstoolbar.md) Element fa in modo che il Framework aggiunga un **ulteriore elemento Commands** all'elenco dei comandi del menu a discesa della barra di accesso rapido (QAT) che richiede la definizione di un gestore di comando secondario.</span><span class="sxs-lookup"><span data-stu-id="41e4d-126">In addition to the basic Command handler for primary Quick Access Toolbar (QAT) functionality, declaring the optional *CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element attribute causes the framework to add a **More Commands** item to the Command list of the Quick Access Toolbar (QAT) drop-down menu that requires a secondary Command handler be defined.</span></span>

<span data-ttu-id="41e4d-127">Per coerenza tra le applicazioni della barra multifunzione, è consigliabile che il gestore di comandi *CustomizeCommandName* avvii una finestra di dialogo di personalizzazione della barra di accesso rapido (QAT).</span><span class="sxs-lookup"><span data-stu-id="41e4d-127">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a Quick Access Toolbar (QAT) customization dialog.</span></span> <span data-ttu-id="41e4d-128">Poiché il Framework della barra multifunzione fornisce solo il punto di avvio nell'interfaccia utente, l'applicazione è responsabile esclusivamente di fornire l'implementazione della finestra di dialogo di personalizzazione quando viene ricevuta la notifica di callback per questo comando.</span><span class="sxs-lookup"><span data-stu-id="41e4d-128">Because the Ribbon framework only provides the launching point in the UI, the application is solely responsible for providing the customization dialog implementation when the callback notification for this Command is received.</span></span>

<span data-ttu-id="41e4d-129">Lo screenshot seguente mostra un menu a discesa della barra di accesso rapido (QAT) con l'elemento di comando **altri comandi** .</span><span class="sxs-lookup"><span data-stu-id="41e4d-129">The following screen shot shows a Quick Access Toolbar (QAT) drop-down menu with the **More Commands** Command item.</span></span>

![Screenshot di un menu qat con altri comandi... elemento del comando.](images/markup/qat-customizecommandname.png)

<span data-ttu-id="41e4d-131">L'elenco delle impostazioni predefinite dell'applicazione per la barra di accesso rapido (QAT) viene specificato tramite la proprietà [QuickAccessToolBar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) , che identifica un elenco predefinito di comandi consigliati, tutti elencati nel menu a discesa della barra di accesso rapido (QAT).</span><span class="sxs-lookup"><span data-stu-id="41e4d-131">The application defaults list for the Quick Access Toolbar (QAT) is specified through the [QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) property which identifies a default list of recommended Commands, all of which are listed in the Quick Access Toolbar (QAT) drop-down menu.</span></span>

<span data-ttu-id="41e4d-132">Per visualizzare i comandi dall'elenco delle impostazioni predefinite dell'applicazione nella barra degli strumenti di accesso rapido (QAT), l'attributo *ApplicationDefaults. Dechecked* di ogni elemento del controllo deve avere un valore pari a `true` .</span><span class="sxs-lookup"><span data-stu-id="41e4d-132">To display Commands from the application defaults list in the Quick Access Toolbar (QAT) toolbar, the *ApplicationDefaults.IsChecked* attribute of each control element must have a value of `true`.</span></span> <span data-ttu-id="41e4d-133">Le immagini precedenti mostrano i risultati dell'impostazione di questo attributo su `true` per i comandi **Save**, **Undo** e **Redo** .</span><span class="sxs-lookup"><span data-stu-id="41e4d-133">The preceding images show the results of setting this attribute to `true` for the **Save**, **Undo**, and **Redo** Commands.</span></span>

<span data-ttu-id="41e4d-134">[QuickAccessToolBar. ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) supporta tre tipi di controlli della barra multifunzione: [Button](windowsribbon-controls-button.md), [interruttore](windowsribbon-controls-togglebutton.md)e [casella di controllo](windowsribbon-controls-checkbox.md).</span><span class="sxs-lookup"><span data-stu-id="41e4d-134">[QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) supports three types of Ribbon controls: [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), and [Check Box](windowsribbon-controls-checkbox.md).</span></span>

> [!Note]
> <span data-ttu-id="41e4d-135">Windows 8 e versioni successive: tutti i controlli basati su raccolta sono supportati ([ComboBox](windowsribbon-element-combobox.md), [inribbongallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md)e [DropDownGallery](windowsribbon-element-dropdowngallery.md)).</span><span class="sxs-lookup"><span data-stu-id="41e4d-135">Windows 8 and newer: All gallery-based controls are supported ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md), and [DropDownGallery](windowsribbon-element-dropdowngallery.md)).</span></span>
>
> <span data-ttu-id="41e4d-136">Gli elementi in un controllo raccolta possono supportare l'evidenziazione al passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="41e4d-136">Items in a gallery control can support highlighting on hover.</span></span> <span data-ttu-id="41e4d-137">Per supportare l'evidenziazione del passaggio del mouse, la raccolta deve essere una raccolta di elementi e usare un [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) di tipo [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).</span><span class="sxs-lookup"><span data-stu-id="41e4d-137">To support hover highlighting, the gallery must be an items gallery and use a [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) of type [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).</span></span>

<span data-ttu-id="41e4d-138">Nell'esempio seguente viene illustrato il markup di base per un elemento [QuickAccessToolBar](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="41e4d-138">The following example demonstrates the basic markup for a [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

<span data-ttu-id="41e4d-139">In questa sezione del codice vengono illustrate le dichiarazioni di comando per un elemento [barra di accesso rapido (QAT)](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="41e4d-139">This section of code shows the Command declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

<span data-ttu-id="41e4d-140">In questa sezione del codice vengono illustrate le dichiarazioni di controllo per un elemento [barra di accesso rapido (QAT)](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="41e4d-140">This section of code shows the control declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```

### <a name="code"></a><span data-ttu-id="41e4d-141">Codice</span><span class="sxs-lookup"><span data-stu-id="41e4d-141">Code</span></span>

<span data-ttu-id="41e4d-142">L'applicazione Ribbon Framework deve fornire un metodo di callback del gestore comandi per modificare la barra di accesso rapido (QAT).</span><span class="sxs-lookup"><span data-stu-id="41e4d-142">The Ribbon framework application must provide a Command handler callback method to manipulate the Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="41e4d-143">Questo gestore funziona in modo simile ai gestori della raccolta dei comandi, ad eccezione del fatto che la barra di accesso rapido (QAT) non supporta le categorie.</span><span class="sxs-lookup"><span data-stu-id="41e4d-143">This handler works in a similar fashion to Command gallery handlers, except that the Quick Access Toolbar (QAT) does not support categories.</span></span> <span data-ttu-id="41e4d-144">Per ulteriori informazioni, vedere [utilizzo delle raccolte](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="41e4d-144">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="41e4d-145">La raccolta di comandi della barra di accesso rapido (QAT) viene recuperata come oggetto [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) tramite la chiave della proprietà [ \_ \_ ItemsSource pkey dell'interfaccia utente](windowsribbon-reference-properties-uipkey-itemssource.md) .</span><span class="sxs-lookup"><span data-stu-id="41e4d-145">The Quick Access Toolbar (QAT) Command collection is retrieved as an [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span> <span data-ttu-id="41e4d-146">L'aggiunta di comandi alla barra di accesso rapido (QAT) in fase di esecuzione viene eseguita aggiungendo un oggetto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) a **IUICollection**.</span><span class="sxs-lookup"><span data-stu-id="41e4d-146">Adding Commands to the Quick Access Toolbar (QAT) at run time is accomplished by adding an [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object to the **IUICollection**.</span></span>

<span data-ttu-id="41e4d-147">Diversamente dalle raccolte di comandi, non è necessaria una proprietà del tipo di comando ([UI \_ pkey \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) per l'oggetto [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) della barra di accesso rapido (QAT).</span><span class="sxs-lookup"><span data-stu-id="41e4d-147">Unlike Command galleries, a command type property ([UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) is not required for the Quick Access Toolbar (QAT) [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object.</span></span> <span data-ttu-id="41e4d-148">Tuttavia, il comando deve esistere nella barra multifunzione o nell'elenco delle impostazioni di accesso rapido (QAT) dell'applicazione. non è possibile creare un nuovo comando in fase di esecuzione e aggiungerlo alla barra di accesso rapido (QAT).</span><span class="sxs-lookup"><span data-stu-id="41e4d-148">However, the Command must exist in the ribbon or Quick Access Toolbar (QAT) application defaults list; a new Command cannot be created at run time and added to the Quick Access Toolbar (QAT).</span></span>

> [!Note]  
> <span data-ttu-id="41e4d-149">L'applicazione Ribbon non può sostituire la barra di accesso rapido (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) con un oggetto raccolta personalizzato derivato da IEnumUnknown.</span><span class="sxs-lookup"><span data-stu-id="41e4d-149">The Ribbon application cannot replace the Quick Access Toolbar (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) with a custom collection object derived from IEnumUnknown.</span></span>

<span data-ttu-id="41e4d-150">Nell'esempio seguente viene illustrata un'implementazione del gestore comando QAT (Basic Quick Access Toolbar).</span><span class="sxs-lookup"><span data-stu-id="41e4d-150">The following example demonstrates a basic Quick Access Toolbar (QAT) Command handler implementation.</span></span>

```C++
/* QAT COMMAND HANDLER IMPLEMENTATION */
class CQATCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
  public:
    BEGIN_COM_MAP(CQATCommandHandler)
      COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    // QAT command handler's Execute method
    STDMETHODIMP Execute(UINT nCmdID,
                         UI_EXECUTIONVERB verb, 
                         const PROPERTYKEY* key,
                         const PROPVARIANT* ppropvarValue,
                         IUISimplePropertySet* pCommandExecutionProperties)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(verb);
      UNREFERENCED_PARAMETER(ppropvarValue);
      UNREFERENCED_PARAMETER(pCommandExecutionProperties);

      // Do not expect Execute callback for a QAT command
      return E_NOTIMPL;
    }

    // QAT command handler's UpdateProperty method
    STDMETHODIMP UpdateProperty(UINT nCmdID,
                                REFPROPERTYKEY key,
                                const PROPVARIANT* ppropvarCurrentValue,
                                PROPVARIANT* ppropvarNewValue)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(ppropvarNewValue);

      HRESULT hr = E_NOTIMPL;

      if (key == UI_PKEY_ItemsSource)
      {
        ATLASSERT(ppropvarCurrentValue->vt == VT_UNKNOWN);

        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        UINT nCount;
        if (SUCCEEDED(hr = spCollection->GetCount(&nCount)))
        {
          if (nCount == 0)
          {
            // If the current Qat list is empty, then we will add a few items here.
            UINT commands[] =  { cmdSave, cmdUndo};

            int count = _countof(commands);

            for (int i = 0; i < count; i++)
            {
              PROPERTYKEY keys[1] = {UI_PKEY_CommandId};
              CComObject<CItemProperties> *pItem = NULL;
              if (SUCCEEDED(CComObject<CItemProperties>::CreateInstance(&pItem)))
              {
                PROPVARIANT vars[1];

                InitPropVariantFromUInt32(commands[i], &vars[0]);

                pItem->Initialize(NULL, _countof(vars), keys, vars);

                CComPtr<IUnknown> spUnknown;
                pItem->QueryInterface(&spUnknown);
                spCollection->Add(spUnknown);
                            
                FreePropVariantArray(_countof(vars), vars);
              }
            }
          }
          else
          {
            // Do nothing if the Qat list is not empty.
            // Return S_FALSE to indicate the callback succeeded.
            return S_FALSE; 
          }
        }
      }
    return hr;
  }
};
```

## <a name="qat-persistence"></a><span data-ttu-id="41e4d-151">Persistenza QAT</span><span class="sxs-lookup"><span data-stu-id="41e4d-151">QAT Persistence</span></span>

<span data-ttu-id="41e4d-152">Le impostazioni e gli elementi del comando della barra di accesso rapido (QAT) possono essere salvati in modo permanente tra le sessioni dell'applicazione usando le funzioni [IUIRibbon:: SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) e [IUIRibbon:: LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="41e4d-152">Quick Access Toolbar (QAT) Command items and settings can be persisted across application sessions using the [IUIRibbon::SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) and [IUIRibbon::LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) functions.</span></span> <span data-ttu-id="41e4d-153">Per ulteriori informazioni, vedere la pagina relativa [allo stato della barra multifunzione permanente](ribbon-statepersistence.md).</span><span class="sxs-lookup"><span data-stu-id="41e4d-153">For more information, see [Persisting Ribbon State](ribbon-statepersistence.md).</span></span>

## <a name="quick-access-toolbar-properties"></a><span data-ttu-id="41e4d-154">Proprietà della barra di accesso rapido</span><span class="sxs-lookup"><span data-stu-id="41e4d-154">Quick Access Toolbar Properties</span></span>

<span data-ttu-id="41e4d-155">Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo barra di accesso rapido (QAT).</span><span class="sxs-lookup"><span data-stu-id="41e4d-155">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Quick Access Toolbar (QAT) control.</span></span>

<span data-ttu-id="41e4d-156">In genere, una proprietà della barra di accesso rapido (QAT) viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [IUIFramework:: InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="41e4d-156">Typically, a Quick Access Toolbar (QAT) property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [IUIFramework::InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="41e4d-157">L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [IUICommandHandler:: UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="41e4d-157">The invalidation event is handled, and the property updates defined, by the [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="41e4d-158">Il metodo di callback [IUICommandHandler:: UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework.</span><span class="sxs-lookup"><span data-stu-id="41e4d-158">The [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="41e4d-159">Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="41e4d-159">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="41e4d-160">In alcuni casi, una proprietà può essere recuperata tramite il metodo [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [IUIFramework:: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="41e4d-160">In some cases, a property can be retrieved through the [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

<span data-ttu-id="41e4d-161">Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo barra di accesso rapido (QAT).</span><span class="sxs-lookup"><span data-stu-id="41e4d-161">The following table lists the property keys that are associated with the Quick Access Toolbar (QAT) control.</span></span>

| <span data-ttu-id="41e4d-162">Chiave della proprietà</span><span class="sxs-lookup"><span data-stu-id="41e4d-162">Property Key</span></span> | <span data-ttu-id="41e4d-163">Note</span><span class="sxs-lookup"><span data-stu-id="41e4d-163">Notes</span></span> |
|---|---|
| [<span data-ttu-id="41e4d-164">Interfaccia utente \_ pkey \_ ItemsSource</span><span class="sxs-lookup"><span data-stu-id="41e4d-164">UI\_PKEY\_ItemsSource</span></span>](windowsribbon-reference-properties-uipkey-itemssource.md) | <span data-ttu-id="41e4d-165">Supporta [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (non supporta [IUIFramework:: SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [IUIFramework:: GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) restituisce un puntatore a un oggetto IUICollection che rappresenta i comandi in qat.</span><span class="sxs-lookup"><span data-stu-id="41e4d-165">Supports [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (does not support [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)).[IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) returns a pointer to an IUICollection object that represents the commands in the QAT.</span></span> <span data-ttu-id="41e4d-166">Ogni comando è identificato dal relativo ID di comando, ottenuto chiamando il metodo [IUISimplePropertySet:: GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) e passando l' [interfaccia utente della chiave \_ pkey \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md).</span><span class="sxs-lookup"><span data-stu-id="41e4d-166">Each Command is identified by its Command ID, which is obtained by calling the [IUISimplePropertySet::GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method and passing in the property key [UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md).</span></span> |

<span data-ttu-id="41e4d-167">Non sono presenti chiavi di proprietà associate all'elemento di comando **altri comandi** del menu a discesa della barra di accesso rapido (QAT)</span><span class="sxs-lookup"><span data-stu-id="41e4d-167">There are no property keys associated with the **More Commands** Command item of the Quick Access Toolbar (QAT) drop-down menu</span></span>

## <a name="related-topics"></a><span data-ttu-id="41e4d-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41e4d-168">Related topics</span></span>

- [<span data-ttu-id="41e4d-169">Libreria di controlli Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="41e4d-169">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
- [<span data-ttu-id="41e4d-170">Elemento di markup QuickAccessToolbar</span><span class="sxs-lookup"><span data-stu-id="41e4d-170">QuickAccessToolbar markup element</span></span>](windowsribbon-element-quickaccesstoolbar.md)