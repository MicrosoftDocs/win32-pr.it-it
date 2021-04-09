---
title: Button (Framework della barra multifunzione di Windows)
description: Il pulsante è un controllo su cui l'utente può fare clic per fornire l'input a un'applicazione.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118751"
---
# <a name="button-windows-ribbon-framework"></a>Button (Framework della barra multifunzione di Windows)

Il pulsante è un controllo su cui l'utente può fare clic per fornire l'input a un'applicazione.

-   [Introduzione](#introduction)
-   [Proprietà pulsante](#button-properties)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Lo screenshot seguente contiene tre esempi dell'elemento Button della barra multifunzione.

![screenshot dei controlli Button nella barra multifunzione di Microsoft WordPad.](images/controls/button.png)

## <a name="button-properties"></a>Proprietà pulsante

Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo Button.

In genere, una proprietà Button viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework. Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo Button.



| Chiave della proprietà                                                                                             | Note                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaccia utente \_ pkey \_ abilitata](windowsribbon-reference-properties-uipkey-enabled.md)                               | Supporta [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [Suggerimento tasto di interfaccia utente \_ pkey \_](windowsribbon-reference-properties-uipkey-keytip.md)                                 | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [\_Etichetta pkey dell'interfaccia utente \_](windowsribbon-reference-properties-uipkey-label.md)                                   | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [Interfaccia utente \_ pkey \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)             | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [Interfaccia utente \_ pkey \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [Interfaccia utente \_ pkey \_ largeImage](windowsribbon-reference-properties-uipkey-largeimage.md)                         | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [Interfaccia utente \_ pkey \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [Interfaccia utente \_ pkey \_ smallImage](windowsribbon-reference-properties-uipkey-smallimage.md)                         | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [Interfaccia utente \_ pkey \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [Interfaccia utente \_ pkey \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento markup Button**](windowsribbon-element-button.md)
</dt> </dl>

 

 
