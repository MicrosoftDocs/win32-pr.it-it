---
title: Gruppo di schede
description: Un gruppo di schede è un controllo contestuale nascosto o visualizzato in fase di esecuzione, in base allo stato di un documento o di un'area di lavoro. Il gruppo di schede contiene un set di controlli scheda relativi al contesto.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338639"
---
# <a name="tab-group"></a>Gruppo di schede

Un gruppo di schede è un controllo contestuale nascosto o visualizzato in fase di esecuzione, in base allo stato di un documento o di un'area di lavoro. Il gruppo di schede contiene un set di controlli [scheda](windowsribbon-controls-tab.md) relativi al contesto.

-   [Dettagli](#details)
-   [Proprietà gruppo di schede](#tab-group-properties)
-   [Argomenti correlati](#related-topics)

## <a name="details"></a>Dettagli

In genere, viene visualizzato un gruppo di schede durante gli stati specifici del documento o dell'area di lavoro, ad esempio quando un utente seleziona un determinato tipo di oggetto. Per la selezione di un'immagine contenuta nell'intestazione di una tabella, ad esempio, potrebbe essere necessario visualizzare diverse schede contestuali che espongono la funzionalità di tabella e immagine.

> [!IMPORTANT]
> Un gruppo di schede non supporta le [modalità di applicazione](ribbon-applicationmodes.md). Tuttavia, i singoli controlli [scheda](windowsribbon-controls-tab.md) in un gruppo di schede possono.

 

Lo screenshot seguente mostra una [scheda](windowsribbon-controls-tab.md) contestuale del disegno di Windows 7.

![screenshot che mostra un controllo scheda contestuale.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a>Proprietà gruppo di schede

Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo gruppo di schede.

In genere, una proprietà del gruppo di schede viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework. Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo gruppo di schede.



| Chiave della proprietà                                                                                     | Note                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaccia utente \_ pkey \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md)     | Supporta [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [Suggerimento tasto di interfaccia utente \_ pkey \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [\_Etichetta pkey dell'interfaccia utente \_](windowsribbon-reference-properties-uipkey-label.md)                           | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [Interfaccia utente \_ pkey \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |
| [Interfaccia utente \_ pkey \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup TabGroup**](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 