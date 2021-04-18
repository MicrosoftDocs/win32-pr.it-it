---
description: Gli argomenti contenuti in questa sezione forniscono le specifiche di riferimento per le interfacce del Presenter di input penna.
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: Interfacce del Presenter di input penna
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 1839c8ebc0a7597ab7c5becaf7c7492128b4d6af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310859"
---
# <a name="ink-presenter-interfaces"></a>Interfacce del Presenter di input penna

Gli argomenti contenuti in questa sezione forniscono le specifiche di riferimento per le interfacce del [Presenter di input penna](ink-presenter.md) .

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|---|---|
| [**IInkCommitRequestHandler**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | Abilita l'app (anziché un oggetto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) ) per eseguire il commit di tutti i comandi Microsoft DirectComposition in sospeso nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app.<br/>   |
| [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | Consente l'input, l'elaborazione e il rendering dell'input penna attraverso la creazione di un thread dell'applicazione per ospitare un oggetto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e inserirlo nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app. <br/> |
| [**IInkHostWorkItem**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | Rappresenta un'operazione di input penna da eseguire su un thread dell'oggetto [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) .<br/>                                                                                                                                                  |
| [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | Rappresenta un oggetto [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) che può essere configurato e inserito nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app di Windows classica. <br/>                                        |

## <a name="related-topics"></a>Argomenti correlati

[Relatore input](ink-presenter.md)penna, [interazioni tra penna e stilo](/windows/uwp/design/input/pen-and-stylus-interactions), [esempio di analisi dell'input penna](/samples/microsoft/windows-universal-samples/inkanalysis/), esempio di [Inking semplice](/samples/microsoft/windows-universal-samples/simpleink/), [esempio di Inking complesso](/samples/microsoft/windows-universal-samples/complexink/)
