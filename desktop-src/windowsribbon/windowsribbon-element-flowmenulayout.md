---
title: Elemento FlowMenuLayout
description: Rappresenta un layout orizzontale con interruzioni di riga per gli elementi in una raccolta.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Barra multifunzione Windows elemento FlowMenuLayout
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ec9690dd9839755a90abee4c8649c32eae4db6b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299231"
---
# <a name="flowmenulayout-element"></a>Elemento FlowMenuLayout

Rappresenta un layout orizzontale con interruzioni di riga per gli elementi in una raccolta.

## <a name="usage"></a>Utilizzo

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
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
<td><strong>Colonne</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Specifica il numero di elementi da visualizzare in una singola riga.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: Integer)<br/> </dt> <dd> Qualsiasi numero intero positivo o negativo. <br/> Il valore predefinito è <strong>2</strong>. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Gripper</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Un handle di ridimensionamento collegato all'elenco a discesa della raccolta. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> Nessuno<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Verticale<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Angolo<br/> </dt> <dd> Valore predefinito. <br/> </dd> </dl></td>
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

L'elemento [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) o **FlowMenuLayout** deve essere presente una volta per ogni elemento [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md), [**inribbongallery. MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)o [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .

Gli elementi sono disposti in base alle proprietà di interruzioni di riga inerenti gli attributi di *riga* e *colonna* . Quando il contenuto supera la lunghezza di una singola riga, il menu interrompe le righe, esegue il wrapping delle righe e allinea il contenuto in modo appropriato.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).

Questa sezione di codice mostra la dichiarazione di controllo [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) con una specifica **FlowMenuLayout** .


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | Sì       |



 

 





