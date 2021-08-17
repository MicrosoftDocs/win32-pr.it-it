---
description: La regola generale è che un'app desktop può chiamare un'API Windows Runtime (WinRT). Tuttavia, alcune API, incluse le API dell'interfaccia utente XAML, richiedono che l'app chiamante abbia un'identità del pacchetto.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: API WinRT chiamabili da un'app desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bbfb2316a6fd4dd8d35d0744acc4ad301dba7f42aee36ee865d67bb2fff805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130303"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a>API WinRT chiamabili da un'app desktop

La [maggior Windows Runtime (WinRT)](/uwp/api/) può essere usata dalle app desktop (.NET e C++native). Tuttavia, alcune classi WinRT sono progettate per e sono supportate solo per l'uso nelle app UWP. Sono inclusi [CoreDispatcher,](/uwp/api/Windows.UI.Core.CoreDispatcher) [CoreWindow,](/uwp/api/Windows.UI.Core.CoreWindow) [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)e alcune classi correlate. Altre classi WinRT funzionano nelle app desktop, ad eccezione di membri specifici.

Per altre informazioni, vedere API Windows runtime non [supportate nelle app desktop.](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api) Se disponibile, questo articolo suggerisce API alternative per ottenere le stesse funzionalità delle API non supportate.
