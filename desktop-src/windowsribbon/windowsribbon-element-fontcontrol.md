---
title: Elemento FontControl
description: Rappresenta un controllo Tipo di carattere, un contenitore specializzato di singoli controlli dedicati alla manipolazione del tipo di carattere.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- Elemento FontControl Windows ribbon
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b6be1fae596e70f15dbfcd27e4bf15e35e04a93
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625977"
---
# <a name="fontcontrol-element"></a>Elemento FontControl

Rappresenta un [controllo Tipo di carattere](windowsribbon-controls-fontcontrol.md), che è un contenitore specializzato di singoli controlli dedicati alla manipolazione del tipo di carattere.

## <a name="usage"></a>Utilizzo

``` syntax
<FontControl
  CommandName = "xs:positiveInteger or xs:string"
  FontType = "xs:string"
  IsGrowShrinkButtonGroupVisible = "Boolean"
  IsStrikethroughButtonVisible = "Boolean"
  IsUnderlineButtonVisible = "Boolean"
  IsHighlightButtonVisible = "Boolean"
  ShowVerticalFonts = "Boolean"
  ShowTrueTypeOnly = "Boolean"
  MinimumFontSize = "xs:positiveInteger"
  MaximumFontSize = "xs:positiveInteger"/>
```

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
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
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>oggetto Command</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger o xs:string)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999, inclusivo o valore esadecimale compreso tra 0x2 e 0xea5f, inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Tipo di carattere</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti: <br/> <br/>
<dt><span></span><span></span><strong></strong> (FontOnly)<br/> </dt> <dd> Valore predefinito. <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> L'impostazione <em>dell'attributo FontType</em> <code>FontOnly</code> su abilita le funzionalità seguenti:<br/>
<ul>
<li><strong>Casella combinata della famiglia</strong> di caratteri.</li>
<li><strong>Casella combinata Dimensioni</strong> carattere.</li>
<li><p><strong>Pulsanti di</strong> <strong>attivazione/disattivazione</strong>grassetto, corsivo, <strong>sottolineatura e barrato.</strong> <strong></strong></p>
<blockquote>
[!Note]<br />
I pulsanti <strong></strong> <strong>di</strong> attivazione/disattivazione Barrato e Sottolineatura vengono visualizzati per impostazione predefinita, ma possono essere nascosti impostando gli attributi <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> su <code>false</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (FontWithColor)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> L'impostazione <em>dell'attributo FontType</em> <code>FontWithColor</code> su abilita le funzionalità seguenti:<br/>
<ul>
<li><strong>Casella combinata della famiglia</strong> di caratteri.</li>
<li><strong>Casella combinata Dimensioni</strong> carattere.</li>
<li><strong>Pulsanti Aumenta dimensioni carattere</strong> <strong>e Riduci dimensioni</strong> carattere incrementa e decrementa.</li>
<li><p><strong>Pulsanti di</strong> <strong>attivazione/disattivazione</strong>grassetto, corsivo, <strong>sottolineatura e barrato.</strong> <strong></strong></p>
<blockquote>
[!Note]<br />
I pulsanti <strong></strong> <strong>di</strong> attivazione/disattivazione Barrato e Sottolineatura vengono visualizzati per impostazione predefinita, ma possono essere nascosti impostando gli attributi <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> su <code>false</code> .
</blockquote>
<p><br/></p></li>
<li><strong>Selezione colori</strong> testo.</li>
<li><p><strong>Selezione colori evidenziazione</strong> testo.</p>
<blockquote>
[!Note]<br />
Questo controllo è nascosto per impostazione predefinita, ma può essere visualizzato impostando <em>l'attributo IsHighlightButtonVisible</em> su <code>true</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (RichFont)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> L'impostazione <em>dell'attributo FontType</em> <code>RichFont</code> su abilita le funzionalità seguenti:<br/>
<ul>
<li><strong>Casella combinata della famiglia</strong> di caratteri.</li>
<li><strong>Casella combinata Dimensioni</strong> carattere.</li>
<li><strong>Pulsanti Aumenta dimensioni carattere</strong> <strong>e Riduci dimensioni</strong> carattere incrementa e decrementa.</li>
<li><p><strong>Pulsanti di</strong> <strong>attivazione/disattivazione</strong>grassetto, corsivo, <strong>sottolineatura e barrato.</strong> <strong></strong></p>
<blockquote>
[!Note]<br />
I pulsanti <strong></strong> <strong>di</strong> attivazione/disattivazione barrato e sottolineatura vengono visualizzati per impostazione predefinita e non possono essere nascosti impostando gli attributi <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> su <code>false</code> .
</blockquote>
<p><br/></p></li>
<li><strong>Selezione colori</strong> testo.</li>
<li><p><strong>Selezione colori evidenziazione</strong> testo.</p>
<blockquote>
[!Note]<br />
Questo controllo viene visualizzato per impostazione predefinita e non può essere nascosto impostando <em>l'attributo IsHighlightButtonVisible</em> su <code>false</code> .
</blockquote>
<p><br/></p></li>
<li><strong>Pulsanti di attivazione/disattivazione</strong> <strong>pedice</strong> e apice.</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsGrowShrinkButtonGroupVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td><strong>Windows 8 e più recente</strong><br/> Limitato a uno dei valori seguenti: <br/>
<blockquote>
[!Note]<br />
I pulsanti Aumenta/Riduci non vengono mai visualizzati in <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Impostazione predefinita quando il valore di <em>FontType</em> è uguale <code>FontWithColor</code> a o <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Impostazione predefinita quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsHighlightButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi): <br/>
<blockquote>
[!Note]<br />
L'evidenziazione dei colori è disponibile solo da <strong>un oggetto FontControl</strong> quando il valore dell'attributo <em>FontType</em> è uguale <code>FontWithColor</code> a o <code>RichFont</code> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Impostazione predefinita quando il valore di <em>FontType</em> è uguale <code>FontWithColor</code> a o <code>RichFont</code> .<br/> Valido solo quando il valore di <em>FontType</em> è uguale <code>FontWithColor</code> a o <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Impostazione predefinita quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> .<br/> Valido solo quando il valore di <em>FontType</em> è uguale <code>FontOnly</code> a o <code>FontWithColor</code> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsStrikethroughButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi): <br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Valido solo quando il valore di <em>FontType</em> è uguale <code>FontOnly</code> a o <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsUnderlineButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi): <br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Valido solo quando il valore di <em>FontType</em> è uguale <code>FontOnly</code> a o <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaximumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Dimensione massima in punti da visualizzare.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Valore intero compreso tra 1 e 9999, inclusi.<br/> Il valore predefinito <strong>è 9999.</strong><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinimumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Dimensione minima in punti da visualizzare.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Valore intero compreso tra 1 e 9999 inclusi.<br/> Il valore predefinito <strong>è 1</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ShowTrueTypeOnly</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Visualizza solo i tipi di carattere TrueType e OpenType. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Valore predefinito. Non viene impostata alcuna restrizione sul tipo di carattere visualizzato.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ShowVerticalFonts</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/>
<blockquote>
[!Note]<br />
I tipi di carattere verticali sono preceduti da un simbolo @ <strong>nell'elenco Famiglia di</strong> caratteri.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Valore predefinito. Visualizza i tipi di carattere verticali impostati su <strong>Mostra nel</strong> pannello di <strong>controllo Tipi</strong> di carattere. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Consente a un'applicazione che non supporta il testo verticale di nascondere i tipi di carattere verticali impostati su <strong>Mostra</strong> nel pannello <strong>di controllo Tipi di</strong> carattere.<br/>
<blockquote>
[!Note]<br />
In Windows Vista il pannello di controllo <strong>Tipi</strong> di carattere non offre <strong>la funzionalità</strong> Mostra <strong>o</strong> Nascondi. In questo caso, <em>l'attributo ShowVerticalFonts</em> deve essere impostato su <code>False</code> .
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementi figlio

