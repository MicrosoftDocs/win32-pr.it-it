---
title: Elemento VerticalMenuLayout
description: Rappresenta un layout verticale per gli elementi in una raccolta.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- Barra multifunzione di Windows per l'elemento VerticalMenuLayout
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e6f3e4a691c9691b9bc6c8c6d760bb10635d8d8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444052"
---
# <a name="verticalmenulayout-element"></a>Elemento VerticalMenuLayout

Rappresenta un layout verticale per gli elementi in una raccolta.

## <a name="usage"></a>Utilizzo

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
```

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Type</th>
<th>Obbligatoria</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Pinza</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Handle di ridimensionamento collegato all'elenco a discesa della raccolta. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Nessuno)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Verticale)<br/> </dt> <dd> Valore predefinito. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsMultipleHighlightingEnabled</strong><br/></td>
<td>xs:boolean<br/></td>
<td>No<br/></td>
<td><strong>Windows 8 e più recente</strong><br/> Evidenzia tutti gli elementi nell'elenco fino all'elemento corrente di passaggio del mouse (anziché solo all'elemento di passaggio del mouse). In genere viene usato per <strong>più funzionalità di</strong> <strong>annullamento e di annullamento.</strong><br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Valore predefinito. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>prime righe</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Specifica il numero di righe di elementi da visualizzare senza scorrimento. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Qualsiasi numero intero positivo o negativo. <br/> Il valore predefinito <strong>è -1,</strong> che specifica di visualizzare il maggior numero possibile di righe di elementi.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

L'elemento **VerticalMenuLayout** o [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) deve essere presente una volta per ogni elemento [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)o [**SplitButtonGallery.MenuLayout.**](windowsribbon-element-splitbuttongallery-menulayout.md)

## <a name="examples"></a>Esempio

L'esempio seguente illustra il markup di base per **un elemento VerticalMenuLayout.**

Questa sezione di codice illustra le dichiarazioni del controllo [**InRibbonGallery.**](windowsribbon-element-inribbongallery.md)


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a>Informazioni sull'elemento


- **Sistema minimo supportato:** Windows 7 
- **Può essere vuoto:** Sì



 

 





