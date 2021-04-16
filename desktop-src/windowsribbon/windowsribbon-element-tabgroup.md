---
title: Elemento TabGroup
description: Rappresenta un set contestuale di controlli struttura a schede.
ms.assetid: f131efe1-b8c4-416e-997a-5e2d3bcc03ea
keywords:
- Barra multifunzione Windows elemento TabGroup
topic_type:
- apiref
api_name:
- TabGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fcbe0760c850f37c6a7bf348c38e48aa7cf54ddc
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104223036"
---
# <a name="tabgroup-element"></a><span data-ttu-id="8f7f9-104">Elemento TabGroup</span><span class="sxs-lookup"><span data-stu-id="8f7f9-104">TabGroup element</span></span>

<span data-ttu-id="8f7f9-105">Rappresenta un set contestuale di controlli struttura a [schede](windowsribbon-controls-tabgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="8f7f9-105">Represents a contextual set of [Tab](windowsribbon-controls-tabgroup.md) controls.</span></span>

## <a name="usage"></a><span data-ttu-id="8f7f9-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="8f7f9-106">Usage</span></span>

``` syntax
<TabGroup
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</TabGroup>
```

## <a name="attributes"></a><span data-ttu-id="8f7f9-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="8f7f9-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f7f9-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="8f7f9-108">Attribute</span></span></th>
<th><span data-ttu-id="8f7f9-109">Type</span><span class="sxs-lookup"><span data-stu-id="8f7f9-109">Type</span></span></th>
<th><span data-ttu-id="8f7f9-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="8f7f9-110">Required</span></span></th>
<th><span data-ttu-id="8f7f9-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f7f9-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f7f9-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="8f7f9-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="8f7f9-113">XS: positiveInteger o xs: String</span><span class="sxs-lookup"><span data-stu-id="8f7f9-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="8f7f9-114">No</span><span class="sxs-lookup"><span data-stu-id="8f7f9-114">No</span></span><br/></td>
<td><span data-ttu-id="8f7f9-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8f7f9-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="8f7f9-116">
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)</span><span class="sxs-lookup"><span data-stu-id="8f7f9-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="8f7f9-117">Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi.</span><span class="sxs-lookup"><span data-stu-id="8f7f9-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="8f7f9-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="8f7f9-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="8f7f9-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="8f7f9-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="8f7f9-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8f7f9-120">Child elements</span></span>



| <span data-ttu-id="8f7f9-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="8f7f9-121">Element</span></span>                                             | <span data-ttu-id="8f7f9-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f7f9-122">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="8f7f9-123">**Scheda**</span><span class="sxs-lookup"><span data-stu-id="8f7f9-123">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="8f7f9-124">Deve essere presente almeno una volta</span><span class="sxs-lookup"><span data-stu-id="8f7f9-124">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="8f7f9-125">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="8f7f9-125">Parent elements</span></span>



| <span data-ttu-id="8f7f9-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="8f7f9-126">Element</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f7f9-127">**Ribbon. ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="8f7f9-127">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8f7f9-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f7f9-128">Remarks</span></span>

<span data-ttu-id="8f7f9-129">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8f7f9-129">Required.</span></span>

<span data-ttu-id="8f7f9-130">Deve essere presente almeno una volta per ogni elemento [**Ribbon. ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) .</span><span class="sxs-lookup"><span data-stu-id="8f7f9-130">Must occur at least once for each [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="8f7f9-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="8f7f9-131">Examples</span></span>

<span data-ttu-id="8f7f9-132">Nell'esempio seguente viene illustrato il markup di base per l'elemento **TabGroup** .</span><span class="sxs-lookup"><span data-stu-id="8f7f9-132">The following example demonstrates the basic markup for the **TabGroup** element.</span></span>

<span data-ttu-id="8f7f9-133">In questa sezione del codice viene illustrata una dichiarazione di comando **TabGroup** con due schede contestuali.</span><span class="sxs-lookup"><span data-stu-id="8f7f9-133">This section of code shows a **TabGroup** Command declaration with two contextual tabs.</span></span>


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



<span data-ttu-id="8f7f9-134">In questa sezione del codice vengono illustrate le dichiarazioni di controllo **TabGroup** corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="8f7f9-134">This section of code shows corresponding **TabGroup** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="8f7f9-135">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="8f7f9-135">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="8f7f9-136">Sistema minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f7f9-136">Minimum supported system</span></span><br/> | <span data-ttu-id="8f7f9-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8f7f9-137">Windows 7</span></span> |
| <span data-ttu-id="8f7f9-138">Può essere vuoto</span><span class="sxs-lookup"><span data-stu-id="8f7f9-138">Can be empty</span></span>                        | <span data-ttu-id="8f7f9-139">No</span><span class="sxs-lookup"><span data-stu-id="8f7f9-139">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="8f7f9-140">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8f7f9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f7f9-141">Controllo gruppo schede</span><span class="sxs-lookup"><span data-stu-id="8f7f9-141">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="8f7f9-142">Controllo Tab</span><span class="sxs-lookup"><span data-stu-id="8f7f9-142">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> </dl>

 

 





