---
title: Interruttore
description: L'interruttore quando si fa clic fornisce l'input per un'applicazione. Il controllo rappresenta uno stato dell'interruttore a esclusione reciproca.
ms.assetid: 290052b7-0528-41c5-b6f4-958cc42d502b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72c06f8382e7210f1041960b92de5f6054548d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104562526"
---
# <a name="toggle-button"></a>Interruttore

L'interruttore quando si fa clic fornisce l'input per un'applicazione. Il controllo rappresenta uno stato dell'interruttore a esclusione reciproca.

-   [Dettagli](#details)
-   [Imposta/Nascondi proprietà pulsante](#toggle-button-properties)
-   [Argomenti correlati](#related-topics)

## <a name="details"></a>Dettagli

Lo screenshot seguente illustra l'interruttore della barra multifunzione.

![Screenshot di un controllo ToggleButton sulla barra multifunzione di Microsoft Paint.](images/controls/togglebutton.png)

## <a name="toggle-button-properties"></a>Imposta/Nascondi proprietà pulsante

Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo interruttore.

In genere, la proprietà di un interruttore viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework. Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo interruttore.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Chiave della proprietà</th>
<th>Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.
<blockquote>
[!Note]<br />
Se il comando associato al controllo viene invalidato tramite una chiamata a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, il Framework esegue una query su questa proprietà quando <code>UI_INVALIDATIONS_VALUE</code> viene passato come valore di <em>flag</em>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Può essere aggiornato solo tramite l'invalidamento.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento markup ToggleButton**](windowsribbon-element-togglebutton.md)
</dt> </dl>