Non ci sono elementi figlio.

## <a name="parent-elements"></a>Elementi padre



| Elemento                                                               |
|-----------------------------------------------------------------------|
| [**ControlGroup**](windowsribbon-element-controlgroup.md)<br/> |
| [**Group**](windowsribbon-element-group.md)<br/>               |
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per [**ogni elemento ControlGroup,**](windowsribbon-element-controlgroup.md) [**Group**](windowsribbon-element-group.md) [**o MenuGroup.**](windowsribbon-element-menugroup.md)

Tutti gli attributi del comando **FontControl** dichiarati nel markup, ad esempio [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) o [**Command.TooltipTitle,**](windowsribbon-element-command-tooltiptitle.md)vengono sottoposti a override dagli attributi dei singoli controlli che comprendono **FontControl.**

Qualsiasi tentativo di selezionare un campione di colore [](windowsribbon-controls-fontcontrol.md) dalla selezione colori di un controllo Tipo di carattere può comportare una violazione di accesso se al controllo non è associato alcun gestore comando.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per i tre tipi di [controllo del tipo di carattere](windowsribbon-controls-fontcontrol.md).

Questa sezione di codice illustra le dichiarazioni **del comando FontControl,** ognuna con una dichiarazione [**del contenitore**](windowsribbon-element-group.md) Group.


```XML
<!-- A FontOnly FontControl -->
<Command Name="cmdFontOnlyGroup"
         Symbol="cmdFontOnlyGroup"
         Comment="FontOnlyGroup"
         Id="50001"
         LabelTitle="FontOnly"/>
<Command Name="cmdFontOnly"
         Symbol="cmdFontOnly"
         Comment="FontOnly"
         Id="50010"/>

<!-- A FontWithColor FontControl -->
<Command Name="cmdFontWithColorGroup"
         Symbol="cmdFontWithColorGroup"
         Comment="FontWithColorGroup"
         Id="50002"
         LabelTitle="FontWithColor"/>
<Command Name="cmdFontWithColor"
         Symbol="cmdFontWithColor"
         Comment="FontWithColor"
         Id="50020"/>

<!-- A RichFont FontControl -->
<Command Name="cmdRichFontGroup"
         Symbol="cmdRichFontGroup"
         Comment="RichFontGroup"
         Id="50003"
         LabelTitle="RichFont"
         Keytip="ZF"/>
<Command Name="cmdRichFont"
         Symbol="cmdRichFont"
         Comment="RichFont"
         Id="50030"
         Keytip="RF"
         LabelTitle="test"
         TooltipTitle="test"/>
```



Questa sezione di codice illustra le **dichiarazioni del controllo FontControl** in cui ogni **fontControl** e [**gruppo**](windowsribbon-element-group.md) viene dichiarato in un'unica scheda.


```XML
<Tab CommandName="cmdTab1">
  <Group CommandName="cmdFontOnlyGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontOnly"
                 FontType="FontOnly"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdFontWithColorGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontWithColor"
                 FontType="FontWithColor"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 IsHighlightButtonVisible="true"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdRichFontGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdRichFont"
                 FontType="RichFont"
                 IsHighlightButtonVisible="true"
                 IsUnderlineButtonVisible="true"
                 IsStrikethroughButtonVisible="true"
                 ShowVerticalFonts="true"
                 MinimumFontSize="15"/>
  </Group>
```



## <a name="element-information"></a>Informazioni sull'elemento

* **Sistema minimo supportato:** Windows 7
* **Può essere vuoto:** Sì



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo Font](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Proprietà del controllo Font](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Esempio di FontControl](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





