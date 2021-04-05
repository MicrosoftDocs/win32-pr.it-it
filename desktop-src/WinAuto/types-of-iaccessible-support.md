---
title: Tipi di supporto di IAccessible
description: Tipi di supporto di IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710687"
---
# <a name="types-of-iaccessible-support"></a><span data-ttu-id="6027b-103">Tipi di supporto di IAccessible</span><span class="sxs-lookup"><span data-stu-id="6027b-103">Types of IAccessible Support</span></span>

<span data-ttu-id="6027b-104">I server Microsoft Active Accessibility hanno due tipi di supporto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : nativo e con proxy.</span><span class="sxs-lookup"><span data-stu-id="6027b-104">Microsoft Active Accessibility servers have two types of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support: native and proxied.</span></span> <span data-ttu-id="6027b-105">Gli elementi dell'interfaccia utente utilizzati in un'applicazione determinano il tipo di supporto appropriato.</span><span class="sxs-lookup"><span data-stu-id="6027b-105">The UI elements used in an application determine which type of support is appropriate.</span></span> <span data-ttu-id="6027b-106">Molti server attualmente scritti sfruttano tutti i vantaggi dei proxy **IAccessible** e implementano solo **IAccessible** per i controlli che non sono inviati tramite proxy da Oleacc.dll, ad esempio controlli o controlli senza finestra con un nome di classe della finestra personalizzata.</span><span class="sxs-lookup"><span data-stu-id="6027b-106">Many servers being written today take full advantage of **IAccessible** proxies and only implement **IAccessible** for those controls that are not proxied by Oleacc.dll, such as windowless controls or controls with a custom window class name.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6027b-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="6027b-107">In this section</span></span>

-   [<span data-ttu-id="6027b-108">Implementazione di Active Accessibility nativa</span><span class="sxs-lookup"><span data-stu-id="6027b-108">Native Active Accessibility Implementation</span></span>](native-active-accessibility-implementation.md)
-   [<span data-ttu-id="6027b-109">Proxy IAccessible</span><span class="sxs-lookup"><span data-stu-id="6027b-109">IAccessible Proxies</span></span>](iaccessible-proxies.md)

 

 




