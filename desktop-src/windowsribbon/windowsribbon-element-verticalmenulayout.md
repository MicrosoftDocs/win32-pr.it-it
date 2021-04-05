---
title: Elemento VerticalMenuLayout
description: Rappresenta un layout verticale per gli elementi in una raccolta.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- Barra multifunzione Windows elemento VerticalMenuLayout
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fb848edcc8ab5ddff1405f35d5abd414ae40d15
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/30/2020
ms.locfileid: "103724343"
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
<td><strong>Gripper</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Un handle di ridimensionamento collegato all'elenco a discesa della raccolta. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> Nessuno<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Verticale<br/> </dt> <dd> Valore predefinito. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsMultipleHighlightingEnabled</strong><br/></td>
<td>xs:boolean<br/></td>
<td>No<br/></td>
<td><strong>Windows 8 e versioni successive</strong><br/> Consente di evidenziare tutti gli elementi dell'elenco fino a, incluso, l'elemento MouseOver corrente (anziché solo l'elemento MouseOver). Usato in genere per più funzionalità di <strong>annullamento</strong> e <strong>ripristino</strong> .<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> false<br/> </dt> <dd> Valore predefinito. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>prime righe</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Specifica il numero di righe di elementi che devono essere visibili senza scorrimento. <br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: Integer)<br/> </dt> <dd> Qualsiasi numero intero positivo o negativo. <br/> Il valore predefinito è <strong>-1</strong> , che specifica di visualizzare il maggior numero possibile di righe di elementi.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [**Inribbongallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a>Commenti

Obbligatorio.

L'elemento **VerticalMenuLayout** o [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md) deve essere presente una volta per ogni elemento [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**inribbongallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)o [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per un elemento **VerticalMenuLayout** .

In questa sezione del codice vengono illustrate le dichiarazioni di controllo [**inribbongallery**](windowsribbon-element-inribbongallery.md) .


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



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | Sì       |



 

 





