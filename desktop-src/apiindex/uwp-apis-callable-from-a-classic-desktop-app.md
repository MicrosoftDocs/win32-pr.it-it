---
description: La regola generale è che un'app desktop può chiamare un'API Windows Runtime (WinRT). Tuttavia, alcune API, incluse le API dell'interfaccia utente XAML, richiedono che l'app chiamante abbia un'identità del pacchetto.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: API WinRT chiamabili da un'app desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f99cca14c066f372ad7fd417e04137a62ae628
ms.sourcegitcommit: 133954d5dbcd5b2b3b50c8efd16cd101278fc1db
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108172483"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a><span data-ttu-id="8c2d6-104">API WinRT chiamabili da un'app desktop</span><span class="sxs-lookup"><span data-stu-id="8c2d6-104">WinRT APIs callable from a desktop app</span></span>

<span data-ttu-id="8c2d6-105">La [maggior Windows Runtime (WinRT) può](/uwp/api/) essere usata dalle app desktop (.NET e C++native).</span><span class="sxs-lookup"><span data-stu-id="8c2d6-105">Most [Windows Runtime (WinRT) APIs](/uwp/api/) can be used by desktop (.NET and native C++) apps.</span></span> <span data-ttu-id="8c2d6-106">Tuttavia, alcune classi WinRT sono progettate per e sono supportate solo per l'uso nelle app UWP.</span><span class="sxs-lookup"><span data-stu-id="8c2d6-106">However, some WinRT classes are designed for and are only supported for use in UWP apps.</span></span> <span data-ttu-id="8c2d6-107">Sono inclusi [CoreDispatcher,](/uwp/api/Windows.UI.Core.CoreDispatcher) [CoreWindow,](/uwp/api/Windows.UI.Core.CoreWindow) [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)e alcune classi correlate.</span><span class="sxs-lookup"><span data-stu-id="8c2d6-107">This includes [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher), [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow), [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview), and some related classes.</span></span> <span data-ttu-id="8c2d6-108">Altre classi WinRT funzionano nelle app desktop, ad eccezione di membri specifici.</span><span class="sxs-lookup"><span data-stu-id="8c2d6-108">Other WinRT classes work in desktop apps except for specific members.</span></span>

<span data-ttu-id="8c2d6-109">Per altre informazioni, vedere [Windows Runtime API non supportate nelle app desktop.](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api)</span><span class="sxs-lookup"><span data-stu-id="8c2d6-109">For more information, see [Windows Runtime APIs not supported in desktop apps](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api).</span></span> <span data-ttu-id="8c2d6-110">Se disponibile, questo articolo suggerisce API alternative per ottenere le stesse funzionalità delle API non supportate.</span><span class="sxs-lookup"><span data-stu-id="8c2d6-110">Where available, this article suggests alternative APIs to achieve the same functionality as the unsupported APIs.</span></span>
