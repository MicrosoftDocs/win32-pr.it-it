---
title: Visualizzazione di schede contestuali
description: In un'applicazione della barra multifunzione di Windows una scheda contestuale è un controllo struttura a schede nascosto visualizzato nella scheda quando viene selezionato o evidenziato un oggetto nell'area di lavoro dell'applicazione, ad esempio un'immagine.
ms.assetid: 2059ca42-6a99-43a2-b1f5-ce5554156993
keywords:
- Barra multifunzione di Windows, schede contestuali
- Barra multifunzione, schede contestuali
- visualizzazione delle schede contestuali della barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a1e81ac6587e39a04114fa2f938a6da0e9a4d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727367"
---
# <a name="displaying-contextual-tabs"></a><span data-ttu-id="97a70-106">Visualizzazione di schede contestuali</span><span class="sxs-lookup"><span data-stu-id="97a70-106">Displaying Contextual Tabs</span></span>

<span data-ttu-id="97a70-107">In un'applicazione della barra multifunzione di Windows una scheda contestuale è un controllo struttura a [schede](windowsribbon-controls-tab.md) nascosto visualizzato nella scheda quando viene selezionato o evidenziato un oggetto nell'area di lavoro dell'applicazione, ad esempio un'immagine.</span><span class="sxs-lookup"><span data-stu-id="97a70-107">In a Windows Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

