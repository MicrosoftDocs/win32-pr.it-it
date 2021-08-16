---
title: Gruppo di schede
description: Un gruppo di schede è un controllo contestuale nascosto o visualizzato in fase di esecuzione, in base allo stato di un documento o di un'area di lavoro. Il gruppo di schede contiene un set di controlli Tab correlati al contesto.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ddf1c34903f0660f6f5ead5eb76cd17934ac5cc987358f24c32bc127c73706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117851257"
---
# <a name="tab-group"></a>Gruppo di schede

Un gruppo di schede è un controllo contestuale nascosto o visualizzato in fase di esecuzione, in base allo stato di un documento o di un'area di lavoro. Il gruppo di schede contiene un set di controlli Tab correlati [al](windowsribbon-controls-tab.md) contesto.

-   [Dettagli](#details)
-   [Proprietà del gruppo di schede](#tab-group-properties)
-   [Argomenti correlati](#related-topics)

## <a name="details"></a>Dettagli

In genere, un gruppo di schede viene visualizzato durante specifici stati del documento o dell'area di lavoro, ad esempio quando un utente seleziona un determinato tipo di oggetto. Ad esempio, la selezione di un'immagine contenuta nell'intestazione di una tabella potrebbe richiedere la visualizzazione di varie schede contestuali che espongono funzionalità sia di tabella che di immagine.

> [!IMPORTANT]
> Un gruppo di schede non supporta le [modalità applicazione](ribbon-applicationmodes.md). Tuttavia, i singoli [controlli Tab](windowsribbon-controls-tab.md) all'interno di un gruppo di schede possono.

 

La schermata seguente mostra una scheda [contestuale](windowsribbon-controls-tab.md) Windows 7 Paint.

![Screenshot che mostra un controllo Struttura a schede contestuale.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a>Proprietà del gruppo di schede

Il framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo Gruppo di schede.

In genere, una proprietà Gruppo schede viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) L'evento di invalidazione viene gestito e la proprietà viene aggiornata dal metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

Il metodo di callback [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha eseguito una query per un valore di proprietà aggiornato, fino a quando la proprietà non è richiesta dal framework. Ad esempio, quando una scheda viene attivata e un controllo viene visualizzato nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

Nella tabella seguente sono elencate le chiavi delle proprietà associate al controllo Gruppo di schede.



| Chiave di proprietà                                                                                     | Note                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Contesto \_ PKEY \_ dell'interfaccia utenteAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md)     | Supporta [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [Suggerimento \_ per la chiave PKEY \_ dell'interfaccia utente](windowsribbon-reference-properties-uipkey-keytip.md)                         | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |
| [Etichetta \_ PKEY \_ dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md)                           | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Può essere aggiornato solo tramite invalidazione.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Libreria di controlli Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup TabGroup**](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 