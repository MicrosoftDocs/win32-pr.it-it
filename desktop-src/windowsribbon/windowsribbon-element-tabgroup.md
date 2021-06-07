---
title: Elemento TabGroup
description: Rappresenta un set contestuale di controlli Tab.
ms.assetid: f131efe1-b8c4-416e-997a-5e2d3bcc03ea
keywords:
- Elemento TabGroup Nella barra multifunzione di Windows
topic_type:
- apiref
api_name:
- TabGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4c18db72d6b0161842bfde9d5a836d14189c6a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444062"
---
# <a name="tabgroup-element"></a><span data-ttu-id="1eea6-104">Elemento TabGroup</span><span class="sxs-lookup"><span data-stu-id="1eea6-104">TabGroup element</span></span>

<span data-ttu-id="1eea6-105">Rappresenta un set contestuale di [controlli Tab.](windowsribbon-controls-tabgroup.md)</span><span class="sxs-lookup"><span data-stu-id="1eea6-105">Represents a contextual set of [Tab](windowsribbon-controls-tabgroup.md) controls.</span></span>

## <a name="usage"></a><span data-ttu-id="1eea6-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="1eea6-106">Usage</span></span>

``` syntax
<TabGroup
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</TabGroup>
```

## <a name="attributes"></a><span data-ttu-id="1eea6-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="1eea6-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1eea6-108">Attributo</span><span class="sxs-lookup"><span data-stu-id="1eea6-108">Attribute</span></span></th>
<th><span data-ttu-id="1eea6-109">Type</span><span class="sxs-lookup"><span data-stu-id="1eea6-109">Type</span></span></th>
<th><span data-ttu-id="1eea6-110">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="1eea6-110">Required</span></span></th>
<th><span data-ttu-id="1eea6-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1eea6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1eea6-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="1eea6-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="1eea6-113">xs:positiveInteger o xs:string</span><span class="sxs-lookup"><span data-stu-id="1eea6-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="1eea6-114">No</span><span class="sxs-lookup"><span data-stu-id="1eea6-114">No</span></span><br/></td>
<td><span data-ttu-id="1eea6-115">Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a></span><span class="sxs-lookup"><span data-stu-id="1eea6-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="1eea6-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)</span><span class="sxs-lookup"><span data-stu-id="1eea6-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1eea6-117">Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi.</span><span class="sxs-lookup"><span data-stu-id="1eea6-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="1eea6-118">Il valore deve essere univoco all'interno del documento XML della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="1eea6-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="1eea6-119">Lunghezza massima: 100 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1eea6-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="1eea6-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="1eea6-120">Child elements</span></span>



| <span data-ttu-id="1eea6-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="1eea6-121">Element</span></span>                                             | <span data-ttu-id="1eea6-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1eea6-122">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="1eea6-123">**Scheda**</span><span class="sxs-lookup"><span data-stu-id="1eea6-123">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="1eea6-124">Deve verificarsi almeno una volta</span><span class="sxs-lookup"><span data-stu-id="1eea6-124">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="1eea6-125">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="1eea6-125">Parent elements</span></span>



| <span data-ttu-id="1eea6-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="1eea6-126">Element</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="1eea6-127">**Ribbon.ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="1eea6-127">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1eea6-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="1eea6-128">Remarks</span></span>

<span data-ttu-id="1eea6-129">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1eea6-129">Required.</span></span>

<span data-ttu-id="1eea6-130">Deve verificarsi almeno una volta per [**ogni elemento Ribbon.ContextualTabs.**](windowsribbon-element-ribbon-contextualtabs.md)</span><span class="sxs-lookup"><span data-stu-id="1eea6-130">Must occur at least once for each [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="1eea6-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="1eea6-131">Examples</span></span>

<span data-ttu-id="1eea6-132">L'esempio seguente illustra il markup di base per **l'elemento TabGroup.**</span><span class="sxs-lookup"><span data-stu-id="1eea6-132">The following example demonstrates the basic markup for the **TabGroup** element.</span></span>

<span data-ttu-id="1eea6-133">Questa sezione di codice mostra una dichiarazione **di comando TabGroup** con due schede contestuali.</span><span class="sxs-lookup"><span data-stu-id="1eea6-133">This section of code shows a **TabGroup** Command declaration with two contextual tabs.</span></span>


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



<span data-ttu-id="1eea6-134">Questa sezione di codice mostra le dichiarazioni **di controllo TabGroup** corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="1eea6-134">This section of code shows corresponding **TabGroup** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="1eea6-135">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="1eea6-135">Element information</span></span>

- <span data-ttu-id="1eea6-136">**Sistema minimo supportato:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="1eea6-136">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="1eea6-137">**Può essere vuoto:** No</span><span class="sxs-lookup"><span data-stu-id="1eea6-137">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="1eea6-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1eea6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eea6-139">Controllo Gruppo di schede</span><span class="sxs-lookup"><span data-stu-id="1eea6-139">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="1eea6-140">Controllo Tab</span><span class="sxs-lookup"><span data-stu-id="1eea6-140">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> </dl>

 

 





