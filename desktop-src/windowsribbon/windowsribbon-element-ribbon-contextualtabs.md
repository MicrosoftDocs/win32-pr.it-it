---
title: Ribbon. ContextualTabs, proprietà
description: Rappresenta un contenitore per le schede contestuali.
ms.assetid: 1f57a8d7-97ac-4007-8a36-c6aec5b85e6c
keywords:
- Barra multifunzione di Windows della proprietà Ribbon. ContextualTabs
topic_type:
- apiref
api_name:
- Ribbon.ContextualTabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790a7c93df71ab5117b591367c6b80fc0f8a748d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740535"
---
# <a name="ribboncontextualtabs-property"></a><span data-ttu-id="700c2-104">Ribbon. ContextualTabs, proprietà</span><span class="sxs-lookup"><span data-stu-id="700c2-104">Ribbon.ContextualTabs property</span></span>

<span data-ttu-id="700c2-105">Rappresenta un contenitore per le schede contestuali.</span><span class="sxs-lookup"><span data-stu-id="700c2-105">Represents a container for contextual tabs.</span></span>

## <a name="usage"></a><span data-ttu-id="700c2-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="700c2-106">Usage</span></span>

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a><span data-ttu-id="700c2-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="700c2-107">Attributes</span></span>

<span data-ttu-id="700c2-108">Non ci sono attributi.</span><span class="sxs-lookup"><span data-stu-id="700c2-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="700c2-109">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="700c2-109">Child elements</span></span>



| <span data-ttu-id="700c2-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="700c2-110">Element</span></span>                                                       | <span data-ttu-id="700c2-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="700c2-111">Description</span></span>                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="700c2-112">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="700c2-112">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/> | <span data-ttu-id="700c2-113">Deve essere presente almeno una volta</span><span class="sxs-lookup"><span data-stu-id="700c2-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="700c2-114">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="700c2-114">Parent elements</span></span>



| <span data-ttu-id="700c2-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="700c2-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="700c2-116">**Barra multifunzione**</span><span class="sxs-lookup"><span data-stu-id="700c2-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="700c2-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="700c2-117">Remarks</span></span>

<span data-ttu-id="700c2-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="700c2-118">Optional.</span></span>

<span data-ttu-id="700c2-119">Può essere presente al massimo una volta per ogni [**barra multifunzione**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="700c2-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

<span data-ttu-id="700c2-120">Le schede contestuali sono utili per visualizzare le funzionalità rilevanti solo per un contesto dell'applicazione specifico, ad esempio una scheda formattazione immagine in un editor di testo visualizzato solo quando viene evidenziata un'immagine.</span><span class="sxs-lookup"><span data-stu-id="700c2-120">Contextual tabs are useful for displaying functionality that is relevant only to a specific application context, such as an image formatting tab in a text editor that is displayed only when an image is highlighted.</span></span> <span data-ttu-id="700c2-121">In genere, le schede contestuali non sono visibili fino a quando non si verifica un contesto di applicazione specifico e l'applicazione invia una notifica al framework della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="700c2-121">Typically, contextual tabs are not visible until a specific application context occurs, and the application notifies the Ribbon framework.</span></span>

<span data-ttu-id="700c2-122">Quando vengono visualizzate, le schede contestuali sono codificate con colori per distinguerle dalle schede normali.</span><span class="sxs-lookup"><span data-stu-id="700c2-122">When displayed, contextual tabs are color coded to differentiate them from regular tabs.</span></span>

## <a name="examples"></a><span data-ttu-id="700c2-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="700c2-123">Examples</span></span>

<span data-ttu-id="700c2-124">Nell'esempio seguente viene illustrato il markup di base per l'elemento **Ribbon. ContextualTabs** .</span><span class="sxs-lookup"><span data-stu-id="700c2-124">The following example demonstrates the basic markup for the **Ribbon.ContextualTabs** element.</span></span>

<span data-ttu-id="700c2-125">Questa sezione di codice mostra una dichiarazione di comando [**TabGroup**](windowsribbon-element-tabgroup.md) e due dichiarazioni di comando per [**schede**](windowsribbon-element-tab.md) contestuali.</span><span class="sxs-lookup"><span data-stu-id="700c2-125">This section of code shows a [**TabGroup**](windowsribbon-element-tabgroup.md) Command declaration and two contextual [**Tab**](windowsribbon-element-tab.md) Command declarations.</span></span>


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



<span data-ttu-id="700c2-126">Questa sezione di codice mostra la dichiarazione di controllo **Ribbon. ContextualTabs** con un [**TabGroup**](windowsribbon-element-tabgroup.md) e due controlli della [**scheda**](windowsribbon-element-tab.md) contestuale.</span><span class="sxs-lookup"><span data-stu-id="700c2-126">This section of code shows the **Ribbon.ContextualTabs** control declaration with a [**TabGroup**](windowsribbon-element-tabgroup.md) and two contextual [**Tab**](windowsribbon-element-tab.md) controls.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="700c2-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="700c2-127">Requirements</span></span>



| <span data-ttu-id="700c2-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="700c2-128">Requirement</span></span> | <span data-ttu-id="700c2-129">Valore</span><span class="sxs-lookup"><span data-stu-id="700c2-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="700c2-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="700c2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="700c2-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="700c2-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="700c2-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="700c2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="700c2-133">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="700c2-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="700c2-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="700c2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="700c2-135">**Ribbon. Tabs**</span><span class="sxs-lookup"><span data-stu-id="700c2-135">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)
</dt> </dl>

 

 





