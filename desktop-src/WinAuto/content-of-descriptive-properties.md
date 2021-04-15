---
title: Contenuto delle proprietà descrittive
description: L'interfaccia IAccessible fornisce proprietà descrittive che descrivono i vari aspetti di un oggetto.
ms.assetid: e6c1d1a3-417d-4aea-abac-f84a55f666b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271dc920034802b87afd4c76ab7ede6bb9476d99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515799"
---
# <a name="content-of-descriptive-properties"></a><span data-ttu-id="6fc21-103">Contenuto delle proprietà descrittive</span><span class="sxs-lookup"><span data-stu-id="6fc21-103">Content of Descriptive Properties</span></span>

<span data-ttu-id="6fc21-104">L'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fornisce proprietà descrittive che descrivono i vari aspetti di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="6fc21-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface provides descriptive properties, which describe various aspects of an object.</span></span> <span data-ttu-id="6fc21-105">Alcune di queste proprietà sono specifiche del contenuto; altre proprietà includono contenuto costituito da testo descrittivo fornito dal server.</span><span class="sxs-lookup"><span data-stu-id="6fc21-105">Some of these properties are content specific; other properties have content consisting of descriptive text that is provided by the server.</span></span> <span data-ttu-id="6fc21-106">Il tipo di informazioni per ogni proprietà varia a seconda dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6fc21-106">The type of information for each property varies depending on the object.</span></span>

<span data-ttu-id="6fc21-107">Negli argomenti seguenti vengono descritte le informazioni ottenute dai client da queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6fc21-107">The following topics describe information that clients obtain from these properties.</span></span> <span data-ttu-id="6fc21-108">Forniscono inoltre ai server suggerimenti per la scelta del contenuto.</span><span class="sxs-lookup"><span data-stu-id="6fc21-108">They also provide servers with suggestions for choosing content.</span></span>

-   [<span data-ttu-id="6fc21-109">Proprietà Name</span><span class="sxs-lookup"><span data-stu-id="6fc21-109">Name Property</span></span>](name-property.md)
-   [<span data-ttu-id="6fc21-110">Proprietà Role</span><span class="sxs-lookup"><span data-stu-id="6fc21-110">Role Property</span></span>](role-property.md)
-   [<span data-ttu-id="6fc21-111">Proprietà State</span><span class="sxs-lookup"><span data-stu-id="6fc21-111">State Property</span></span>](state-property.md)
-   [<span data-ttu-id="6fc21-112">Proprietà Value</span><span class="sxs-lookup"><span data-stu-id="6fc21-112">Value Property</span></span>](value-property.md)
-   [<span data-ttu-id="6fc21-113">Proprietà Description</span><span class="sxs-lookup"><span data-stu-id="6fc21-113">Description Property</span></span>](description-property.md)
-   [<span data-ttu-id="6fc21-114">Proprietà della Guida</span><span class="sxs-lookup"><span data-stu-id="6fc21-114">Help Property</span></span>](help-property.md)
-   [<span data-ttu-id="6fc21-115">Proprietà HelpTopic</span><span class="sxs-lookup"><span data-stu-id="6fc21-115">HelpTopic Property</span></span>](helptopic-property.md)
-   [<span data-ttu-id="6fc21-116">Proprietà KeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="6fc21-116">KeyboardShortcut Property</span></span>](keyboardshortcut-property.md)
-   [<span data-ttu-id="6fc21-117">Proprietà DefaultAction</span><span class="sxs-lookup"><span data-stu-id="6fc21-117">DefaultAction Property</span></span>](defaultaction-property.md)

<span data-ttu-id="6fc21-118">Quando si progettano oggetti accessibili, è necessario che gli sviluppatori di server facciano riferimento anche agli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="6fc21-118">When designing accessible objects, server developers should also refer to the following topics:</span></span>

-   [<span data-ttu-id="6fc21-119">Scelta delle proprietà da supportare</span><span class="sxs-lookup"><span data-stu-id="6fc21-119">Choosing Which Properties to Support</span></span>](choosing-which-properties-to-support.md)
-   [<span data-ttu-id="6fc21-120">Scelta del contenuto per le proprietà descrittive</span><span class="sxs-lookup"><span data-stu-id="6fc21-120">Choosing the Content for Descriptive Properties</span></span>](choosing-the-content-for-descriptive-properties.md)

<span data-ttu-id="6fc21-121">Per informazioni sui parametri e sui valori restituiti di queste proprietà, vedere la sezione [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del riferimento a Microsoft Active Accessibility [C/C++](c-c---reference.md).</span><span class="sxs-lookup"><span data-stu-id="6fc21-121">For information about the parameters and return values of these properties, see the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) section of the Microsoft Active Accessibility[C/C++ Reference](c-c---reference.md).</span></span>

 

 




