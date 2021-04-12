---
description: Le API di visualizzazione dell'input penna consentono alle app di Microsoft Win32 di gestire l'input, l'elaborazione e il rendering dell’input penna (standard e modificato) tramite un oggetto InkPresenter inserito nella struttura ad albero visuale dell'app DirectComposition.
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: Presentatore input penna
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9bd9f4c3c98b443110a0a7948075ab836a9493c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232542"
---
# <a name="ink-presenter"></a>Presentatore input penna

Le API Presenter di input penna consentono alle app Microsoft Win32 di gestire l'input, l'elaborazione e il rendering dell'input penna (standard e modificato) tramite un oggetto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) inserito nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app.

> [!Note]
>
> L'input input penna standard (suggerimento per la penna o suggerimento/pulsante della gomma) non viene modificato con una convenienza secondaria, ad esempio un pulsante della penna, un pulsante destro del mouse o simile.

Le app piattaforma UWP (Universal Windows Platform) (UWP) che usano Extensible Application Markup Language (XAML) forniscono questa funzionalità tramite un controllo [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) insieme a un oggetto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) che si connette alla struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) XAML. Per informazioni dettagliate, vedere [interazioni di penna e stilo](/windows/uwp/design/input/pen-and-stylus-interactions).

Il [renderer di input penna](ink-renderer.md) è progettato per essere usato dagli sviluppatori di app di Windows universali interessati a fornire la funzionalità di InkPresenter [**basata su**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)XAML / [](/uwp/api/windows.ui.input.inking.inkpresenter) in app Win32 native.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                               | Descrizione                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Classi Presenter di input penna](ink-presenter-classes.md)<br/>       | Negli argomenti contenuti in questa sezione vengono fornite le specifiche di riferimento per le classi del Presenter di input penna. <br/>    |
| [Interfacce del Presenter di input penna](ink-presenter-interfaces.md)<br/> | Gli argomenti contenuti in questa sezione forniscono le specifiche di riferimento per le interfacce del Presenter di input penna. <br/> |



 

## <a name="related-topics"></a>Argomenti correlati

[Relatore input](ink-presenter.md)penna, [interazioni tra penna e stilo](/windows/uwp/design/input/pen-and-stylus-interactions), [esempio di analisi dell'input penna](/samples/microsoft/windows-universal-samples/inkanalysis/), esempio di [Inking semplice](/samples/microsoft/windows-universal-samples/simpleink/), [esempio di Inking complesso](/samples/microsoft/windows-universal-samples/complexink/)
