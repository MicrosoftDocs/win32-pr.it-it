---
title: Drop-Down Selezione colori
description: Il framework della barra multifunzione di Windows fornisce un controllo Drop-Down Selezione colori controllo che espone un'ampia gamma di impostazioni di colore tramite un pulsante di menu suddiviso e un selettore di colore a discesa personalizzabile.
ms.assetid: 65e1fc23-7ac0-4bb3-9359-28ce88acf356
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366cc7eadaca23271d5b2afa43ec66235839694a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443662"
---
# <a name="drop-down-color-picker"></a>Drop-Down Selezione colori

Il framework della barra multifunzione di Windows fornisce un controllo Drop-Down Selezione colori controllo che espone un'ampia gamma di impostazioni di colore tramite un pulsante di menu suddiviso e un selettore di colore a discesa personalizzabile.

-   [Introduzione](#introduction)
-   [markup](#markup)
-   [Codice](#code)
    -   [Proprietà](#properties)
    -   [Gestori di comandi](#command-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Grazie all'emulazione dell'aspetto e delle funzionalità della selezione colori di Microsoft Office, il framework della barra multifunzione è in grado di trarre vantaggio da e contribuire alla coerenza e alla familiarità in un'ampia gamma di applicazioni.

## <a name="markup"></a>markup

Come tutti i controlli della barra multifunzione, Drop-Down Selezione colori è facilmente implementato e personalizzato tramite markup. Il framework fornisce una serie di attributi dell'elemento per Drop-Down Selezione colori esporre vari livelli di funzionalità. Nella tabella seguente sono elencati Drop-Down Selezione colori attributi.



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
<td>Modelli di layout che specificano il tipo di Drop-Down Selezione colori.<br/> Sono disponibili tre modelli, ognuno dei quali specifica un layout di controllo e i valori predefiniti per gli attributi associati e le chiavi di proprietà. <br/>
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
<td>Numero di colonne chip (o campione) di colore.<br/></td>
</tr>
<tr class="even">
<td>CommandName</td>
<td>Nome della dichiarazione Command associata. <br/></td>
</tr>
<tr class="odd">
<td>IsAutomaticColorButtonVisible</td>
<td>Visualizza o nasconde il <strong>pulsante</strong> Automatico.<br/> Valido solo quando <em>ColorTemplate</em> ha un valore <code>ThemeColors</code> di o <code>StandardColors</code> .<br/></td>
</tr>
<tr class="even">
<td>IsNoColorButtonVisible</td>
<td>Visualizza (o nasconde) il <strong>pulsante Nessun</strong> colore.<br/> Valido per tutti <em>i valori ColorTemplate.</em><br/></td>
</tr>
<tr class="odd">
<td>RecentColorGridRows</td>
<td>Numero di righe di chip di colori (o campione) nell'area <strong>Colori</strong> recenti.<br/> Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> .<br/></td>
</tr>
<tr class="even">
<td>StandardColorGridRows</td>
<td>Numero di righe chip di colori (o campione) nell'area <strong>Colori</strong> standard.<br/></td>
</tr>
<tr class="odd">
<td>ThemeColorGridRows</td>
<td>Numero di righe chip di colori (o campione) nell'area <strong>Colori tema.</strong><br/> Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> .<br/></td>
</tr>
</tbody>
</table>



 

Le schermate seguenti illustrano i layout Drop-Down Selezione colori predefiniti per i tre modelli di colore.



|     &nbsp;     |  &nbsp;   | &nbsp;  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ThemeColors`: \[ screenshot di nuova riga \] ![ dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su 'themecolors'. ](images/markup/colortemplate.themedcolors.1.png) \[ Newline\] | `standardcolors`: \[ screenshot di nuova riga \] ![ dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su 'standardcolors'. ](images/markup/colortemplate.standardcolors.3.png) \[ Newline\] | `highlightcolors`: \[ screenshot di nuova riga \] ![ dell'elemento dropdowncolorpicker con l'attributo colortemplate impostato su "highlightcolors".](images/markup/colortemplate.highlightcolors.2.png)<br/> |



 

Il markup di base necessario per Drop-Down Selezione colori tipo di dati è illustrato negli esempi seguenti:

> [!Note]  
> Il Drop-Down Selezione colori è un controllo [Button](windowsribbon-controls-button.md) valido in un [**modello SizeDefinition.**](windowsribbon-element-sizedefinition.md)

 


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

In quanto controllo specializzato che supporta la personalizzazione, qualsiasi implementazione del Drop-Down Selezione colori che sfrutta queste funzionalità richiede codice dell'applicazione specializzato per gestire le proprietà e gli eventuali comandi emessi dal controllo.

### <a name="properties"></a>Proprietà

Il framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il Drop-Down Selezione colori controllo .

In genere, una Drop-Down Selezione colori viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al [**metodo IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) L'evento di invalidamento viene gestito e la proprietà viene aggiornata dal metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

Il metodo di callback [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha eseguito una query per un valore di proprietà aggiornato, fino a quando la proprietà non è richiesta dal framework. Ad esempio, quando una scheda viene attivata e un controllo viene visualizzato nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al Drop-Down Selezione colori controllo .



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Chiave di proprietà</th>
<th>Descrizione</th>
<th>Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-automaticcolorlabel.md">UI_PKEY_AutomaticColorLabel</a></td>
<td>Definisce l'etichetta per il <strong>pulsante Colore</strong> automatico.<br/> Valido solo quando <em>ColorTemplate</em> ha un valore <code>ThemeColors</code> di o <code>StandardColors</code> .<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-color.md">UI_PKEY_Color</a></td>
<td>Definisce il valore del colore selezionato come <a href="/windows/win32/gdi/colorref">COLORREF.</a><br/> Valido solo quando <a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a> ha un valore pari a <code>UI_SWATCHCOLORTYPE_RGB</code> .<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-colortype.md">UI_PKEY_ColorType</a></td>
<td>Definisce il tipo di colore selezionato.<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Definisce la possibilità per un controllo di rispondere all'interazione dell'utente.<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>

<td>Può essere aggiornato solo tramite invalidamento.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Definisce la stringa di caratteri per un'etichetta di controllo.<br/></td>
<td>Può essere aggiornato solo tramite invalidamento.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Definisce l'immagine a contrasto elevato di grandi dimensioni da visualizzare per un controllo .<br/></td>
<td>Può essere aggiornato solo tramite invalidamento.<br/> Per altre informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">Specifica delle risorse immagine della barra multifunzione.</a><br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Definisce l'immagine grande da visualizzare per un controllo .<br/></td>
<td>Può essere aggiornato solo tramite invalidamento.<br/> Per altre informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">Specifica delle risorse immagine della barra multifunzione.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-morecolorslabel.md">UI_PKEY_MoreColorsLabel</a></td>
<td>Definisce l'etichetta per il <strong>pulsante Altri</strong> colori.<br/> Valido solo quando <em>ColorTemplate</em> ha un valore <code>ThemeColors</code> di o <code>StandardColors</code> .<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-nocolorlabel.md">UI_PKEY_NoColorLabel</a></td>
<td>Definisce l'etichetta per il <strong>pulsante Nessun</strong> colore.<br/> Valido per tutti <em>i valori ColorTemplate.</em><br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-recentcolorscategorylabel.md">UI_PKEY_RecentColorsCategoryLabel</a></td>
<td>Definisce l'etichetta per la <strong>categoria Colori</strong> recenti.<br/> Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> . Questo è l'unico modello che contiene categorie etichettate.<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Definisce la piccola immagine a contrasto elevato da visualizzare per un controllo .<br/></td>
<td>Può essere aggiornato solo tramite invalidamento.<br/> Per altre informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">Specifica delle risorse immagine della barra multifunzione.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Definisce l'immagine piccola da visualizzare per un controllo .<br/></td>
<td>Può essere aggiornato solo tramite invalidamento.<br/> Per altre informazioni sui formati di immagine, vedere <a href="windowsribbon-imageformats.md">Specifica delle risorse immagine della barra multifunzione.</a><br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolors.md">UI_PKEY_StandardColors</a></td>
<td>Definisce una matrice di <a href="/windows/win32/gdi/colorref">valori COLORREF</a> per i campioni di un Drop-Down Selezione colori.<br/> Ogni Drop-Down Selezione colori <em>ColorTemplate contiene</em> una <code>StandardColors</code> griglia. <br/>
<blockquote>
[!Note]<br />
Vengono visualizzati i valori <a href="/windows/win32/gdi/colorref">COLORREF</a> dell'oggetto <em>StandardColorGridRows</em> x <em>Columns</em> iniziale della matrice. Se la matrice definisce un numero di colori inferiore al numero di campioni dichiarati nel markup, vengono visualizzati spazi vuoti <code>StandardColors</code> per i chip mancanti.
</blockquote>
<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorscategorylabel.md">UI_PKEY_StandardColorsCategoryLabel</a></td>
<td>Definisce l'etichetta per la <strong>categoria Colori</strong> standard.<br/> Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> . Questo è l'unico modello che contiene categorie etichettate.<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-standardcolorstooltips.md">UI_PKEY_StandardColorsTooltips</a></td>
<td>Definisce una matrice di stringhe di descrizioni comando del controllo colore per la <code>StandardColors</code> griglia.<br/> Ogni Drop-Down Selezione colori <em>ColorTemplate contiene</em> una <code>StandardColors</code> griglia. <br/>
<blockquote>
[!Note]<br />
Vengono usate solo le descrizioni comandi necessarie per etichettare i campioni di colore visualizzati <code>StandardColors</code> nella griglia. Se vengono fornite meno etichette rispetto al numero di campioni nella griglia, viene fornito un valore predefinito per i campioni di <code>StandardColors</code> resto.
</blockquote>
<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolors.md">UI_PKEY_ThemeColors</a></td>
<td>Definisce una matrice di <a href="/windows/win32/gdi/colorref">valori COLORREF</a> per i campioni di un Drop-Down Selezione colori.<br/> Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Vengono visualizzati i valori <a href="/windows/win32/gdi/colorref">COLORREF</a> <em>dell'oggetto ThemeColorGridRows</em> x <em>Columns</em> iniziale della matrice. Se la matrice definisce un numero di colori inferiore al numero di campioni dichiarati nel markup, vengono visualizzati spazi vuoti <code>ThemeColors</code> per i chip mancanti.
</blockquote>
<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorstooltips.md">UI_PKEY_ThemeColorsTooltips</a></td>
<td>Definisce la matrice di stringhe di descrizioni comando del controllo colore per la <code>ThemeColors</code> griglia.<br/> Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> . <br/>
<blockquote>
[!Note]<br />
Vengono usate solo le descrizioni comandi necessarie per etichettare i campioni di colore visualizzati <code>ThemeColors</code> nella griglia. Se vengono fornite meno etichette rispetto al numero di campioni nella griglia, viene fornito un valore predefinito per i campioni di <code>ThemeColors</code> resto.
</blockquote>
<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-themecolorscategorylabel.md">UI_PKEY_ThemeColorsCategoryLabel</a></td>
<td>Definisce l'etichetta per la <strong>categoria Colori</strong> tema.<br/> Valido solo quando <em>ColorTemplate</em> ha un valore pari a <code>ThemeColors</code> . Questo è l'unico modello che contiene categorie etichettate.<br/></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Definisce la stringa di caratteri per una descrizione comando associata a un <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a>.<br/></td>
<td>Può essere aggiornato solo tramite invalidamento.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Definisce la stringa di caratteri per una descrizione comando.<br/></td>
<td>Può essere aggiornato solo tramite invalidamento.</td>
</tr>
</tbody>
</table>



 

### <a name="command-handlers"></a>Gestori di comandi

Il [**metodo IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) viene usato per personalizzare un Drop-Down Selezione colori tramite le chiavi di proprietà elencate in precedenza. L'esempio seguente illustra come impostare i campioni di colore di un Drop-Down Selezione colori, in base a una preferenza di stile personalizzata o a una griglia di controllo personalizzata dichiarata nel markup.


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



L'esempio seguente illustra un'implementazione del metodo [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) che espone i colori Drop-Down Selezione colori campione all'applicazione della barra multifunzione.


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

[Libreria di controlli del framework della barra multifunzione di Windows](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md)
</dt> <dt>

[Selezione colori proprietà](windowsribbon-reference-properties-colorpicker.md)
</dt> <dt>

[Personalizzazione di una barra multifunzione tramite definizioni delle dimensioni e criteri di ridimensionamento](windowsribbon-templates.md)
</dt> <dt>

[Esempio di DropDownColorPicker](windowsribbon-dropdowncolorpickersample.md)
</dt> </dl>

