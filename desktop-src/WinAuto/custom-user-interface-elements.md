---
title: Elementi dell'interfaccia utente personalizzati
description: Gli sviluppatori di server progettano oggetti accessibili in base all'interfaccia utente di un'applicazione.
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32a086b977a1737a17206261aaaa94faa754d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855649"
---
# <a name="custom-user-interface-elements"></a><span data-ttu-id="36409-103">Elementi dell'interfaccia utente personalizzati</span><span class="sxs-lookup"><span data-stu-id="36409-103">Custom User Interface Elements</span></span>

<span data-ttu-id="36409-104">Gli sviluppatori di server progettano oggetti accessibili in base all'interfaccia utente di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="36409-104">Server developers design accessible objects based on an application's UI.</span></span> <span data-ttu-id="36409-105">Poiché [Active Accessibility implementa l'interfaccia IAccessible per conto degli elementi dell'interfaccia utente forniti dal sistema](appendix-a--supported-user-interface-elements-reference.md) , ad esempio caselle di riepilogo, menu e controlli TrackBar, è necessario implementare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) solo per i tipi seguenti di elementi dell'interfaccia utente personalizzati:</span><span class="sxs-lookup"><span data-stu-id="36409-105">Because [Active Accessibility implements the IAccessible interface on behalf of system-provided user interface elements](appendix-a--supported-user-interface-elements-reference.md) such as list boxes, menus, and trackbar controls, you need to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface only for the following kinds of custom UI elements:</span></span>

-   <span data-ttu-id="36409-106">Controlli personalizzati creati mediante la registrazione di una classe di finestra definita dall'applicazione</span><span class="sxs-lookup"><span data-stu-id="36409-106">Custom controls created by registering an application-defined window class</span></span>
-   <span data-ttu-id="36409-107">Controlli personalizzati disegnati direttamente sullo schermo a cui non è associato un **HWND**</span><span class="sxs-lookup"><span data-stu-id="36409-107">Custom controls drawn directly on the screen that do not have an associated **HWND**</span></span>
-   <span data-ttu-id="36409-108">Controlli personalizzati, ad esempio i controlli Microsoft ActiveX e Java</span><span class="sxs-lookup"><span data-stu-id="36409-108">Custom controls such as Microsoft ActiveX and Java controls</span></span>
-   <span data-ttu-id="36409-109">Controlli o oggetti nella finestra del client dell'applicazione che non sono già esposti</span><span class="sxs-lookup"><span data-stu-id="36409-109">Controls or objects in the application's client window that aren't already exposed</span></span>

<span data-ttu-id="36409-110">I menu e i controlli creati dal proprietario sono accessibili purché si seguano le linee guida descritte in [collegamenti per esporre gli elementi personalizzati dell'interfaccia utente](shortcuts-for-exposing-custom-user-interface-elements.md).</span><span class="sxs-lookup"><span data-stu-id="36409-110">Owner-drawn controls and menus are accessible as long as you follow the guidelines discussed in [Shortcuts for Exposing Custom User Interface Elements](shortcuts-for-exposing-custom-user-interface-elements.md).</span></span> <span data-ttu-id="36409-111">Se si seguono queste linee guida, non è necessario implementare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per i controlli e i menu creati dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="36409-111">If you follow these guidelines, then you do not need to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for owner-drawn controls and menus.</span></span>

<span data-ttu-id="36409-112">Nella maggior parte dei casi, i controlli sottoclassati e sottoclassati sono accessibili perché il sistema gestisce la funzionalità di base del controllo.</span><span class="sxs-lookup"><span data-stu-id="36409-112">In most cases, superclassed and subclassed controls are accessible because the system handles the basic functionality of the control.</span></span> <span data-ttu-id="36409-113">Tuttavia, se un controllo sottoclassato o sottoclassato modifica in modo significativo il comportamento del controllo fornito dal sistema su cui si basa, è necessario implementare l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="36409-113">However, if a superclassed or subclassed control significantly modifies the behavior of the system-provided control on which it is based, then you must implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="36409-114">Per altre informazioni, vedere [esposizione di controlli in base ai controlli di sistema](exposing-controls-based-on-system-controls.md).</span><span class="sxs-lookup"><span data-stu-id="36409-114">For more information, see [Exposing Controls Based on System Controls](exposing-controls-based-on-system-controls.md).</span></span>

<span data-ttu-id="36409-115">Se in un'applicazione vengono utilizzati solo elementi dell'interfaccia utente forniti dal sistema, non è necessario implementare [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), ad eccezione della relativa finestra client.</span><span class="sxs-lookup"><span data-stu-id="36409-115">If an application uses only system-provided user interface elements, then it does not need to implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), except for its client window.</span></span> <span data-ttu-id="36409-116">Ad esempio, un'applicazione che include un editor di testo, non implementato utilizzando un controllo di modifica, espone righe di testo come oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="36409-116">For example, an application that includes a text editor, not implemented using an edit control, exposes lines of text as accessible objects.</span></span> <span data-ttu-id="36409-117">Si noti che Microsoft Active Accessibility espone automaticamente il testo nei controlli Edit e Rich Edit come una singola stringa di testo nella proprietà [**value**](value-property.md) del controllo.</span><span class="sxs-lookup"><span data-stu-id="36409-117">Note that Microsoft Active Accessibility automatically exposes the text in edit and rich edit controls as a single string of text in the [**Value**](value-property.md) property of the control.</span></span>

 

 




