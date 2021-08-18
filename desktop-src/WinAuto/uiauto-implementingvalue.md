---
title: Pattern di controllo Value
description: Descrive le linee guida e le convenzioni per l'implementazione di IValueProvider, incluse le informazioni su proprietà e metodi.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo Value
- Automazione interfaccia utente,Pattern di controllo Value
- Automazione interfaccia utente,IValueProvider
- IValueProvider
- implementazione di pattern Automazione interfaccia utente value
- Pattern di controllo del valore
- pattern di controllo, IValueProvider
- pattern di controllo, implementazione Automazione interfaccia utente Value
- pattern di controllo, valore
- interfacce, IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b30d8c84bc5f998d55ee17d7699bb37f33b7e19c52a2694578c3d11ef1d888
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997807"
---
# <a name="value-control-pattern"></a>Pattern di controllo Value

Vengono descritte le linee guida e le convenzioni per [**l'implementazione di IValueProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)incluse le informazioni su proprietà e metodi. Il **pattern di** controllo Value viene usato per supportare i controlli che hanno un valore intrinseco che non si estende su un intervallo e che possono essere rappresentati come stringa.

La stringa del valore può essere modificabile, a seconda del controllo e delle relative impostazioni. Per esempi di controlli che implementano questo pattern di controllo, vedere [Tipi di controllo e pattern di controllo supportati.](uiauto-controlpatternmapping.md)

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IValueProvider**](#required-members-for-ivalueprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **Value,** tenere presente le linee guida e le convenzioni seguenti:

-   I controlli quali un elemento elenco o un elemento della struttura ad albero devono supportare il pattern di controllo **Value** se il valore di uno degli elementi è modificabile, indipendentemente dalla modalità di modifica corrente del controllo. Il controllo padre deve supportare anche il pattern di controllo **Value** se gli elementi figlio sono modificabili. L'immagine seguente mostra un esempio di elemento di elenco modificabile.

    ![illustrazione che mostra un elemento dell'elenco modificabile](images/uia-valuepattern-editable-listitem.jpg)

- I controlli di modifica a riga singola e su più righe devono implementare [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) per esporre il contenuto di sola lettura.
- I controlli di modifica su più righe devono [**implementare IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) se il relativo contenuto può essere modificato.
- [**IValueProvider non**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) supporta il recupero di informazioni di formattazione o valori di sottostringa. Implementare [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in questi scenari.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) deve essere implementato da controlli come il controllo di selezione colori di Microsoft Word (vedere l'immagine seguente), che supporta il mapping di stringhe tra un valore di colore (ad esempio, "giallo") e un valore [RGB interno equivalente.](/windows/win32/api/wingdi/nf-wingdi-rgb)

    ![illustrazione che mostra il mapping delle stringhe di controllo colore](images/uia-valuepattern-colorpicker.jpg)

- La proprietà **IsEnabled** di un controllo deve essere impostata su **TRUE** e la relativa proprietà [**ITextProvider::IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) deve essere impostata su **FALSE** prima di consentire una chiamata a [**ITextProvider::SetValue.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)

## <a name="required-members-for-ivalueprovider"></a>Membri obbligatori per **IValueProvider**

Per implementare l'interfaccia [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) sono necessari i metodi e le proprietà seguenti.



| Membri obbligatori                                       | Tipo di membro | Note |
|--------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | Proprietà    | Nessuno  |
| [**Valore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | Proprietà    | Nessuno  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | Metodo      | Nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[Pattern di controllo Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 