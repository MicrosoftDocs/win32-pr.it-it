---
title: Elemento DropDownColorPicker
description: Rappresenta un Drop-Down controllo Selezione colori che quando si fa clic visualizza una tavolozza di campioni di colore.
ms.assetid: fc4df978-9c52-43d5-8a5e-e015aa7058cd
keywords:
- Barra multifunzione di Windows per l'elemento DropDownColorPicker
topic_type:
- apiref
api_name:
- DropDownColorPicker
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce2fd1d9ff12b56d87955304fad24af23209ff91
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442902"
---
# <a name="dropdowncolorpicker-element"></a>Elemento DropDownColorPicker

Rappresenta un [controllo elenco a Selezione colori](windowsribbon-controls-dropdowncolorpicker.md)che quando si fa clic visualizza una tavolozza di campioni di colore.

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
<td>Dimensioni di ogni chip o campione di colore. <br/> Limitato a uno dei valori seguenti:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Piccola)<br/> </dt> <dd> Ogni chip di colore è un quadrato di 11 x 11 pixel. <br/> </dd> <dt><span></span><span></span><strong></strong> (Media)<br/> </dt> <dd> Ogni chip di colore è un quadrato di 16 x 16 pixel. <br/> </dd> <dt><span></span><span></span><strong></strong> (Grande)<br/> </dt> <dd> Ogni chip di colore è un quadrato di 24 x 24 pixel. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ColorTemplate</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Modelli di layout che specificano il tipo <a href="windowsribbon-controls-dropdowncolorpicker.md">di elenco a discesa Selezione colori</a>. <br/> Limitato a uno dei valori seguenti (se non viene dichiarato alcun attributo facoltativo correlato a <em>un oggetto ColorTemplate,</em> viene visualizzata la visualizzazione predefinita):<br/> <br/>
<dt><span></span><span></span><strong></strong> (ThemeColors)<br/> </dt> <dd> Valore predefinito. <br/> <img src="images/markup/colortemplate.themedcolors.1.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;ThemeColors&#39;." /><br/> L'impostazione <em>dell'attributo ColorTemplate</em> <code>ThemeColors</code> su abilita le funzionalità seguenti:<br/>
<ul>
<li>Ancoraggio SplitButton.</li>
<li><strong>Il pulsante</strong> a colori automatico viene visualizzato per impostazione predefinita.</li>
<li>Griglia <strong>dei campioni dei colori</strong> del tema di Windows.</li>
<li><strong>Griglia dei campioni</strong> di colori standard.</li>
<li><strong>La griglia dei</strong> campioni colori recenti è facoltativa.</li>
<li><strong>Icona di avvio della finestra</strong> di dialogo Altri colori.</li>
<li><strong>Per impostazione predefinita,</strong> non viene visualizzato alcun pulsante colore.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (StandardColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.standardcolors.3.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;StandardColors&#39;." /><br/> L'impostazione <em>dell'attributo ColorTemplate</em> <code>StandardColors</code> su abilita le funzionalità seguenti:<br/>
<ul>
<li>Ancoraggio SplitButton.</li>
<li><strong>Il pulsante</strong> a colori automatico viene visualizzato per impostazione predefinita.</li>
<li><strong>Griglia dei campioni</strong> di colori standard.</li>
<li><strong>Icona di avvio della finestra</strong> di dialogo Altri colori.</li>
<li><strong>Per impostazione predefinita,</strong> non viene visualizzato alcun pulsante colore.</li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (HighlightColors)<br/> </dt> <dd> <img src="images/markup/colortemplate.highlightcolors.2.png" alt="Screen shot of the DropDownColorPicker element with the ColorTemplate attribute set to &#39;HighlightColors&#39;." /><br/> L'impostazione <em>dell'attributo ColorTemplate</em> <code>HighlightColors</code> su abilita le funzionalità seguenti:<br/>
<ul>
<li>Ancoraggio SplitButton.</li>
<li><strong>Griglia di campioni</strong> di colori standard senza intestazione.</li>
<li><strong>Per impostazione predefinita,</strong> non viene visualizzato alcun pulsante colore.</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Colonne</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Numero di colonne di chip di colore (o campione).<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger o xs:string<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999, inclusivo o valore esadecimale compreso tra 0x2 e 0xea5f, inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsAutomaticColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Visualizza (o nasconde) il <strong>pulsante Colore</strong> automatico. <br/> Valido solo quando <code>StandardColors</code> o viene specificato per <code>ThemeColors</code> <em>l'attributo ColorTemplate.</em> <br/> Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsNoColorButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Visualizza (o nasconde) il <strong>pulsante Nessun</strong> colore. <br/> Valido per tutti <em>i valori ColorTemplate.</em><br/> Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>RecentColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Numero di righe di chip di colore (o campione) nell'area <strong>Colori</strong> recenti. <br/> Valido solo quando <code>ThemeColors</code> viene specificato per <em>l'attributo ColorTemplate.</em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>StandardColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Numero di righe di chip di colore (o campione) nell'area <strong>Colori</strong> standard.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ThemeColorGridRows</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Numero di righe di chip di colore (o campione) nell'area <strong>Colori tema.</strong><br/> Valido solo quando <code>ThemeColors</code> viene specificato per <em>l'attributo ColorTemplate.</em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Qualsiasi valore intero positivo compreso tra 1 e 256 inclusi.<br/> </dd> </dl></td>
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
| [**Gruppo**](windowsribbon-element-group.md)<br/>                           |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>                   |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>               |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi una o più volte per ogni elemento [**ControlGroup,**](windowsribbon-element-controlgroup.md) [**DropDownButton,**](windowsribbon-element-dropdownbutton.md) [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**Group,**](windowsribbon-element-group.md) [**MenuGroup,**](windowsribbon-element-menugroup.md) [**SplitButton**](windowsribbon-element-splitbutton.md)o [**SplitButtonGallery.**](windowsribbon-element-splitbuttongallery.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per tutti e tre i tipi di elenco a [discesa Selezione colori](windowsribbon-controls-dropdowncolorpicker.md).

Questa sezione di codice illustra le dichiarazioni Command per tre **elementi DropDownColorPicker.**


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



Questa sezione di codice illustra i tre tipi di dichiarazioni di controllo **DropDownColorPicker.**


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

* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** Sì



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco a discesa Selezione colori controllo](windowsribbon-controls-dropdowncolorpicker.md)
</dt> <dt>

[Esempio di DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

 

 





