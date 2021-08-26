---
description: Gli argomenti contenuti in questa sezione forniscono le specifiche di riferimento per le interfacce del presentatore ink.
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: Interfacce del presentatore di input penna
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 0c1fb4cab0b8387dec7c75087a72719f72fbc85dc2776a5e20fc6d638fb02d95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092391"
---
# <a name="ink-presenter-interfaces"></a>Interfacce del presentatore di input penna

Gli argomenti contenuti in questa sezione forniscono le specifiche di riferimento per le [interfacce del presentatore](ink-presenter.md) ink.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|---|---|
| [**IInkCommitRequestHandler**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | Consente all'app (anziché a un oggetto [**IInkPresenterDesktop)**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) di eseguire il commit di tutti i comandi Microsoft DirectComposition in sospeso nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app.<br/>   |
| [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | Abilita l'input penna, l'elaborazione e il rendering tramite la creazione di un thread dell'app per ospitare un oggetto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e inserirlo nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app. <br/> |
| [**IInkHostWorkItem**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | Rappresenta un'operazione di input penna da eseguire su un thread [**dell'oggetto IInkDesktopHost.**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>                                                                                                                                                  |
| [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | Rappresenta un [**oggetto InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) che può essere configurato e inserito nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app Windows classica. <br/>                                        |

## <a name="related-topics"></a>Argomenti correlati

[Presentatore di input](ink-presenter.md)penna, [Interazioni con penna e stilo,](/windows/uwp/design/input/pen-and-stylus-interactions) [Esempio](/samples/microsoft/windows-universal-samples/inkanalysis/)di analisi dell'input penna, Esempio di input penna [semplice,](/samples/microsoft/windows-universal-samples/simpleink/) [Esempio di input penna complesso](/samples/microsoft/windows-universal-samples/complexink/)
