---
title: Scheda (Windows del framework della barra multifunzione)
description: Una scheda contiene gruppi di controlli correlati.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fae518c29e91dac8518c6dc217228e23d0521a562043849f8352783e26e5855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592176"
---
# <a name="tab-windows-ribbon-framework"></a>Scheda (Windows del framework della barra multifunzione)

Una scheda contiene [gruppi](windowsribbon-controls-group.md) di controlli correlati.

-   [Dettagli](#details)
-   [Proprietà della scheda](#tab-properties)
-   [Argomenti correlati](#related-topics)

## <a name="details"></a>Dettagli

Nel framework della barra multifunzione sono disponibili tre tipi di scheda.



| Tipo               | Descrizione                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Scheda Core**       | Schede principali che organizzano le funzioni predefinite dell'applicazione.                                                                                                                                                                                                                   |
| **Scheda contestuale** | Schede visualizzate durante stati specifici del documento o dell'area di lavoro. Ad esempio, se un utente seleziona un particolare tipo di oggetto, ad esempio un'immagine contenuta nell'intestazione di una tabella, potrebbero essere visualizzate diverse schede contestuali che espongono sia la funzionalità di tabella che di immagine. |
| **Scheda Modale**      | Schede principali visualizzate durante la modalità di applicazione di un documento o di un'area di lavoro [specifica,](ribbon-applicationmodes.md)ad esempio l'anteprima di stampa.                                                                                                                                        |



 

La schermata seguente mostra una scheda principale Windows 7 Paint.

![Screenshot che mostra un controllo Struttura a schede principale.](images/controls/coretab.png)

## <a name="tab-properties"></a>Proprietà della scheda

Il framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo Tab.

In genere, una proprietà Tab viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) L'evento di invalidazione viene gestito e la proprietà viene aggiornata dal metodo di callback [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

Il metodo di callback [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha eseguito una query per un valore di proprietà aggiornato, fino a quando la proprietà non è richiesta dal framework. Ad esempio, quando una scheda viene attivata e un controllo viene visualizzato nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo Tab.



| Chiave di proprietà                                                                                     | Note                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [Etichetta \_ PKEY \_ dell'interfaccia utente](windowsribbon-reference-properties-uipkey-label.md)                           | Può essere aggiornato solo tramite invalidazione. |
| [Suggerimento \_ per la chiave PKEY \_ dell'interfaccia utente](windowsribbon-reference-properties-uipkey-keytip.md)                         | Può essere aggiornato solo tramite invalidazione. |
| [UI \_ PKEY \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Può essere aggiornato solo tramite invalidazione. |
| [UI \_ PKEY \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Può essere aggiornato solo tramite invalidazione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Libreria di controlli Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento di markup Tab**](windowsribbon-element-tab.md)
</dt> </dl>

 

 
