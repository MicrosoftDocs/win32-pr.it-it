---
title: In-Ribbon Gallery
description: La In-Ribbon è un controllo che visualizza una raccolta di elementi correlati o comandi nella barra multifunzione. Se la raccolta contiene troppi elementi, viene visualizzata una freccia di espansione per visualizzare il resto della raccolta in un riquadro espanso.
ms.assetid: d608dd0d-a0af-49a6-a129-7115195c0df2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713455e962996e2cc1a70b418000d0f94a383174
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479797"
---
# <a name="in-ribbon-gallery"></a>In-Ribbon Gallery

La In-Ribbon è un controllo che visualizza una raccolta di elementi correlati o comandi nella barra multifunzione. Se la raccolta contiene troppi elementi, viene visualizzata una freccia di espansione per visualizzare il resto della raccolta in un riquadro espanso.

-   [Dettagli](#details)
-   [Proprietà della raccolta nella barra multifunzione](#in-ribbon-gallery-properties)
-   [Argomenti correlati](#related-topics)

## <a name="details"></a>Dettagli

Lo screenshot seguente illustra il controllo Raccolta In-Ribbon barra multifunzione in Microsoft Paint.

![Screenshot di un controllo inribbongallery nella barra multifunzione Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="in-ribbon-gallery-properties"></a>proprietà In-Ribbon Gallery

Il framework della barra multifunzione definisce una raccolta di chiavi [di proprietà](windowsribbon-reference-properties.md) per In-Ribbon controllo Raccolta.

In genere, una In-Ribbon gallery viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al [**metodo IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) L'evento di invalidamento viene gestito e la proprietà viene aggiornata dal metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

Il metodo di callback [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha eseguito una query per un valore di proprietà aggiornato, fino a quando la proprietà non è richiesta dal framework. Ad esempio, quando una scheda viene attivata e un controllo viene visualizzato nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo In-Ribbon Gallery.




| Chiave di proprietà | Note | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a> | Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a> | Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>. | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(valido solo per una raccolta di elementi)<br /> | Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.<blockquote>[!Note]<br />Se il comando associato al controllo viene invalidato tramite una chiamata a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, il framework esegue una query su questa proprietà quando viene passato come valore dei <code>UI_INVALIDATIONS_VALUE</code> <em>flag</em>.</blockquote><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Può essere aggiornato solo tramite invalidamento. | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Libreria di controlli del framework della barra multifunzione](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento InRibbonGallery**](windowsribbon-element-inribbongallery.md)
</dt> <dt>

[Uso delle raccolte](ribbon-controls-galleries.md)
</dt> <dt>

[Esempio di raccolta](windowsribbon-gallerysample.md)
</dt> </dl>

