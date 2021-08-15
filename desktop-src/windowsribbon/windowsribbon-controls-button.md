---
title: Pulsante (Windows Ribbon Framework)
description: Il pulsante è un controllo su cui l'utente può fare clic per fornire input a un'applicazione.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82a1a71181b3478e065922b5a1836f6cd0f47bf9b3f2e497f45564118449b95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118707795"
---
# <a name="button-windows-ribbon-framework"></a>Pulsante (Windows Ribbon Framework)

Il pulsante è un controllo su cui l'utente può fare clic per fornire input a un'applicazione.

-   [Introduzione](#introduction)
-   [Proprietà pulsante](#button-properties)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

La schermata seguente contiene tre esempi dell'elemento Pulsante della barra multifunzione.

![Screenshot dei controlli pulsante nella barra multifunzione microsoft wordpad.](images/controls/button.png)

## <a name="button-properties"></a>Proprietà pulsante

Il framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo Button.

In genere, una proprietà Button viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) L'evento di invalidazione viene gestito e la proprietà viene aggiornata dal metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

Il metodo di callback [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha eseguito una query per un valore di proprietà aggiornato, fino a quando la proprietà non è richiesta dal framework. Ad esempio, quando una scheda viene attivata e un controllo viene visualizzato nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo Button.



| Chiave di proprietà                                                                                             | Note                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CHIAVE \_ PKEY dell'interfaccia \_ utente abilitata](windowsribbon-reference-properties-uipkey-enabled.md)                               | Supporta [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [Suggerimento \_ per la chiave PKEY \_ dell'interfaccia utente](windowsribbon-reference-properties-uipkey-keytip.md)                                 | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |
| [Etichetta \_ PKEY \_ dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md)                                   | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |
| [UI \_ PKEY \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)             | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |
| [UI \_ PKEY \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |
| [UI \_ PKEY \_ LargeImage](windowsribbon-reference-properties-uipkey-largeimage.md)                         | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |
| [UI \_ PKEY \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |
| [UI \_ PKEY \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)                         | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Libreria di controlli Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup button**](windowsribbon-element-button.md)
</dt> </dl>

 

 
