---
title: Tab (Framework della barra multifunzione di Windows)
description: Una scheda contiene gruppi di controlli correlati.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340252"
---
# <a name="tab-windows-ribbon-framework"></a>Tab (Framework della barra multifunzione di Windows)

Una scheda contiene [gruppi](windowsribbon-controls-group.md) di controlli correlati.

-   [Dettagli](#details)
-   [Proprietà della scheda](#tab-properties)
-   [Argomenti correlati](#related-topics)

## <a name="details"></a>Dettagli

Sono disponibili tre tipi di scheda nel framework della barra multifunzione.



| Tipo               | Descrizione                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Scheda Core**       | Schede principali che consentono di organizzare le funzioni predefinite dell'applicazione.                                                                                                                                                                                                                   |
| **Scheda contestuale** | Schede visualizzate durante gli stati specifici del documento o dell'area di lavoro. Se, ad esempio, un utente seleziona un particolare tipo di oggetto, ad esempio un'immagine contenuta nell'intestazione di una tabella, è possibile che vengano visualizzate varie schede contestuali che espongono le funzionalità di tabella e immagine. |
| **Scheda modale**      | Schede principali visualizzate durante una [modalità di applicazione](ribbon-applicationmodes.md)di un documento o di un'area di lavoro specifica, ad esempio anteprima di stampa.                                                                                                                                        |



 

Lo screenshot seguente mostra una scheda di base di Paint di Windows 7.

![screenshot che mostra un controllo scheda principale.](images/controls/coretab.png)

## <a name="tab-properties"></a>Proprietà della scheda

Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo Tab.

In genere, una proprietà di tabulazione viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework. Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo struttura a schede.



| Chiave della proprietà                                                                                     | Note                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [\_Etichetta pkey dell'interfaccia utente \_](windowsribbon-reference-properties-uipkey-label.md)                           | Può essere aggiornato solo tramite l'invalidamento. |
| [Suggerimento tasto di interfaccia utente \_ pkey \_](windowsribbon-reference-properties-uipkey-keytip.md)                         | Può essere aggiornato solo tramite l'invalidamento. |
| [Interfaccia utente \_ pkey \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Può essere aggiornato solo tramite l'invalidamento. |
| [Interfaccia utente \_ pkey \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Può essere aggiornato solo tramite l'invalidamento. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento markup Tab**](windowsribbon-element-tab.md)
</dt> </dl>

 

 
