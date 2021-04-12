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
# <a name="ink-presenter"></a><span data-ttu-id="6f9ad-103">Presentatore input penna</span><span class="sxs-lookup"><span data-stu-id="6f9ad-103">Ink presenter</span></span>

<span data-ttu-id="6f9ad-104">Le API Presenter di input penna consentono alle app Microsoft Win32 di gestire l'input, l'elaborazione e il rendering dell'input penna (standard e modificato) tramite un oggetto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) inserito nella struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) dell'app.</span><span class="sxs-lookup"><span data-stu-id="6f9ad-104">The ink presenter APIs enable Microsoft Win32 apps to manage the input, processing, and rendering of ink input (standard and modified) through an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object inserted into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

> [!Note]
>
> <span data-ttu-id="6f9ad-105">L'input input penna standard (suggerimento per la penna o suggerimento/pulsante della gomma) non viene modificato con una convenienza secondaria, ad esempio un pulsante della penna, un pulsante destro del mouse o simile.</span><span class="sxs-lookup"><span data-stu-id="6f9ad-105">Standard ink input (pen tip or eraser tip/button) is not modified with a secondary affordance, such as a pen barrel button, right mouse button, or similar.</span></span>

<span data-ttu-id="6f9ad-106">Le app piattaforma UWP (Universal Windows Platform) (UWP) che usano Extensible Application Markup Language (XAML) forniscono questa funzionalità tramite un controllo [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) insieme a un oggetto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) che si connette alla struttura ad albero visuale [DirectComposition](../directcomp/directcomposition-portal.md) XAML.</span><span class="sxs-lookup"><span data-stu-id="6f9ad-106">Universal Windows Platform (UWP) apps using Extensible Application Markup Language (XAML) provide this functionality through an [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control along with an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object that connects to the XAML [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span> <span data-ttu-id="6f9ad-107">Per informazioni dettagliate, vedere [interazioni di penna e stilo](/windows/uwp/design/input/pen-and-stylus-interactions).</span><span class="sxs-lookup"><span data-stu-id="6f9ad-107">For more detail, see [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions).</span></span>

<span data-ttu-id="6f9ad-108">Il [renderer di input penna](ink-renderer.md) è progettato per essere usato dagli sviluppatori di app di Windows universali interessati a fornire la funzionalità di InkPresenter [**basata su**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)XAML / [](/uwp/api/windows.ui.input.inking.inkpresenter) in app Win32 native.</span><span class="sxs-lookup"><span data-stu-id="6f9ad-108">[Ink renderer](ink-renderer.md) is designed for use by Universal Windows app developers interested in providing XAML-based [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)/[**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) functionality in native Win32 apps.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6f9ad-109">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="6f9ad-109">In this section</span></span>



| <span data-ttu-id="6f9ad-110">Argomento</span><span class="sxs-lookup"><span data-stu-id="6f9ad-110">Topic</span></span>                                                               | <span data-ttu-id="6f9ad-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f9ad-111">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f9ad-112">Classi Presenter di input penna</span><span class="sxs-lookup"><span data-stu-id="6f9ad-112">Ink presenter classes</span></span>](ink-presenter-classes.md)<br/>       | <span data-ttu-id="6f9ad-113">Negli argomenti contenuti in questa sezione vengono fornite le specifiche di riferimento per le classi del Presenter di input penna.</span><span class="sxs-lookup"><span data-stu-id="6f9ad-113">The topics contained in this section provide the reference specifications for Ink presenter classes.</span></span> <br/>    |
| [<span data-ttu-id="6f9ad-114">Interfacce del Presenter di input penna</span><span class="sxs-lookup"><span data-stu-id="6f9ad-114">Ink presenter interfaces</span></span>](ink-presenter-interfaces.md)<br/> | <span data-ttu-id="6f9ad-115">Gli argomenti contenuti in questa sezione forniscono le specifiche di riferimento per le interfacce del Presenter di input penna.</span><span class="sxs-lookup"><span data-stu-id="6f9ad-115">The topics contained in this section provide the reference specifications for Ink presenter interfaces.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="6f9ad-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f9ad-116">Related topics</span></span>

<span data-ttu-id="6f9ad-117">[Relatore input](ink-presenter.md)penna, [interazioni tra penna e stilo](/windows/uwp/design/input/pen-and-stylus-interactions), [esempio di analisi dell'input penna](/samples/microsoft/windows-universal-samples/inkanalysis/), esempio di [Inking semplice](/samples/microsoft/windows-universal-samples/simpleink/), [esempio di Inking complesso](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="6f9ad-117">[Ink presenter](ink-presenter.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
