---
title: Pulsante della Guida
description: Il pulsante? è un controllo su cui l'utente può fare clic per visualizzare il sistema di guida dell'applicazione.
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963101"
---
# <a name="help-button"></a>Pulsante della Guida

Il pulsante? è un controllo su cui l'utente può fare clic per visualizzare il sistema di guida dell'applicazione.

-   [Dettagli](#details)
-   [Proprietà pulsante della Guida](#help-button-properties)
-   [Argomenti correlati](#related-topics)

## <a name="details"></a>Dettagli

Lo screenshot seguente illustra il pulsante della guida della barra multifunzione.

![screenshot che mostra il pulsante della guida.](images/controls/helpbutton.png)

## <a name="help-button-properties"></a>Proprietà pulsante della Guida

Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo pulsante della guida.

In genere, la proprietà di un pulsante della guida viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework. Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo pulsante della guida.



| Chiave della proprietà                                                                                     | Note                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [Suggerimento tasto di interfaccia utente \_ pkey \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Può essere aggiornato solo tramite l'invalidamento. |
| [\_Etichetta pkey dell'interfaccia utente \_](windowsribbon-reference-properties-uipkey-label.md)                           | Può essere aggiornato solo tramite l'invalidamento. |
| [Interfaccia utente \_ pkey \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Può essere aggiornato solo tramite l'invalidamento. |
| [Interfaccia utente \_ pkey \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Può essere aggiornato solo tramite l'invalidamento. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento HelpButton**](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 