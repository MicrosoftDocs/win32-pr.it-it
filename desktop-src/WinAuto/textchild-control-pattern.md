---
title: Pattern di controllo TextChild
description: Introduce le linee guida e le convenzioni per l'implementazione di ITextChildProvider, incluse informazioni su proprietà e metodi. Il pattern di controllo TextChild viene usato per accedere al predecessore più vicino di un elemento che supporta il pattern di controllo Text.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo TextChild
- Automazione interfaccia utente, pattern di controllo TextChild
- Automazione interfaccia utente, ITextChildProvider
- ITextChildProvider
- implementazione di pattern di controllo TextChild di automazione interfaccia utente
- Pattern di controllo TextChild
- pattern di controllo, ITextChildProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente TextChild
- pattern di controllo, TextChild
- interfacce, ITextChildProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21102abfef7cee0553850ac01c4f759f81988e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729954"
---
# <a name="textchild-control-pattern"></a>Pattern di controllo TextChild

Introduce le linee guida e le convenzioni per l'implementazione di [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), incluse informazioni su proprietà e metodi. Il pattern di controllo **TextChild** viene usato per accedere al predecessore più vicino di un elemento che supporta il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) .

Si supponga, ad esempio, che il testo in un documento contenga un'immagine incorporata e un collegamento ipertestuale, come illustrato nella figura seguente.

![screenshot che mostra il testo che contiene un'immagine incorporata e un collegamento ipertestuale](images/textchild-pattern.png)

Se si usano gli strumenti di automazione interfaccia utente Microsoft per esaminare l'albero di automazione interfaccia utente per questo contenuto del documento, è possibile che venga visualizzato un elemento documento con un elemento figlio che rappresenta l'immagine e un altro elemento figlio che rappresenta il collegamento ipertestuale. Ad esempio:

![screenshot che Mostra come controllare la creazione di un esempio di albero degli elementi di automazione interfaccia utente](images/textchild-pattern-tree.png)

In genere, l'elemento Document nell'esempio precedente supporta il pattern di controllo [Text](uiauto-implementingtextandtextrange.md) , ma i due elementi figlio dell'elemento document non lo fanno. Se un'applicazione client di automazione interfaccia utente contiene un riferimento all'elemento Image o al collegamento ipertestuale, il client può usare il pattern di controllo **TextChild** come modo pratico per accedere al modello TextControl esposto dall'elemento del documento contenitore.

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa l'interfaccia [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) , tenere presenti le linee guida e le convenzioni seguenti:

-   Per la proprietà [**ITextChildProvider:: TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) è necessario specificare l'elemento predecessore più vicino che supporta l'interfaccia [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) , indipendentemente dal fatto che gli elementi superiori nella catena di predecessore supportino anche **ITextProvider**.
-   Un elemento non deve supportare sia l'interfaccia [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) che l'interfaccia [ITextChildProvider * *](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .
- Un elemento che implementa [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) deve essere un elemento figlio o discendente di un elemento che implementa [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider). Non è necessario che questo elemento implementi anche il [pattern di controllo Text](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).
-   La proprietà [**ITextChildProvider:: TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) deve specificare lo stesso intervallo di testo restituito dall'elemento del provider di testo contenitore quando la funzione [**ITextProvider:: RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) viene chiamata con l'elemento figlio text come elemento figlio racchiuso.

## <a name="required-members-for-itextchildprovider"></a>Membri obbligatori per **ITextChildProvider**

Queste proprietà e questi metodi sono necessari per implementare l'interfaccia [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .



| Membri obbligatori                                                     | Tipo di membro | Note |
|----------------------------------------------------------------------|-------------|-------|
| [**TextContainer**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | Proprietà    | nessuno  |
| [**TextRange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | Proprietà    | nessuno  |



 

Questo pattern di controllo non è associato a metodi o eventi.

## <a name="related-topics"></a>Argomenti correlati

**Informazioni concettuali**

- [Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
- [Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
- [Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)