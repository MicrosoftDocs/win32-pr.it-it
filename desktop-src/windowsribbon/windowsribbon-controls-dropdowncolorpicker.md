---
title: Selezione colori Drop-Down
description: Il Framework della barra multifunzione di Windows fornisce un controllo di selezione colori Drop-Down specializzato che espone diverse impostazioni dei colori tramite un pulsante di suddivisione e un selettore di colori personalizzabile.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552cd05e619ba71653d0d72e8457f5d4c8c39624
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104399825"
---
# <a name="drop-down-color-picker"></a>Selezione colori Drop-Down

Il Framework della barra multifunzione di Windows fornisce un controllo di selezione colori Drop-Down specializzato che espone diverse impostazioni dei colori tramite un pulsante di suddivisione e un selettore di colori personalizzabile.

-   [Introduzione](#introduction)
-   [markup](#markup)
-   [Codice](#code)
    -   [Proprietà](#properties)
    -   [Gestori di comandi](#command-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Emulando l'aspetto e la funzionalità della selezione colori Microsoft Office, il Framework della barra multifunzione è in grado di trarre vantaggio da e contribuire a coerenza e familiarità in un'ampia gamma di applicazioni.

## <a name="markup"></a>markup

Come tutti i controlli della barra multifunzione, il Drop-Down selezione colori viene facilmente implementato e personalizzato tramite markup. Il Framework fornisce un numero di attributi degli elementi per la selezione colori Drop-Down per esporre diversi livelli di funzionalità. Nella tabella seguente sono elencati gli attributi di selezione colori Drop-Down.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ColorTemplate</td>
<td>Modelli di layout che specificano il tipo di selezione colori Drop-Down.<br/> Sono disponibili tre modelli, ognuno dei quali specifica un layout di controllo e i valori predefiniti per gli attributi e le chiavi di proprietà associati. <br/>
<ul>
<li><code>ThemeColors</code></li>
<li><code>StandardColors</code></li>
<li><code>HighlightColors</code></li>
</ul></td>
</tr>
<tr class="even">
<td>ChipSize</td>
<td>Dimensioni di ogni chip di colore (o campione).<br/>
<ul>
<li><code>Small</code></li>
<li><code>Medium</code></li>
<li><code>Large</code></li>
</ul></td>
</tr>
<tr class="odd">
<td>Colonne</td>
<td>Numero di colonne del chip di colore (o campione).<br/></td>
</tr>
<tr class="even">
<td>CommandName</td>
<td>Nome della dichiarazione del comando associato. <br/></td>
</tr>
<tr class="odd">
<td>IsAutomaticColorButtonVisible</td>
<td>Consente di visualizzare o nascondere il pulsante <strong>automatico</strong> .<br/> Valido solo quando <em>ColorTemplate</em> ha il valore <code>ThemeColors</code> o <code>StandardColors</code> .<br/></td>
</tr>
<tr class="even">
<td>IsNoColorButtonVisible</td>
<td>Consente di visualizzare o nascondere il pulsante <strong>nessun colore</strong> .<br/> Valido per tutti i valori <em>ColorTemplate</em> .<br/></td>
</tr>
<tr class="odd">
<td>RecentColorGridRows</td>
<td>Numero di righe del chip di colore (o campione) nell'area dei <strong>colori recenti</strong> .<br/> Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> .<br/></td>
</tr>
<tr class="even">
<td>StandardColorGridRows</td>
<td>Numero di righe del chip di colore (o campione) nell'area dei <strong>colori standard</strong> .<br/></td>
</tr>
<tr class="odd">
<td>ThemeColorGridRows</td>
<td>Numero di righe del chip di colore (o campione) nell'area dei <strong>colori del tema</strong> .<br/> Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> .<br/></td>
</tr>
</tbody>
</table>



 

Le schermate seguenti illustrano i layout di selezione colori predefiniti Drop-Down per i tre modelli di colore.



|                                                                                                                                                                                               |                                                                                                                                                                                                       |                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ThemeColors`: \[ \] ![ screenshot di nuova riga dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su' ThemeColors '. ](images/markup/colortemplate.themedcolors.1.png) \[ NewLine\] | `standardcolors`: \[ \] ![ screenshot di nuova riga dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su' standardcolors '. ](images/markup/colortemplate.standardcolors.3.png) \[ NewLine\] | `highlightcolors`: \[ \] ![ screenshot di nuova riga dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su' highlightcolors '.](images/markup/colortemplate.highlightcolors.2.png)<br/> |



 

Il markup di base necessario per ogni tipo di selezione dei colori Drop-Down è illustrato negli esempi seguenti:

> [!Note]  
> La selezione colori Drop-Down è un controllo [Button](windowsribbon-controls-button.md) valido in un modello [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .

 


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


```XML

<Group CommandName=&quot;cmdDropDownColorPickerGroup&quot;
       SizeDefinition=&quot;ThreeButtons&quot;>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerThemeColors&quot;
    ColorTemplate=&quot;ThemeColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerStandardColors&quot;
    ColorTemplate=&quot;StandardColors&quot;/>
  <DropDownColorPicker
    CommandName=&quot;cmdDropDownColorPickerHighlightColors&quot;
    ColorTemplate=&quot;HighlightColors&quot;
    StandardColorGridRows=&quot;1&quot;/>
</Group>
```





## <a name="code"></a>Codice

Come controllo specializzato che supporta la personalizzazione, qualsiasi implementazione della selezione colori Drop-Down che sfrutta tali funzionalità richiede un codice dell'applicazione specializzato per gestire le proprietà e gestire qualsiasi comando emesso dal controllo.

### <a name="properties"></a>Proprietà

Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo Drop-Down selezione colori.

In genere, una proprietà della selezione colori Drop-Down viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework. Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo Drop-Down selezione colori.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Chiave della proprietà</th>
<th>Descrizione</th>
<th>Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></td>
<td>Definisce l'etichetta per il pulsante colore <strong>automatico</strong> .<br/> Valido solo quando <em>ColorTemplate</em> ha il valore <code>ThemeColors</code> o <code>StandardColors</code> .<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></td>
<td>Definisce il valore di colore selezionato come <a href="/windows/win32/gdi/colorref">COLORREF</a>.<br/> Valido solo quando <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> ha un valore <code>UI_SWATCHCOLORTYPE_RGB</code> .<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></td>
<td>Definisce il tipo di colore selezionato.<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Definisce la possibilità per un controllo di rispondere all'interazione dell'utente.<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>

<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Definisce la stringa di caratteri per un'etichetta del controllo.<br/></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Definisce l'immagine a contrasto elevato grande da visualizzare per un controllo.<br/></td>
<td>Può essere aggiornato solo tramite l'invalidamento.<br/> Per ulteriori informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">specifica delle risorse dell'immagine della barra multifunzione</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Definisce l'immagine di grandi dimensioni da visualizzare per un controllo.<br/></td>
<td>Può essere aggiornato solo tramite l'invalidamento.<br/> Per ulteriori informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">specifica delle risorse dell'immagine della barra multifunzione</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></td>
<td>Definisce l'etichetta per il pulsante <strong>altri colori...</strong> .<br/> Valido solo quando <em>ColorTemplate</em> ha il valore <code>ThemeColors</code> o <code>StandardColors</code> .<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></td>
<td>Definisce l'etichetta per il pulsante <strong>nessun colore</strong> .<br/> Valido per tutti i valori <em>ColorTemplate</em> .<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></td>
<td>Definisce l'etichetta per la categoria dei <strong>colori recenti</strong> .<br/> Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> . Si tratta dell'unico modello che contiene le categorie con etichetta.<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Definisce la piccola immagine a contrasto elevato da visualizzare per un controllo.<br/></td>
<td>Può essere aggiornato solo tramite l'invalidamento.<br/> Per ulteriori informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">specifica delle risorse dell'immagine della barra multifunzione</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Definisce l'immagine piccola da visualizzare per un controllo.<br/></td>
<td>Può essere aggiornato solo tramite l'invalidamento.<br/> Per ulteriori informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">specifica delle risorse dell'immagine della barra multifunzione</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></td>
<td>Definisce una matrice di valori <a href="/windows/win32/gdi/colorref">COLORREF</a> per i campioni di una selezione colori Drop-Down.<br/> Ogni <em>ColorTemplate</em> di selezione colori Drop-Down contiene una <code>StandardColors</code> griglia. <br/>
<blockquote>
[!Note]<br />
Vengono visualizzati i valori <a href="/windows/win32/gdi/colorref">COLORREF</a> delle <em>colonne</em> <em>StandardColorGridRows</em> x iniziali della matrice. Se la matrice definisce un numero inferiore di colori rispetto al numero di <code>StandardColors</code> campioni dichiarati nel markup, vengono visualizzati spazi vuoti per i chip mancanti.
</blockquote>
<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></td>
<td>Definisce l'etichetta per la categoria dei <strong>colori standard</strong> .<br/> Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> . Si tratta dell'unico modello che contiene le categorie con etichetta.<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></td>
<td>Definisce una matrice di stringhe di descrizioni comandi dei campioni di colore per la <code>StandardColors</code> griglia.<br/> Ogni <em>ColorTemplate</em> di selezione colori Drop-Down contiene una <code>StandardColors</code> griglia. <br/>
<blockquote>
[!Note]<br />
Vengono utilizzate solo le descrizioni comandi necessarie per etichettare i campioni di colore visualizzati nella <code>StandardColors</code> griglia. Se viene fornito un minor numero di etichette rispetto al numero di campioni nella <code>StandardColors</code> griglia, viene fornito un valore predefinito per i campioni remainining.
</blockquote>
<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></td>
<td>Definisce una matrice di valori <a href="/windows/win32/gdi/colorref">COLORREF</a> per i campioni di una selezione colori Drop-Down.<br/> Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Vengono visualizzati i valori <a href="/windows/win32/gdi/colorref">COLORREF</a> delle <em>colonne</em> <em>ThemeColorGridRows</em> x iniziali della matrice. Se la matrice definisce un numero inferiore di colori rispetto al numero di <code>ThemeColors</code> campioni dichiarati nel markup, vengono visualizzati spazi vuoti per i chip mancanti.
</blockquote>
<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></td>
<td>Definisce la matrice di stringhe di descrizioni comandi dei campioni di colore per la <code>ThemeColors</code> griglia.<br/> Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Vengono utilizzate solo le descrizioni comandi necessarie per etichettare i campioni di colore visualizzati nella <code>ThemeColors</code> griglia. Se viene fornito un minor numero di etichette rispetto al numero di campioni nella <code>ThemeColors</code> griglia, viene fornito un valore predefinito per i campioni remainining.
</blockquote>
<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></td>
<td>Definisce l'etichetta per la categoria dei <strong>colori del tema</strong> .<br/> Valido solo quando il valore di <em>ColorTemplate</em> è <code>ThemeColors</code> . Si tratta dell'unico modello che contiene le categorie con etichetta.<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Definisce la stringa di caratteri per una descrizione della descrizione comando associata a un <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.<br/></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Definisce la stringa di caratteri per una descrizione comando.<br/></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a>Gestori di comandi

Il metodo [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) viene usato per personalizzare una selezione dei colori Drop-Down tramite le chiavi di proprietà elencate in precedenza. Nell'esempio seguente viene illustrato come impostare i campioni di colore di un selettore di colore Drop-Down, in base a una preferenza di stile personalizzata o a una griglia di campioni personalizzata dichiarata nel markup.


```C++
STDMETHODIMP DropDownColorPickerHandler::UpdateProperty(
              UINT nCmdID,
              __in REFPROPERTYKEY key,
              __in_opt const PROPVARIANT* ppropvarCurrentValue,
              __out PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_ThemeColors)
  {
    COLORREF rThemeColors[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeColors); i++)
    {
      // any COLORREF
      rThemeColors[i] = RGB(0, 255, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rThemeColors, ARRAYSIZE(rThemeColors), ppropvarNewValue);
  }

  else if (key == UI_PKEY_StandardColors)
  {
    ULONG rStandardColors[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rStandardColors); i++)
    {
      // any COLORREF
      rStandardColors[i] = RGB(255, 0, 0); 
    }
    hr = InitPropVariantFromUInt32Vector(
           &rStandardColors, ARRAYSIZE(rStandardColors),ppropvarNewValue);
  }

  else if (key == UI_PKEY_ThemeColorsTooltips)
  {
    BSTR rThemeTooltips[TOT_THEME_COLORS];
    for (LONG i = 0; i < ARRAYSIZE(rThemeTooltips); i++)
    {
      // any constant character string
      rThemeTooltips[i] = L"Green"; 
    }
    hr = InitPropVariantFromStringVector((PCWSTR *)&rThemeTooltips, 50, ppropvarNewValue);
  }
  else if (key == UI_PKEY_StandardColorsTooltips)
  {
    static BSTR rStandardTooltips[TOT_STANDARD_COLORS];
    for (LONG i = 0; i < ARRAYSize(rStandardTooltips); i++)
    {
      // any constant character string
      rStandardTooltips[i] = L"Red"; 
    }
    hr = InitPropVariantFromStringVector(
           (PCWSTR *)&rStandardTooltips, 20, ppropvarNewValue);
  }
  return hr;
}
```



Nell'esempio seguente viene illustrata un'implementazione del metodo [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) che espone i colori del campione di selezione colori Drop-Down all'applicazione Ribbon.


```C++
STDMETHODIMP DropDownColorPickerHandler::Execute(
                 UINT nCmdID,
                 UI_EXECUTIONVERB verb,
                 __in_opt const PROPERTYKEY* key,
                 __in_opt const PROPVARIANT* ppropvarValue,
                 __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  HRESULT hr = E_NOTIMPL;
  if (*key == UI_PKEY_ColorType)
  {
    UI_SWATCHCOLORTYPE uType = 
      (UI_SWATCHCOLORTYPE)PropVariantToUInt32WithDefault(
        *ppropvarValue, 
        UI_SWATCHCOLORTYPE_NOCOLOR);

    COLORREF color;
    switch(uType)
    {
      case UI_SWATCHCOLORTYPE_RGB:
        PROPVARIANT var;
        pCommandExecutionProperties->GetValue(UI_PKEY_Color, &var);
        color = PropVariantToUInt32WithDefault(var, 0);
        break;
      case UI_SWATCHCOLORTYPE_AUTOMATIC:
        color = COLOR_WINDOWTEXT;
        break;
      case UI_SWATCHCOLORTYPE_NOCOLOR:
        color = MSONoFill;
        break;
    }

    // do with your color what you will...
    gInternalColor = color;
    hr = S_OK;
  }
  return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[Proprietà selezione colori](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[Personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità](windowsribbon-templates.md)
</dt> <dt>

[Esempio DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

