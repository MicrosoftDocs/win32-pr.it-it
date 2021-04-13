---
title: Elemento FontControl
description: Rappresenta un controllo del tipo di carattere, ovvero un contenitore specializzato di singoli controlli dedicati alla manipolazione dei tipi di carattere.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- Barra multifunzione Windows elemento FontControl
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fa080b58e3a9d53fa044e7dbbb6598d5b7be7c49
ms.sourcegitcommit: 2387bc0339a1764564c1509e72ed5f2e8ae60b36
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/30/2020
ms.locfileid: "104398823"
---
# <a name="fontcontrol-element"></a>Elemento FontControl

Rappresenta un [controllo del tipo di carattere](windowsribbon-controls-fontcontrol.md), ovvero un contenitore specializzato di singoli controlli dedicati alla manipolazione dei tipi di carattere.

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
<td>XS: positiveInteger o xs: String<br/></td>
<td>No<br/></td>
<td>Associa l'elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o xs: String)<br/> </dt> <dd> Stringa, valore intero compreso tra 2 e 59999, inclusivo o un valore esadecimale compreso tra 0x2 e 0xea5f, inclusi. <br/> Il valore deve essere univoco all'interno del documento XML della barra multifunzione. <br/> Lunghezza massima: 100 caratteri. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>FontType</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti: <br/> <br/>
<dt><span></span><span></span><strong></strong> (FontOnly)<br/> </dt> <dd> Valore predefinito. <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> Impostando l'attributo <em>FontType</em> su <code>FontOnly</code> sono abilitate le funzionalità seguenti:<br/>
<ul>
<li>Casella combinata della <strong>famiglia di caratteri</strong> .</li>
<li>Casella combinata <strong>dimensioni carattere</strong> .</li>
<li><p>Pulsanti di attivazione con <strong>grassetto</strong>, <strong>corsivo</strong>, <strong>sottolineatura</strong>e <strong>barrato</strong> .</p>
<blockquote>
[!Note]<br />
I pulsanti per l'interruttore <strong>barrato</strong> e <strong>sottolineatura</strong> vengono visualizzati per impostazione predefinita, ma possono essere nascosti impostando gli attributi <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> su <code>false</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (FontWithColor)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> Impostando l'attributo <em>FontType</em> su <code>FontWithColor</code> sono abilitate le funzionalità seguenti:<br/>
<ul>
<li>Casella combinata della <strong>famiglia di caratteri</strong> .</li>
<li>Casella combinata <strong>dimensioni carattere</strong> .</li>
<li><strong>Aumentare</strong> le dimensioni del carattere e <strong>ridurre</strong> i pulsanti di incremento e decremento del tipo di carattere.</li>
<li><p>Pulsanti di attivazione con <strong>grassetto</strong>, <strong>corsivo</strong>, <strong>sottolineatura</strong>e <strong>barrato</strong> .</p>
<blockquote>
[!Note]<br />
I pulsanti per l'interruttore <strong>barrato</strong> e <strong>sottolineatura</strong> vengono visualizzati per impostazione predefinita, ma possono essere nascosti impostando gli attributi <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> su <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Selezione colori <strong>colore testo</strong> .</li>
<li><p>Selezione colore colore <strong>evidenziazione testo</strong> .</p>
<blockquote>
[!Note]<br />
Questo controllo è nascosto per impostazione predefinita, ma può essere visualizzato impostando l'attributo <em>IsHighlightButtonVisible</em> su <code>true</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (RichFont)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> Impostando l'attributo <em>FontType</em> su <code>RichFont</code> sono abilitate le funzionalità seguenti:<br/>
<ul>
<li>Casella combinata della <strong>famiglia di caratteri</strong> .</li>
<li>Casella combinata <strong>dimensioni carattere</strong> .</li>
<li><strong>Aumentare</strong> le dimensioni del carattere e <strong>ridurre</strong> i pulsanti di incremento e decremento del tipo di carattere.</li>
<li><p>Pulsanti di attivazione con <strong>grassetto</strong>, <strong>corsivo</strong>, <strong>sottolineatura</strong>e <strong>barrato</strong> .</p>
<blockquote>
[!Note]<br />
I pulsanti per l'interruttore <strong>barrato</strong> e <strong>sottolineatura</strong> vengono visualizzati per impostazione predefinita e non possono essere nascosti impostando gli attributi <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> su <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Selezione colori <strong>colore testo</strong> .</li>
<li><p>Selezione colore colore <strong>evidenziazione testo</strong> .</p>
<blockquote>
[!Note]<br />
Questo controllo viene visualizzato per impostazione predefinita e non può essere nascosto impostando l'attributo <em>IsHighlightButtonVisible</em> su <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Pulsanti <strong>per l'attivazione di pedice</strong> <strong>e pedice</strong> .</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsGrowShrinkButtonGroupVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td><strong>Windows 8 e versioni successive</strong><br/> Limitato a uno dei valori seguenti: <br/>
<blockquote>
[!Note]<br />
I pulsanti di espansione/compattazione non vengono mai visualizzati in <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd> Impostazione predefinita quando il valore di <em>FontType</em> è uguale a <code>FontWithColor</code> o <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> false<br/> </dt> <dd> Impostazione predefinita quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsHighlightButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi): <br/>
<blockquote>
[!Note]<br />
L'evidenziazione dei colori è disponibile solo da un <strong>FontControl</strong> quando il valore dell'attributo <em>FontType</em> è uguale a <code>FontWithColor</code> o <code>RichFont</code> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd> Impostazione predefinita quando il valore di <em>FontType</em> è uguale a <code>FontWithColor</code> o <code>RichFont</code> .<br/> Valido solo quando il valore di <em>FontType</em> è uguale a <code>FontWithColor</code> o <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> false<br/> </dt> <dd> Impostazione predefinita quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> .<br/> Valido solo quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> o <code>FontWithColor</code> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsStrikethroughButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi): <br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> false<br/> </dt> <dd> Valido solo quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> o <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsUnderlineButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi): <br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd> Valore predefinito. <br/> </dd> <dt><span></span><span></span><strong></strong> false<br/> </dt> <dd> Valido solo quando il valore di <em>FontType</em> è uguale a <code>FontOnly</code> o <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaximumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Dimensioni massime del punto da visualizzare.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Valore intero compreso tra 1 e 9999 inclusi.<br/> Il valore predefinito è <strong>9999</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinimumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td>Dimensioni minime del punto da visualizzare.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger)<br/> </dt> <dd> Valore intero compreso tra 1 e 9999 inclusi.<br/> Il valore predefinito è <strong>1</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ShowTrueTypeOnly</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd> Consente di visualizzare solo i tipi di carattere TrueType e OpenType. <br/> </dd> <dt><span></span><span></span><strong></strong> false<br/> </dt> <dd> Valore predefinito. Nessuna restrizione viene posizionata sul tipo di carattere visualizzato.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ShowVerticalFonts</strong><br/></td>
<td>Boolean<br/></td>
<td>No<br/></td>
<td>Limitato a uno dei valori seguenti (0 e 1 non sono validi):<br/>
<blockquote>
[!Note]<br />
I tipi di carattere verticali sono preceduti da un simbolo @ nell'elenco della <strong>famiglia di caratteri</strong> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd> Valore predefinito. Consente di visualizzare i tipi di carattere verticali impostati per la <strong>visualizzazione</strong> nel pannello di controllo dei <strong>tipi di carattere</strong> . <br/> </dd> <dt><span></span><span></span><strong></strong> false<br/> </dt> <dd> Consente a un'applicazione che non supporta il testo verticale di nascondere i tipi di carattere verticali impostati per la <strong>visualizzazione</strong> nel pannello di controllo dei <strong>tipi di carattere</strong> .<br/>
<blockquote>
[!Note]<br />
In Windows Vista, il pannello di controllo dei <strong>tipi di carattere</strong> non offre funzionalità <strong>Mostra</strong> o <strong>Nascondi</strong> . In questo caso, l'attributo <em>ShowVerticalFonts</em> deve essere impostato su <code>False</code> .
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
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a>Commenti

