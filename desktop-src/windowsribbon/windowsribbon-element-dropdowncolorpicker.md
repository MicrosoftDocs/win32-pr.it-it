---
title: Elemento DropDownColorPicker
description: Rappresenta un Pickercontrol colore Drop-Down che, quando selezionato, Visualizza una tavolozza dei campioni di colore.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- Barra multifunzione Windows elemento DropDownColorPicker
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 00185d14d9066b2cb85da4b23959e84df1827007
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "103720490"
---
# <a name="dropdowncolorpicker-element"></a>Elemento DropDownColorPicker

Rappresenta un controllo [selezione colori a discesa](windowsribbon-controls-dropdowncolorpicker.md)che, quando selezionato, Visualizza una tavolozza di campioni colore.

## <a name="usage"></a>Utilizzo

``` syntax
<DropDownColorPicker
  CommandName = "xs:positiveInteger or xs:string"
  Columns = "xs:positiveInteger"
  ThemeColorGridRows = "xs:positiveInteger"
  StandardColorGridRows = "xs:positiveInteger"
  RecentColorGridRows = "xs:positiveInteger"
  IsAutomaticColorButtonVisible = "Boolean"
  IsNoColorButtonVisible = "Boolean"
  ColorTemplate = "xs:string"
  ChipSize = "xs:string"/>
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
<td><strong>ChipSize</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Dimensioni di ogni chip di colore o campione. <br/> Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> Piccolo<br/> </dt> <dd> Ogni chip di colore è un quadrato di pixel 11x11. <br/> </dd> <dt><span></span><span></span><strong></strong> Media<br/> </dt> <dd> Ogni chip di colore è un quadrato di pixel 16x16. <br/> </dd> <dt><span></span><span></span><strong></strong> Grandi dimensioni<br/> </dt> <dd> Ogni chip di colore è un quadrato di pixel 24x24. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ColorTemplate</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Modelli di layout che specificano il tipo di <a href="windowsribbon-controls-dropdowncolorpicker.md">selezione colori a discesa</a>. <br/> Limitato a uno dei valori seguenti (se non sono dichiarati attributi facoltativi relativi a un <em>ColorTemplate</em> , viene visualizzata la visualizzazione predefinita):<br/> <br/>
<dt><span></span><span></span><strong></strong> ThemeColors<br/> </dt> <dd> Valore predefinito. <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> Impostando l'attributo <em>ColorTemplate</em> su <code>ThemeColors</code> sono abilitate le funzionalità seguenti:<br/>
<ul>
<li>Ancoraggio SplitButton.</li>
<li>Il pulsante colore <strong>automatico</strong> viene visualizzato per impostazione predefinita.</li>
<li>Griglia campione <strong>colori del tema</strong> di Windows.</li>
<li>Griglia campioni <strong>colori standard</strong> .</li>
<li>La griglia di campioni <strong>colori recenti</strong> è facoltativa.</li>
<li>Pulsante di avvio finestra di dialogo <strong>altri colori</strong> .</li>
<li>Per impostazione predefinita, non viene visualizzato alcun pulsante colore <strong>colore</strong> .</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (StandardColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> Impostando l'attributo <em>ColorTemplate</em> su <code>StandardColors</code> sono abilitate le funzionalità seguenti:<br/>
<ul>
<li>Ancoraggio SplitButton.</li>
<li>Il pulsante colore <strong>automatico</strong> viene visualizzato per impostazione predefinita.</li>
<li>Griglia campioni <strong>colori standard</strong> .</li>
<li>Pulsante di avvio finestra di dialogo <strong>altri colori</strong> .</li>
<li>Per impostazione predefinita, non viene visualizzato alcun pulsante colore <strong>colore</strong> .</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (HighlightColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> Impostando l'attributo <em>ColorTemplate</em> su <code>HighlightColors</code> sono abilitate le funzionalità seguenti:<br/>
<ul>
<li>Ancoraggio SplitButton.</li>
<li>Griglia campioni <strong>colori standard</strong> senza intestazione.</li>
<li>Per impostazione predefinita, non viene visualizzato alcun pulsante colore <strong>colore</strong> .</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Colonne</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Numero di colonne del chip di colore (o campione).<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>XS: positiveInteger o xs: String<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsAutomaticColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Consente di visualizzare o nascondere il pulsante colore <strong>automatico</strong> . <br/> Valido solo quando <code>StandardColors</code> <code>ThemeColors</code> viene specificato o per l'attributo <em>ColorTemplate</em> . <br/> Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> false<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsNoColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Consente di visualizzare o nascondere il pulsante <strong>nessun colore</strong> . <br/> Valido per tutti i valori <em>ColorTemplate</em> .<br/> Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> false<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>RecentColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Numero di righe del chip di colore (o campione) nell'area dei <strong>colori recenti</strong> . <br/> Valido solo quando <code>ThemeColors</code> viene specificato per l'attributo <em>ColorTemplate</em> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>StandardColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Numero di righe del chip di colore (o campione) nell'area dei <strong>colori standard</strong> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ThemeColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Numero di righe del chip di colore (o campione) nell'area dei <strong>colori del tema</strong> .<br/> Valido solo quando <code>ThemeColors</code> viene specificato per l'attributo <em>ColorTemplate</em> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/>             |
| [**DropDownButton**](windowsribbon-element-dropdownbutton.md)<br/>         |
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/>       |
| [**Group**](windowsribbon-element-group.md)<br/>                           |
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può essere presente una o più volte per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per tutti e tre i tipi di [selezione colori a discesa](windowsribbon-controls-dropdowncolorpicker.md).

In questa sezione del codice vengono illustrate le dichiarazioni di comando per tre elementi **DropDownColorPicker** .


```XML
<!-- DropDownColorPickers -->
<Command Name="cmdDropDownColorPickerGroup"
         Symbol="cmdDropDownColorPickerGroup"
         Comment="DropDownColorPicker Group"
         Id="55000"/>
<Command Name="cmdDropDownColorPickerThemeColors"
         Symbol="cmdDropDownColorPickerThemeColors"
         Comment="DropDownColorPicker ThemeColors"
         Id="55010"
         LabelTitle="ThemeColors"
         LabelDescription="ThemeColors\ndescription."/>
<Command Name="cmdDropDownColorPickerStandardColors"
         Symbol="cmdDropDownColorPickerStandardColors"
         Comment="DropDownColorPicker StandardColors"
         Id="55011"
         LabelTitle="StandardColors"/>
<Command Name="cmdDropDownColorPickerHighlightColors"
         Symbol="cmdDropDownColorPickerHighlightColors"
         Comment="DropDownColorPicker HighlightColors"
         Id="55012"
         LabelTitle="HighlightColors"/>
```



Questa sezione di codice mostra i tre tipi di dichiarazioni di controllo **DropDownColorPicker** .


```XML
<Group CommandName="cmdDropDownColorPickerGroup"
       SizeDefinition="ThreeButtons">
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerThemeColors"
    ColorTemplate="ThemeColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerStandardColors"
    ColorTemplate="StandardColors"/>
  <DropDownColorPicker
    CommandName="cmdDropDownColorPickerHighlightColors"
    ColorTemplate="HighlightColors"
    StandardColorGridRows="1"/>
</Group>
```



## <a name="element-information"></a>Informazioni sull'elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | Sì       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo selezione colori a discesa](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[Esempio DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





