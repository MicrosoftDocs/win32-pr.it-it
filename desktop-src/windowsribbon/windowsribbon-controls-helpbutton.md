---
title: Pulsante ?
description: Il pulsante ? è un controllo su cui l'utente può fare clic per visualizzare la Guida dell'applicazione.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 295b3c7feae2aecada128dadbccd093f654c6a6660a68f4790975aee060aaf61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933386"
---
# <a name="help-button"></a>Pulsante ?

Il pulsante ? è un controllo su cui l'utente può fare clic per visualizzare la Guida dell'applicazione.

-   [Dettagli](#details)
-   [Proprietà del pulsante ?](#help-button-properties)
-   [Argomenti correlati](#related-topics)

## <a name="details"></a>Dettagli

Lo screenshot seguente illustra il pulsante Guida della barra multifunzione.

![Screenshot che mostra il pulsante ?](images/controls/helpbutton.png)

## <a name="help-button-properties"></a>Proprietà del pulsante ?

Il framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo Pulsante ? .

In genere, una proprietà del pulsante della Guida viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) L'evento di invalidazione viene gestito e la proprietà viene aggiornata dal metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

Il metodo di callback [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha eseguito una query per un valore di proprietà aggiornato, fino a quando la proprietà non è richiesta dal framework. Ad esempio, quando una scheda viene attivata e un controllo viene visualizzato nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo Pulsante ? .



| Chiave di proprietà                                                                                     | Note                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [Suggerimento \_ per la chiave PKEY \_ dell'interfaccia utente](windowsribbon-reference-properties-uipkey-keytip.md)                         | Può essere aggiornato solo tramite invalidazione. |
| [Etichetta \_ PKEY \_ dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md)                           | Può essere aggiornato solo tramite invalidazione. |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Può essere aggiornato solo tramite invalidazione. |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Può essere aggiornato solo tramite invalidazione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Libreria di controlli Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento HelpButton**](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 