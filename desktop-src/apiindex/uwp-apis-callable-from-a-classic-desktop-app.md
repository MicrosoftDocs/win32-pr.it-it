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
# <a name="winrt-apis-callable-from-a-desktop-app"></a>API WinRT chiamabili da un'app desktop

La [maggior Windows Runtime (WinRT) può](/uwp/api/) essere usata dalle app desktop (.NET e C++native). Tuttavia, alcune classi WinRT sono progettate per e sono supportate solo per l'uso nelle app UWP. Sono inclusi [CoreDispatcher,](/uwp/api/Windows.UI.Core.CoreDispatcher) [CoreWindow,](/uwp/api/Windows.UI.Core.CoreWindow) [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)e alcune classi correlate. Altre classi WinRT funzionano nelle app desktop, ad eccezione di membri specifici.

Per altre informazioni, vedere [Windows Runtime API non supportate nelle app desktop.](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api) Se disponibile, questo articolo suggerisce API alternative per ottenere le stesse funzionalità delle API non supportate.
