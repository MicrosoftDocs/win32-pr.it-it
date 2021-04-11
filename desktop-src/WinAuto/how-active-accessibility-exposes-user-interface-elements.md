---
title: Come Active Accessibility espone gli elementi dell'interfaccia utente
description: Microsoft Active Accessibility crea un oggetto proxy per ogni elemento dell'interfaccia utente esposto.
ms.assetid: 64aa8fac-cea7-4466-ae34-2760956c296b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b450ebe79aa467100fe9b6fb3bc4cdfb5540b60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221417"
---
# <a name="how-active-accessibility-exposes-user-interface-elements"></a><span data-ttu-id="00c35-103">Come Active Accessibility espone gli elementi dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="00c35-103">How Active Accessibility Exposes User Interface Elements</span></span>

<span data-ttu-id="00c35-104">Microsoft Active Accessibility crea un oggetto *proxy* per ogni elemento dell'interfaccia utente esposto.</span><span class="sxs-lookup"><span data-stu-id="00c35-104">Microsoft Active Accessibility creates a *proxy* object for each user interface element that it exposes.</span></span> <span data-ttu-id="00c35-105">Un oggetto proxy funge da intermediario tra l'utilità client e l'elemento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="00c35-105">A proxy object acts as an intermediary between the client utility and the UI element.</span></span> <span data-ttu-id="00c35-106">Lo scopo dell'oggetto proxy consiste nel monitorare il ciclo di vita dell'elemento dell'interfaccia utente e implementare le proprietà e i metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per conto dell'elemento dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="00c35-106">The purpose of the proxy object is to monitor the life span of the UI element and to implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods on behalf of the UI element.</span></span> <span data-ttu-id="00c35-107">Gli sviluppatori di server che creano controlli personalizzati o altri elementi dell'interfaccia utente personalizzati devono anche creare oggetti proxy.</span><span class="sxs-lookup"><span data-stu-id="00c35-107">Server developers who create custom controls or other custom UI elements should also create proxy objects.</span></span> <span data-ttu-id="00c35-108">Per ulteriori informazioni, vedere [creazione di oggetti proxy](creating-proxy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="00c35-108">For more information, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

<span data-ttu-id="00c35-109">Quando Microsoft Active Accessibility crea un oggetto per esporre un controllo comune o predefinito, crea effettivamente almeno due oggetti: uno per il controllo e uno per la finestra che racchiude il controllo.</span><span class="sxs-lookup"><span data-stu-id="00c35-109">When Microsoft Active Accessibility creates an object to expose a predefined or common control, it actually creates at least two objects: one for the control and one for the window that surrounds the control.</span></span> <span data-ttu-id="00c35-110">Nella maggior parte dei casi, queste finestre padre hanno la [Proprietà Role](role-property.md) della [**\_ \_ finestra del sistema dei ruoli**](object-roles.md) e hanno la stessa [proprietà Name](name-property.md) e il nome della classe di finestra del controllo.</span><span class="sxs-lookup"><span data-stu-id="00c35-110">In most cases, these parent windows have the [Role property](role-property.md) of [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) and have the same [Name property](name-property.md) and window class name as the control.</span></span> <span data-ttu-id="00c35-111">Le informazioni sul controllo che i client comunicano agli utenti finali sono contenute nell'oggetto creato da Microsoft Active Accessibility per esporre il controllo, non l'oggetto padre che espone la finestra che racchiude il controllo.</span><span class="sxs-lookup"><span data-stu-id="00c35-111">The information about the control that clients convey to end users is contained in the object that Microsoft Active Accessibility creates to expose the control, not the parent object that exposes the window that surrounds the control.</span></span>

<span data-ttu-id="00c35-112">Per ulteriori informazioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="00c35-112">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="00c35-113">Selezione di oggetti non necessari</span><span class="sxs-lookup"><span data-stu-id="00c35-113">Screening Out Unnecessary Objects</span></span>](screening-out-unnecessary-objects.md)
-   [<span data-ttu-id="00c35-114">Specifica della proprietà Name</span><span class="sxs-lookup"><span data-stu-id="00c35-114">Providing the Name Property</span></span>](providing-the-name-property.md)
-   [<span data-ttu-id="00c35-115">Verifica della corretta denominazione degli elementi dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="00c35-115">Ensuring that UI Elements are Correctly Named</span></span>](ensure-that-ui-elements-are-named-correctly.md)
-   [<span data-ttu-id="00c35-116">Elementi dell'interfaccia utente non supportati</span><span class="sxs-lookup"><span data-stu-id="00c35-116">Unsupported User Interface Elements</span></span>](unsupported-user-interface-elements.md)

 

 




