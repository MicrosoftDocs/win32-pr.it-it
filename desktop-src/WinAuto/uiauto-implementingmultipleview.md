---
title: Pattern di controllo MultipleView
description: Vengono descritte le linee guida e le convenzioni per l'implementazione di IMultipleViewProvider, incluse informazioni su proprietà e metodi.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Automazione interfaccia utente, implementazione del pattern di controllo MultipleView
- Automazione interfaccia utente, pattern di controllo MultipleView
- Automazione interfaccia utente, IMultipleViewProvider
- IMultipleViewProvider
- implementazione di pattern di controllo MultipleView di automazione interfaccia utente
- Pattern di controllo MultipleView
- pattern di controllo, IMultipleViewProvider
- pattern di controllo, implementazione dell'automazione interfaccia utente MultipleView
- pattern di controllo, MultipleView
- interfacce, IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396270"
---
# <a name="multipleview-control-pattern"></a>Pattern di controllo MultipleView

Vengono descritte le linee guida e le convenzioni per l'implementazione di [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), incluse informazioni su proprietà e metodi. Alla fine della panoramica sono elencati collegamenti ad altro materiale di riferimento. Il pattern di controllo **MultipleView** viene usato per supportare i controlli che forniscono e sono in grado di passare tra più rappresentazioni delle stesse informazioni o dello stesso set di controlli figlio.

Esempi di controlli che possono presentare più viste includono la visualizzazione elenco, che può mostrare il contenuto come anteprime, riquadri, icone o dettagli), grafici di Microsoft Excel (a torta, a linee, a barre, valore della cella con una formula), documenti di Microsoft Word (normale, layout Web, layout di stampa, layout di lettura, struttura), calendario di Microsoft Outlook (anno, mese, settimana, giorno) e interfacce di Media Player di Microsoft Windows. Le visualizzazioni supportate sono determinate dallo sviluppatore del controllo e sono specifiche di ogni controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Linee guida e convenzioni di implementazione](#implementation-guidelines-and-conventions)
-   [Membri obbligatori per **IMultipleViewProvider**](#required-members-for-imultipleviewprovider)
-   [Argomenti correlati](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Linee guida e convenzioni di implementazione

Quando si implementa il pattern di controllo **MultipleView** , tenere presenti le linee guida e le convenzioni seguenti:

-   [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) deve essere implementato anche in un contenitore che gestisce la visualizzazione corrente se è diverso da un controllo che fornisce la visualizzazione corrente. Ad esempio, Esplora risorse contiene un controllo elenco per il contenuto della cartella corrente, mentre la visualizzazione per il controllo viene gestita dall'applicazione Esplora risorse.
-   Un controllo in grado di ordinare il relativo contenuto non supporta più visualizzazioni.
-   La raccolta di visualizzazioni deve essere identica tra istanze.
-   I nomi delle visualizzazioni devono essere adatti per l'uso in sintesi vocale, Braille e altre applicazioni leggibili.

## <a name="required-members-for-imultipleviewprovider"></a>Membri obbligatori per **IMultipleViewProvider**

Le proprietà e i metodi seguenti sono necessari per implementare l'interfaccia [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) .



| Membri obbligatori                                                            | Tipo di membro | Note |
|-----------------------------------------------------------------------------|-------------|-------|
| [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | Proprietà    | nessuno  |
| [**GetSupportedViews**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | Metodo      | nessuno  |
| [**GetViewName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | Metodo      | nessuno  |
| [**SetCurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | Metodo      | nessuno  |



 

Questo pattern di controllo non è associato a eventi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di controllo e i pattern di controllo supportati](uiauto-controlpatternmapping.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Panoramica dell'albero di automazione dell'interfaccia utente](uiauto-treeoverview.md)
</dt> <dt>

[Pattern di controllo ExpandCollapse](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




