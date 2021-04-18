---
description: Informazioni sulle diverse API di Inking desktop per le app di Windows.
ms.assetid: 0691afb1-575a-4bb7-8fa5-006b231b8f1f
title: Input input penna
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ffb67d452e3bee327195f8ff920bfcab3c0232a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315060"
---
# <a name="ink-input"></a><span data-ttu-id="1fe85-103">Input input penna</span><span class="sxs-lookup"><span data-stu-id="1fe85-103">Ink input</span></span>

<span data-ttu-id="1fe85-104">Informazioni sulle diverse API di Inking desktop per le app di Windows.</span><span class="sxs-lookup"><span data-stu-id="1fe85-104">Learn about the various Desktop inking APIs for Windows apps.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1fe85-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="1fe85-105">In this section</span></span>

| <span data-ttu-id="1fe85-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="1fe85-106">Topic</span></span> | <span data-ttu-id="1fe85-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fe85-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="1fe85-108">Presentatore input penna</span><span class="sxs-lookup"><span data-stu-id="1fe85-108">Ink presenter</span></span>](ink-presenter.md)<br/> | <span data-ttu-id="1fe85-109">Le API Presenter di input penna consentono alle app Microsoft Win32 di gestire l'input, l'elaborazione e il rendering dell'input penna (standard e modificato) tramite un oggetto [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) inserito nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app.</span><span class="sxs-lookup"><span data-stu-id="1fe85-109">The ink presenter APIs enable Microsoft Win32 apps to manage the input, processing, and rendering of ink input (standard and modified) through an [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) object inserted into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span><br/> |
| [<span data-ttu-id="1fe85-110">Renderer di input penna</span><span class="sxs-lookup"><span data-stu-id="1fe85-110">Ink renderer</span></span>](ink-renderer.md)<br/>   | <span data-ttu-id="1fe85-111">Le API [renderer di input penna](ink-renderer.md) consentono il rendering dei tratti di input penna nel contesto di periferica Direct2D designato di un'app di Windows universale, anziché il controllo [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) predefinito.</span><span class="sxs-lookup"><span data-stu-id="1fe85-111">The [Ink renderer](ink-renderer.md) APIs enable the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span><br/>                                                                        |

## <a name="related-topics"></a><span data-ttu-id="1fe85-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1fe85-112">Related topics</span></span>

<span data-ttu-id="1fe85-113">[Interazioni di penna e stilo](/windows/uwp/design/input/pen-and-stylus-interactions), [esempio di analisi dell'input penna](/samples/microsoft/windows-universal-samples/inkanalysis/), esempio di [Inking semplice](/samples/microsoft/windows-universal-samples/simpleink/), [esempio di Inking complesso](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="1fe85-113">[Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
