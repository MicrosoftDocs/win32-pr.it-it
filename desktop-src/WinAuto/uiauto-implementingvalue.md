---
title: Pattern di controllo value
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IValueProvider, incluse informazioni su proprietà e metodi.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo value
- Automazione interfaccia utente, pattern di controllo value
- Automazione interfaccia utente, IValueProvider
- IValueProvider
- implementazione di pattern di controllo Value di automazione interfaccia utente
- Pattern di controllo value
- pattern di controllo, IValueProvider
- pattern di controllo, implementazione del valore di automazione interfaccia utente
- pattern di controllo, valore
- interfacce, IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40633a21fdd6b59a2aa35c34258037582a647f05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399364"
---
# <a name="value-control-pattern"></a>Pattern di controllo value

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **value** viene usato per supportare i controlli con un valore intrinseco che non si estende su un intervallo e che può essere rappresentato come stringa.

La stringa di valore può essere modificabile, a seconda del controllo e delle relative impostazioni. Per esempi di controlli che implementano questo pattern di controllo, vedere [tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md).

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IValueProvider**](#required-members-for-ivalueprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **value** , tenere presenti le linee guida e le convenzioni seguenti:

-   I controlli, ad esempio un elemento elenco o un elemento albero, devono supportare il pattern di controllo **value** se il valore di uno degli elementi è modificabile, indipendentemente dalla modalità di modifica corrente del controllo. Il controllo padre deve supportare anche il pattern di controllo **value** se gli elementi figlio sono modificabili. Nell'immagine seguente viene illustrato un esempio di elemento di elenco modificabile.

    ![illustrazione che mostra l'elemento elenco modificabile](images/uia-valuepattern-editable-listitem.jpg)

- I controlli di modifica a riga singola e a più righe devono implementare [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) per esporre il contenuto di sola lettura.
- I controlli di modifica a più righe devono implementare [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) se il relativo contenuto può essere modificato.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) non supporta il recupero delle informazioni di formattazione o dei valori della sottostringa. Implementare [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in questi scenari.
- [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) deve essere implementato da controlli come il controllo di selezione della selezione colori di Microsoft Word (vedere l'immagine seguente), che supporta il mapping delle stringhe tra un valore di colore (ad esempio, "Yellow") e un valore [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) interno equivalente.

    ![illustrazione che mostra il mapping del campione di colore delle stringhe](images/uia-valuepattern-colorpicker.jpg)

- Una proprietà **IsEnabled** di un controllo deve essere impostata su **true** e la relativa proprietà [**ITextProvider:: IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) è impostata su **false** prima di consentire una chiamata a [**ITextProvider:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).

## <a name="required-members-for-ivalueprovider"></a>Membri obbligatori per **IValueProvider**

Per l'implementazione dell'interfaccia [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) sono necessari i metodi e le proprietà seguenti.



| Membri obbligatori                                       | Tipo di membro | Note |
|--------------------------------------------------------|-------------|-------|
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | Proprietà    | nessuno  |
| [**Valore**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | Proprietà    | nessuno  |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | Metodo      | nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[Pattern di controllo Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 