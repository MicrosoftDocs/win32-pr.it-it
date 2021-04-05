---
title: Creazione di oggetti proxy
description: Oltre a progettare classi che implementano proprietà e metodi IAccessible, gli sviluppatori di server possono anche progettare oggetti proxy che monitorano la durata degli oggetti accessibili.
ms.assetid: d140206a-9918-438b-96bd-df141da2f04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e005af4f02430376bc013a45c68cdecef8c0feba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708554"
---
# <a name="creating-proxy-objects"></a><span data-ttu-id="9b339-103">Creazione di oggetti proxy</span><span class="sxs-lookup"><span data-stu-id="9b339-103">Creating Proxy Objects</span></span>

<span data-ttu-id="9b339-104">Oltre a progettare classi che implementano proprietà e metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , gli sviluppatori di server possono anche progettare oggetti *proxy* che monitorano la durata degli oggetti accessibili.</span><span class="sxs-lookup"><span data-stu-id="9b339-104">In addition to designing classes that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods, server developers may also need to design *proxy* objects that monitor the life span of accessible objects.</span></span> <span data-ttu-id="9b339-105">Se un oggetto accessibile in un'applicazione è disponibile per tutto il tempo in cui l'applicazione è in esecuzione, non è necessario creare un oggetto proxy.</span><span class="sxs-lookup"><span data-stu-id="9b339-105">If an accessible object in an application is available the entire time the application is running, then you do not need to create a proxy object.</span></span> <span data-ttu-id="9b339-106">Se è possibile eliminare l'oggetto accessibile mentre l'applicazione è in esecuzione, è necessario creare un oggetto proxy.</span><span class="sxs-lookup"><span data-stu-id="9b339-106">If it is possible to destroy the accessible object while the application is running, then you must create a proxy object.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b339-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="9b339-107">In this section</span></span>

-   [<span data-ttu-id="9b339-108">Che cosa sono gli oggetti proxy?</span><span class="sxs-lookup"><span data-stu-id="9b339-108">What Are Proxy Objects?</span></span>](what-are-proxy-objects.md)
-   [<span data-ttu-id="9b339-109">Perché gli oggetti proxy sono necessari</span><span class="sxs-lookup"><span data-stu-id="9b339-109">Why Proxy Objects Are Needed</span></span>](why-proxy-objects-are-needed.md)
-   [<span data-ttu-id="9b339-110">Considerazioni di progettazione per gli oggetti proxy</span><span class="sxs-lookup"><span data-stu-id="9b339-110">Design Considerations for Proxy Objects</span></span>](design-considerations-for-proxy-objects.md)

 

 




