---
description: Le API di visualizzazione dell'input penna consentono alle app di Microsoft Win32 di gestire l'input, l'elaborazione e il rendering dell’input penna (standard e modificato) tramite un oggetto InkPresenter inserito nella struttura ad albero visuale dell'app DirectComposition.
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: Presentatore input penna
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ccd201f39cf232e91c65d8ef15c6ccc0e8202b231818aa50d34d70f780f2d9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977021"
---
# <a name="ink-presenter"></a>Presentatore input penna

Le API del presentatore di input penna consentono alle app Microsoft Win32 di gestire l'input, l'elaborazione e il rendering dell'input penna (standard e modificato) tramite un oggetto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) inserito nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app.

> [!Note]
>
> L'input input penna standard (punta della penna o punta della gomma/pulsante) non viene modificato con un affordance secondario, ad esempio un pulsante pentole, un pulsante destro del mouse o simili.

Le app UWP (Universal Windows Platform) che usano Extensible Application Markup Language (XAML) forniscono questa funzionalità tramite un controllo [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) insieme a un oggetto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) che si connette alla struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) XAML. Per altre informazioni, vedere [Interazioni con penna e stilo.](/windows/uwp/design/input/pen-and-stylus-interactions)

[Il renderer di](ink-renderer.md) input penna è progettato per l'uso da parte degli sviluppatori di app universal Windows interessati a fornire funzionalità [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)InkPresenter basate su XAML nelle app / [](/uwp/api/windows.ui.input.inking.inkpresenter) Win32 native.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                               | Descrizione                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Classi del presentatore di input penna](ink-presenter-classes.md)<br/>       | Gli argomenti contenuti in questa sezione forniscono le specifiche di riferimento per le classi del presentatore ink. <br/>    |
| [Interfacce del presentatore di input penna](ink-presenter-interfaces.md)<br/> | Gli argomenti contenuti in questa sezione forniscono le specifiche di riferimento per le interfacce del presentatore ink. <br/> |



 

## <a name="related-topics"></a>Argomenti correlati

[Presentatore di input](ink-presenter.md)penna, [Interazioni con penna e stilo,](/windows/uwp/design/input/pen-and-stylus-interactions) [Esempio](/samples/microsoft/windows-universal-samples/inkanalysis/)di analisi dell'input penna, Esempio di input penna [semplice,](/samples/microsoft/windows-universal-samples/simpleink/) [Esempio di input penna complesso](/samples/microsoft/windows-universal-samples/complexink/)
