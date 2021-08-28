---
title: Drop-Down pulsante
description: Il Drop-Down è costituito da un pulsante che, quando selezionato, visualizza un elenco a discesa di elementi che si escludono a vicenda.
ms.assetid: 41c5da07-43f7-4544-83be-248941cb8633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887b5979d5536b255526789aa541a6f2d1b67d1b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473517"
---
# <a name="drop-down-button"></a>Drop-Down pulsante

Il Drop-Down è costituito da un pulsante che, quando selezionato, visualizza un elenco a discesa di elementi che si escludono a vicenda.

-   [Dettagli](#details)
-   [Proprietà dei pulsanti a discesa](#drop-down-button-properties)
-   [Argomenti correlati](#related-topics)

## <a name="details"></a>Dettagli

Questo controllo è utile per esporre elementi strettamente correlati nei casi in cui non sono disponibili impostazioni predefinite ovvie e in cui i singoli elementi possono essere rappresentati da un'immagine, da un testo o da entrambi.

Lo screenshot seguente illustra il pulsante Drop-Down barra multifunzione in una barra multifunzione di esempio.

![screenshot di un controllo pulsante a discesa in una barra multifunzione di esempio.](images/controls/dropdownbutton.png)

## <a name="drop-down-button-properties"></a>Drop-Down proprietà del pulsante

Il framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per Drop-Down controllo Button.

In genere, una Drop-Down button viene aggiornata nell'interfaccia utente della barra multifunzione invalidando l'oggetto Command associato al controllo tramite una chiamata al [**metodo IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) L'evento di invalidamento viene gestito e la proprietà viene aggiornata dal metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

Il metodo di callback [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha eseguito una query per un valore di proprietà aggiornato, fino a quando la proprietà non è richiesta dal framework. Ad esempio, quando una scheda viene attivata e un controllo viene visualizzato nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

Nella tabella seguente sono elencate le chiavi di proprietà associate Drop-Down controllo Button.




| Chiave di proprietà | Note | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a> | Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.<br /> Se tutti gli elementi figlio sono disabilitati, il framework <a href="windowsribbon-reference-properties-uipkey-enabled.md">imposta UI_PKEY_Enabled</a> su false (0). In caso contrario, se uno o più elementi figlio sono abilitati, UI_PKEY_Enabled è impostato su true (-1).<blockquote>[!Important]<br />La <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> proprietà per il controllo Drop-Down Button deve essere invalidata dopo l'a attivazione o la disabilitazione di uno o più elementi figlio. In questo modo il framework esegue query sul valore della proprietà aggiornato e aggiorna lo stato del controllo pulsante Drop-Down nell'interfaccia utente della barra multifunzione.</blockquote><br /><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a> | Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a> | Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.<blockquote>[!Note]<br />Se il comando associato al controllo viene invalidato tramite una chiamata a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, il framework esegue una query su questa proprietà quando viene passato come valore dei <code>UI_INVALIDATIONS_VALUE</code> <em>flag</em>.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Può essere aggiornato solo tramite invalidamento. | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Libreria di controlli del framework della barra multifunzione](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup DropDownButton**](windowsribbon-element-dropdownbutton.md)
</dt> </dl>