-   [<span data-ttu-id="97a70-108">Introduzione</span><span class="sxs-lookup"><span data-stu-id="97a70-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="97a70-109">Implementazione di schede contestuali</span><span class="sxs-lookup"><span data-stu-id="97a70-109">Implementing Contextual Tabs</span></span>](#implementing-contextual-tabs)
    -   [<span data-ttu-id="97a70-110">markup</span><span class="sxs-lookup"><span data-stu-id="97a70-110">Markup</span></span>](#markup)
    -   [<span data-ttu-id="97a70-111">Codice</span><span class="sxs-lookup"><span data-stu-id="97a70-111">Code</span></span>](#code)
-   [<span data-ttu-id="97a70-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97a70-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="97a70-113">Introduzione</span><span class="sxs-lookup"><span data-stu-id="97a70-113">Introduction</span></span>

<span data-ttu-id="97a70-114">Diversamente dalle schede principali, che contengono vari comandi comuni che sono rilevanti indipendentemente dal contesto dell'area di lavoro, le schede contestuali contengono in genere uno o più comandi applicabili solo a un oggetto selezionato o evidenziato.</span><span class="sxs-lookup"><span data-stu-id="97a70-114">In contrast to core tabs, which contain various common Commands that are relevant regardless of workspace context, contextual tabs typically contain one or more Commands that are applicable to a selected or highlighted object only.</span></span>

<span data-ttu-id="97a70-115">Quando un oggetto viene selezionato o evidenziato nell'area di lavoro dell'applicazione, il tipo e il contesto dell'oggetto potrebbero richiedere comandi diversi che non rendono il senso aziendale o funzionale in una scheda contestuale. In questi casi, potrebbe essere necessario disporre di più schede contestuali, contenute all'interno di un [gruppo di schede](windowsribbon-controls-tabgroup.md).</span><span class="sxs-lookup"><span data-stu-id="97a70-115">When an object is selected or highlighted in the application workspace, the type and context of the object might require disparate Commands that do not make organizational or functional sense on one contextual tab. In these cases, multiple contextual tabs, which are contained within a [Tab Group](windowsribbon-controls-tabgroup.md), may be required.</span></span> <span data-ttu-id="97a70-116">Ad esempio, la selezione di un'immagine contenuta in una cella della tabella potrebbe richiedere due schede contestuali che espongono le funzionalità di tabella e immagine.</span><span class="sxs-lookup"><span data-stu-id="97a70-116">For example, selecting an image contained in a table cell might require two contextual tabs that expose both table and image functionality.</span></span>

> [!Note]  
> <span data-ttu-id="97a70-117">Oltre a più schede contestuali, il Framework della barra multifunzione supporta anche più controlli [gruppo di schede](windowsribbon-controls-tabgroup.md) in una barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="97a70-117">In addition to multiple contextual tabs, the Ribbon framework also supports multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls within a ribbon.</span></span>

 

<span data-ttu-id="97a70-118">Quando si visualizzano le schede contestuali, il Framework della barra multifunzione impone un set di comportamenti di base che includono:</span><span class="sxs-lookup"><span data-stu-id="97a70-118">When displaying contextual tabs, the Ribbon framework enforces a basic set of behaviors that include:</span></span>

-   <span data-ttu-id="97a70-119">Le schede contestuali sono posizionate nell'ordine in cui sono dichiarate e a destra delle schede principali nella riga della scheda della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="97a70-119">Contextual tabs are positioned in the order they are declared and to the right of core tabs in the ribbon tab row.</span></span>
-   <span data-ttu-id="97a70-120">Quando la barra multifunzione viene ridimensionata, le tabulazioni vengono ridimensionate e le etichette di tabulazione vengono troncate come richiesto dallo spazio.</span><span class="sxs-lookup"><span data-stu-id="97a70-120">When the ribbon is resized, tabs are scaled and tab labels are truncated as space requires.</span></span> <span data-ttu-id="97a70-121">Tuttavia, alle schede contestuali visibili viene assegnata una priorità di visualizzazione superiore in cui vengono ridimensionate e troncate per ultime.</span><span class="sxs-lookup"><span data-stu-id="97a70-121">However, visible contextual tabs are given a higher display priority in which they are scaled and truncated last.</span></span>
-   <span data-ttu-id="97a70-122">L'etichetta per un [gruppo di schede](windowsribbon-controls-tabgroup.md) viene visualizzata nella barra del titolo dell'applicazione e si estende a tutte le schede contestuali associate.</span><span class="sxs-lookup"><span data-stu-id="97a70-122">The label for a [Tab Group](windowsribbon-controls-tabgroup.md) is displayed in the application title bar and spans all associated contextual tabs.</span></span>
-   <span data-ttu-id="97a70-123">Quando più controlli [gruppo di schede](windowsribbon-controls-tabgroup.md) vengono visualizzati contemporaneamente, uno dei cinque colori univoci viene assegnato allo sfondo di ogni gruppo di schede nella barra del titolo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97a70-123">When multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at the same time, one of five unique colors is assigned to the background of each Tab Group in the application title bar.</span></span> <span data-ttu-id="97a70-124">Questo colore viene usato anche come colore di evidenziazione per le schede contestuali nel gruppo di schede.</span><span class="sxs-lookup"><span data-stu-id="97a70-124">This color is also used as a highlight color for the contextual tabs in the Tab Group.</span></span>
-   <span data-ttu-id="97a70-125">L'assegnazione dei colori del [gruppo di schede](windowsribbon-controls-tabgroup.md) è basata sull'ordine con cui gli elementi del gruppo di schede sono dichiarati nel markup.</span><span class="sxs-lookup"><span data-stu-id="97a70-125">The [Tab Group](windowsribbon-controls-tabgroup.md) color assignment is based on the order the Tab Group elements are declared in markup.</span></span> <span data-ttu-id="97a70-126">I colori sono definiti dal Framework e non possono essere specificati dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97a70-126">The colors are defined by the framework and cannot be specified by the application.</span></span>
-   <span data-ttu-id="97a70-127">I colori del [gruppo di schede](windowsribbon-controls-tabgroup.md) definiti dal Framework possono essere modificati indirettamente tramite le chiavi delle proprietà del [Framework](windowsribbon-reference-properties-framework.md) .</span><span class="sxs-lookup"><span data-stu-id="97a70-127">The [Tab Group](windowsribbon-controls-tabgroup.md) colors defined by the framework can be modified indirectly through the [Framework Properties](windowsribbon-reference-properties-framework.md) property keys.</span></span> <span data-ttu-id="97a70-128">Per ulteriori informazioni, vedere [personalizzazione dei colori della barra multifunzione](ribbon-color.md).</span><span class="sxs-lookup"><span data-stu-id="97a70-128">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>
-   <span data-ttu-id="97a70-129">Quando più di cinque controlli [gruppo di schede](windowsribbon-controls-tabgroup.md) vengono visualizzati in una sola volta, il Framework esegue il ciclo dei colori associati.</span><span class="sxs-lookup"><span data-stu-id="97a70-129">When more than five [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at any single time, the framework cycles the associated colors.</span></span>
-   <span data-ttu-id="97a70-130">Il numero massimo di controlli struttura a [schede](windowsribbon-controls-tab.md) in una barra multifunzione è limitato a 100.</span><span class="sxs-lookup"><span data-stu-id="97a70-130">The maximum number of [Tab](windowsribbon-controls-tab.md) controls in a ribbon is limited to 100.</span></span> <span data-ttu-id="97a70-131">Sono incluse le schede contestuali, visibili o meno.</span><span class="sxs-lookup"><span data-stu-id="97a70-131">This includes contextual tabs, visible or not.</span></span>

<span data-ttu-id="97a70-132">Lo screenshot seguente mostra una scheda contestuale del disegno di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="97a70-132">The following screen shot shows a contextual tab from Windows 7 Paint.</span></span>

![screenshot che mostra un controllo scheda contestuale.](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a><span data-ttu-id="97a70-134">Implementazione di schede contestuali</span><span class="sxs-lookup"><span data-stu-id="97a70-134">Implementing Contextual Tabs</span></span>

<span data-ttu-id="97a70-135">In questa sezione vengono illustrati i dettagli di implementazione delle schede contestuali della barra multifunzione e viene illustrato come incorporarli in un'applicazione Ribbon.</span><span class="sxs-lookup"><span data-stu-id="97a70-135">This section discusses the implementation details of Ribbon contextual tabs and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="markup"></a><span data-ttu-id="97a70-136">markup</span><span class="sxs-lookup"><span data-stu-id="97a70-136">Markup</span></span>

<span data-ttu-id="97a70-137">Gli esempi seguenti illustrano il markup di base per un elemento [**TabGroup**](windowsribbon-element-tabgroup.md) che contiene due schede contestuali.</span><span class="sxs-lookup"><span data-stu-id="97a70-137">The following examples demonstrate the basic markup for a [**TabGroup**](windowsribbon-element-tabgroup.md) element that contains two contextual tabs.</span></span>

<span data-ttu-id="97a70-138">Questa sezione di codice mostra le dichiarazioni dei comandi [**TabGroup**](windowsribbon-element-tabgroup.md) e [Tab](windowsribbon-controls-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="97a70-138">This section of code shows the [**TabGroup**](windowsribbon-element-tabgroup.md) and [Tab](windowsribbon-controls-tab.md) Command declarations.</span></span>


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



<span data-ttu-id="97a70-139">In questa sezione del codice vengono illustrate le dichiarazioni di controllo necessarie per visualizzare due schede contestuali all'interno di un [**TabGroup**](windowsribbon-element-tabgroup.md).</span><span class="sxs-lookup"><span data-stu-id="97a70-139">This section of code shows the control declarations required to display two contextual tabs within a [**TabGroup**](windowsribbon-element-tabgroup.md).</span></span>


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



### <a name="code"></a><span data-ttu-id="97a70-140">Codice</span><span class="sxs-lookup"><span data-stu-id="97a70-140">Code</span></span>

<span data-ttu-id="97a70-141">[Interfaccia utente \_ PKEY \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) è la singola chiave di proprietà definita dal Framework per specificare la visibilità e lo stato delle schede contestuali.</span><span class="sxs-lookup"><span data-stu-id="97a70-141">[UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) is the single property key defined by the framework for specifying the visibility and state of contextual tabs.</span></span> <span data-ttu-id="97a70-142">Quando si seleziona un oggetto nell'area di lavoro dell'applicazione, è possibile assegnare a questa proprietà uno dei tre valori dell'enumerazione [**\_ CONTEXTAVAILABILITY dell'interfaccia utente**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) che definiscono se una scheda contestuale esiste e, in tal caso, se viene visualizzata come scheda attiva.</span><span class="sxs-lookup"><span data-stu-id="97a70-142">When an object is selected in the application workspace, this property can be assigned one of three values from the [**UI\_CONTEXTAVAILABILITY**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) enumeration that define whether a contextual tab exists and, if it does, whether it is shown as the active tab.</span></span>

<span data-ttu-id="97a70-143">Un'applicazione richiede un aggiornamento del [gruppo di schede](windowsribbon-controls-tabgroup.md) invalidando e aggiornando la proprietà [ \_ pkey \_ ContextAvailable dell'interfaccia utente](windowsribbon-reference-properties-uipkey-contextavailable.md) quando viene modificato il contesto dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="97a70-143">An application requests a [Tab Group](windowsribbon-controls-tabgroup.md) update by invalidating and updating the [UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) property when the workspace context changes.</span></span>

<span data-ttu-id="97a70-144">Nelle sezioni seguenti del codice viene illustrato come visualizzare una scheda contestuale quando si seleziona un'immagine in un'area di lavoro dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97a70-144">The follow sections of code demonstrate how to display a contextual tab when an image is selected in an application workspace.</span></span>


```C++
// Initialize the image tools contextual tab visibility setting.
UI_CONTEXTAVAILABILITY g_ImageTools = UI_CONTEXTAVAILABILITY_NOTAVAILABLE;

// Called when an image is selected in the application.
void SelectImage()
{
  ...
  g_ImageTools = UI_CONTEXTAVAILABILITY_ACTIVE;

  // Invalidate the UI_PKEY_ContextAvailable property of the image tools  
  // contextual tab Command and trigger the UpdatePropery callback function.
  pUIFramework->InvalidateUICommand(
                  cmdImageTabSet, 
                  UI_INVALIDATIONS_PROPERTY, 
                  UI_PKEY_ContextAvailable);
  ...
}

// Update Tab Group properties.
HRESULT MyTabGroupCommandHandler::UpdateProperty(
                                  UINT nCmdID,
                                  REFPROPERTYKEY key,
                                  const PROPVARIANT* ppropvarCurrentValue,
                                  PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_FAIL;

  if (key == UI_PKEY_ContextAvailable)
  {
    hr = UIInitPropertyFromUInt32(key, g_ImageTools, ppropvarNewValue);
  }
  ...
  return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="97a70-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97a70-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97a70-146">Linee guida sull'esperienza utente della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="97a70-146">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="97a70-147">Processo di progettazione della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="97a70-147">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 