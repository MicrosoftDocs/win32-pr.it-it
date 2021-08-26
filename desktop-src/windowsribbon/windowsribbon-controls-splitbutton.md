---
title: Pulsante di menu combinato
description: Il pulsante di menu suddiviso è un controllo composito con cui l'utente può selezionare un valore predefinito associato a un pulsante primario oppure da un elenco di valori che si escludono a vicenda visualizzati in un elenco a discesa associato a un pulsante secondario.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066a2275c49ad8d6dd32dd8ce4fd3d89956f204c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473757"
---
# <a name="split-button"></a>Pulsante di menu combinato

Il pulsante di menu suddiviso è un controllo composito con cui l'utente può selezionare un valore predefinito associato a un pulsante primario oppure da un elenco di valori che si escludono a vicenda visualizzati in un elenco a discesa associato a un pulsante secondario.

-   [Introduzione](#introduction)
-   [Proprietà del pulsante di menu suddiviso](#split-button-properties)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Questo controllo è utile per esporre elementi strettamente correlati nei casi in cui è disponibile un'impostazione predefinita ovvia e in cui i singoli elementi possono essere rappresentati da un'immagine, da un testo o da entrambi.

Lo screenshot seguente illustra il pulsante di menu suddiviso della barra multifunzione.

![Screenshot di un controllo splitbutton in una barra multifunzione di esempio.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a>Proprietà del pulsante di menu suddiviso

Il framework della barra multifunzione definisce una raccolta di chiavi [di proprietà](windowsribbon-reference-properties.md) per il controllo Pulsante di menu suddiviso.

In genere, una proprietà split button viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al [**metodo IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) L'evento di invalidamento viene gestito e la proprietà viene aggiornata dal metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

Il metodo di callback [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha eseguito una query per un valore di proprietà aggiornato, fino a quando la proprietà non è richiesta dal framework. Ad esempio, quando una scheda viene attivata e un controllo viene visualizzato nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo Pulsante di menu suddiviso.




| Chiave di proprietà | Note | 
|--------------|-------|
| <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> | Supporta <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.<br /> Se tutti gli elementi figlio sono disabilitati, il framework <a href="windowsribbon-reference-properties-uipkey-enabled.md">imposta UI_PKEY_Enabled</a> su false (0). In caso contrario, se uno o più elementi figlio sono abilitati, UI_PKEY_Enabled è impostato su true (-1).<blockquote>[!Important]<br />La <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> proprietà per il controllo Pulsante di menu suddiviso deve essere invalidata dopo che uno o più elementi figlio sono stati abilitati o disabilitati. In questo modo il framework esegue query sul valore della proprietà aggiornato e aggiorna lo stato del controllo Pulsante di menu suddiviso nell'interfaccia utente della barra multifunzione.</blockquote><br /><br /> | 
| <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a> | Può essere aggiornato solo tramite invalidamento. | 
| <a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a> | Può essere aggiornato solo tramite invalidamento. | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Libreria di controlli del framework della barra multifunzione](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup SplitButton**](windowsribbon-element-splitbutton.md)
</dt> </dl>