facoltativo.

Può verificarsi al massimo una volta per ogni elemento [**ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md)o [**MenuGroup**](windowsribbon-element-menugroup.md) .

Tutti gli attributi del comando **FontControl** dichiarati nel markup, ad esempio [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) o [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), vengono sottoposti a override dagli attributi dei singoli controlli che comprendono **FontControl**.

Qualsiasi tentativo di selezionare un campione di colore dalla selezione colori di un [controllo del tipo di carattere](windowsribbon-controls-fontcontrol.md) può causare una violazione di accesso se al controllo non è associato alcun gestore di comando.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il markup di base per i tre tipi di [controllo del tipo di carattere](windowsribbon-controls-fontcontrol.md).

In questa sezione del codice vengono illustrate le dichiarazioni di comando **FontControl** , ognuna con una dichiarazione del contenitore di [**gruppo**](windowsribbon-element-group.md) .


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



Questa sezione di codice mostra le dichiarazioni di controllo **FontControl** in cui ogni **FontControl** e [**gruppo**](windowsribbon-element-group.md) viene dichiarato in una singola scheda.


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



|                                     |           |
|-------------------------------------|-----------|
| Sistema minimo supportato<br/> | Windows 7 |
| Può essere vuoto                        | Sì       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo del tipo di carattere](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Esempio FontControl](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





