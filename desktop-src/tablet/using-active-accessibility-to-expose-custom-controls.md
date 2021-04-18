---
description: Descrizione dell'utilizzo di Active Accessibility per esporre i controlli personalizzati per il Tablet PC.
ms.assetid: 1557bde2-c382-4259-ae0c-a70902fa91bd
title: Uso di Active Accessibility per esporre controlli personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d33d4c2b57a881cfbdc15f14e71e339ed7f9e84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306724"
---
# <a name="using-active-accessibility-to-expose-custom-controls"></a><span data-ttu-id="ed713-103">Uso di Active Accessibility per esporre controlli personalizzati</span><span class="sxs-lookup"><span data-stu-id="ed713-103">Using Active Accessibility to Expose Custom Controls</span></span>

<span data-ttu-id="ed713-104">È possibile usare Microsoft Active Accessibility come metodo efficace per rendere i controlli personalizzati compatibili con gli strumenti per l'accessibilità.</span><span class="sxs-lookup"><span data-stu-id="ed713-104">You can use Microsoft Active Accessibility as an effective way to make custom controls compatible with accessibility aids.</span></span> <span data-ttu-id="ed713-105">Active Accessibility richiede che l'applicazione:</span><span class="sxs-lookup"><span data-stu-id="ed713-105">Active Accessibility requires that the application:</span></span>

-   <span data-ttu-id="ed713-106">Creare oggetti Component Object Model (COM) che rappresentano singoli controlli o gruppi di controlli personalizzati che supportano correttamente l'interfaccia **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="ed713-106">Create Component Object Model (COM) objects that represent individual custom controls or groups of controls that properly support the **IAccessible** interface.</span></span> <span data-ttu-id="ed713-107">(L'oggetto può essere creato su richiesta quando viene richiesto da un client di Active Accessibility).</span><span class="sxs-lookup"><span data-stu-id="ed713-107">(The object may be created on demand when it is requested by an Active Accessibility client.)</span></span>
-   <span data-ttu-id="ed713-108">Chiamare [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) quando i controlli vengono creati o eliminati, ottenere o perdere lo stato attivo o modificare lo stato in altro modo.</span><span class="sxs-lookup"><span data-stu-id="ed713-108">Call [**NotifyWinEvent**](/windows/win32/api/winuser/nf-winuser-notifywinevent) when the controls are created or destroyed, gain or lose focus, or otherwise change state.</span></span>
-   <span data-ttu-id="ed713-109">Gestire il \_ messaggio WM GetObject quando viene usato per eseguire query sulle proprietà dell'oggetto o degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="ed713-109">Handle the WM\_GETOBJECT message when used to query properties of the object or objects.</span></span>

<span data-ttu-id="ed713-110">Ai fini di questa discussione, è necessario esporre una finestra contenente altri oggetti personalizzati anche a Active Accessibility, consentendo al client di individuare e spostarsi sugli oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="ed713-110">For the purposes of this discussion, a window containing other custom objects also needs to be exposed to Active Accessibility, allowing the client to discover and navigate to the child objects.</span></span> <span data-ttu-id="ed713-111">Per altre informazioni su come rendere i controlli personalizzati compatibili con gli strumenti di accessibilità, vedere [accessibilità](../accessibility/accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="ed713-111">For more information about how to make custom controls compatible with accessibility aids, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
