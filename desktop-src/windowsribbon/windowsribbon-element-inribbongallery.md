---
title: Elemento InRibbonGallery
description: Rappresenta la In-Ribbon, un controllo basato su raccolta che espone un subset predefinito di elementi direttamente nella barra multifunzione. Tutti gli elementi rimanenti vengono visualizzati quando si fa clic su un pulsante di menu a discesa.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- Elemento InRibbonGallery Barra multifunzione di Windows
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a25b2ebb937d954adce58231fd8c6b3347a031a7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443372"
---
# <a name="inribbongallery-element"></a>Elemento InRibbonGallery

Rappresenta la [raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md), un controllo basato su raccolta che espone un subset predefinito di elementi direttamente nella barra multifunzione. Tutti gli elementi rimanenti vengono visualizzati quando si fa clic su un pulsante di menu a discesa.

## <a name="usage"></a>Utilizzo

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
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
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command.</strong></a><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999 inclusi o valore esadecimale compreso tra 0x2 e 0xea5f inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>HasLargeItems</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Determina se la risorsa immagine grande o piccola del comando viene visualizzata nel controllo raccolta. <br/>
<blockquote>
[!Note]<br />
Si applica solo alle raccolte in cui il valore <em>dell'attributo Type</em> è uguale a <code>Command</code> .
</blockquote>
<br/> Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ItemHeight</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Insieme a <em>ItemWidth,</em>determina le dimensioni dell'immagine dell'elemento visualizzata nel controllo raccolta. <br/>
<blockquote>
[!Note]<br />
Si applica solo alle raccolte in cui il valore <em>dell'attributo Type</em> è uguale a <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Il valore predefinito è -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ItemWidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Insieme a <em>ItemHeight,</em>determina le dimensioni dell'immagine dell'elemento visualizzata nel controllo raccolta. <br/>
<blockquote>
[!Note]<br />
Si applica solo alle raccolte in cui il valore <em>dell'attributo Type</em> è uguale a <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Il valore predefinito è -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxColumns</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Specifica il numero massimo di colonne visualizzate da <strong>InRibbonGallery,</strong> ad esempio nell'elenco a discesa Layout gruppo di grandi dimensioni. <em></em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MaxColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Specifica il numero massimo di colonne visualizzate da <strong>InRibbonGallery</strong> nel layout gruppo Medio, prima di passare al layout <em>Large.</em> <em></em> <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxRows</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Specifica il numero massimo di righe per il layout degli <strong>elementi InRibbonGallery.</strong> <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> Il valore predefinito è 1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinColumnsLarge</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Specifica il numero minimo di colonne visualizzate da <strong>InRibbonGallery</strong> nel layout Gruppo di grandi dimensioni, prima di passare a <em>Medio.</em> <em></em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MinColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>No<br/></td>
<td>Specifica il numero minimo di colonne visualizzate da <strong>InRibbonGallery</strong> nel layout del gruppo <em>Medium,</em> prima di passare a <em>Small.</em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>No<br/></td>
<td>Specifica dove viene visualizzata l'etichetta dell'elemento, rispetto all'immagine. <br/> Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Inferiore)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Nascondi)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (A sinistra)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Sovrapposizione)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (A destra)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (In alto)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Tipo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Elementi)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Comandi)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                                           | Descrizione                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Casella**](windowsribbon-element-checkbox.md)<br/>                                     | Può verificarsi una o più volte<br/> <br/> |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/> | Deve verificarsi esattamente una volta<br/> <br/>     |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/> | Può verificarsi al massimo una volta<br/> <br/>      |
| [**Pulsante**](windowsribbon-element-button.md)<br/>                                       | Può verificarsi una o più volte<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                               | Può verificarsi una o più volte<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                             | Può verificarsi una o più volte<br/> <br/> |



## <a name="parent-elements"></a>Elementi padre



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Gruppo</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 e più recente.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per [**ogni elemento ControlGroup**](windowsribbon-element-controlgroup.md) [**o Group.**](windowsribbon-element-group.md)

La schermata seguente illustra il controllo [Raccolta barra](windowsribbon-controls-inribbongallery.md) multifunzione in Microsoft Paint per Windows 7.

![Screenshot di un controllo della raccolta nella barra multifunzione di Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per [una raccolta nella barra multifunzione](windowsribbon-controls-inribbongallery.md).

Questa sezione di codice illustra le dichiarazioni del comando **InRibbonGallery,** con un [**gruppo**](windowsribbon-element-group.md) associato che funge da contenitore padre per l'elemento **InRibbonGallery.**


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



Questa sezione di codice illustra le **dichiarazioni di controllo InRibbonGallery.**


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


* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** No



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Raccolta barra multifunzione](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Uso delle raccolte](ribbon-controls-galleries.md)
</dt> <dt>

[Esempio di raccolta](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





