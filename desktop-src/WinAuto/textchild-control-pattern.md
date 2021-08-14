---
title: Pattern di controllo TextChild
description: Introduce linee guida e convenzioni per l'implementazione di ITextChildProvider, incluse le informazioni su proprietà e metodi. Il pattern di controllo TextChild viene usato per accedere al predecessore più vicino di un elemento che supporta il pattern di controllo Text.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- Automazione interfaccia utente,implementazione del pattern di controllo TextChild
- Automazione interfaccia utente,Pattern di controllo TextChild
- Automazione interfaccia utente,ITextChildProvider
- ITextChildProvider
- Implementazione Automazione interfaccia utente pattern di controllo TextChild
- Pattern di controllo TextChild
- pattern di controllo, ITextChildProvider
- pattern di controllo, implementazione Automazione interfaccia utente TextChild
- pattern di controllo, TextChild
- interfacce, ITextChildProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5c7bfb1852a02efc7baa789e137a4c05e2c2e85a65606109b26a622dfafcf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929044"
---
# <a name="textchild-control-pattern"></a>Pattern di controllo TextChild

Introduce linee guida e convenzioni per l'implementazione [**di ITextChildProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider)incluse le informazioni su proprietà e metodi. Il **pattern di controllo TextChild** viene usato per accedere al predecessore più vicino di un elemento che supporta il pattern di controllo [Text.](uiauto-implementingtextandtextrange.md)

Si supponga, ad esempio, che il testo in un documento contenga un'immagine incorporata e un collegamento ipertestuale, come illustrato nell'immagine seguente.

![Screenshot che mostra il testo contenente un'immagine incorporata e un collegamento ipertestuale](images/textchild-pattern.png)

Se si usano gli strumenti di Microsoft Automazione interfaccia utente per esaminare l'albero Automazione interfaccia utente per il contenuto del documento, è possibile che venga visualizzato un elemento documento con un elemento figlio che rappresenta l'immagine e un altro elemento figlio che rappresenta il collegamento ipertestuale. Esempio:

![Screenshot che mostra la segnalazione di un esempio di albero degli elementi di automazione interfaccia utente](images/textchild-pattern-tree.png)

In genere, l'elemento documento nell'esempio precedente supporta il pattern di controllo [Text,](uiauto-implementingtextandtextrange.md) mentre i due elementi figlio dell'elemento documento non lo supportano. Se un'applicazione client Automazione interfaccia utente ha un riferimento all'elemento immagine o all'elemento collegamento ipertestuale, il client può usare il pattern di controllo **TextChild** come modo pratico per accedere al pattern Textcontrol esposto dall'elemento del documento contenitore.

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa [**l'interfaccia ITextChildProvider,**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) tenere presente le linee guida e le convenzioni seguenti:

-   La [**proprietà ITextChildProvider::TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) deve specificare l'elemento predecessore più vicino che supporta l'interfaccia [**ITextProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) indipendentemente dal fatto che gli elementi superiori nella catena predecessore supportino **anche ITextProvider.**
-   Un elemento non deve supportare sia [**l'interfaccia ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) che [l'interfaccia ITextChildProvider**.](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider)
- Un elemento che implementa [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) deve essere figlio, o discendente, di un elemento che implementa [**ITextProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider) Non è necessario che questo elemento implementi anche il [pattern di controllo Text](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).
-   La proprietà [**ITextChildProvider::TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) deve specificare lo stesso intervallo di testo restituito dall'elemento del provider di testo contenitore quando la relativa funzione [**ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) viene chiamata con l'elemento figlio di testo come elemento figlio racchiuso.

## <a name="required-members-for-itextchildprovider"></a>Membri obbligatori per **ITextChildProvider**

Queste proprietà e metodi sono necessari per l'implementazione [**dell'interfaccia ITextChildProvider.**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider)



| Membri obbligatori                                                     | Tipo di membro | Note |
|----------------------------------------------------------------------|-------------|-------|
| [**Contenitore di testo**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | Proprietà    | Nessuno  |
| [**Textrange**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | Proprietà    | Nessuno  |



 

Questo pattern di controllo non è associato a metodi o eventi.

## <a name="related-topics"></a>Argomenti correlati

**Informazioni concettuali**

- [Tipi di controllo e pattern di controllo supportati](uiauto-controlpatternmapping.md)
- [Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
- [Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)