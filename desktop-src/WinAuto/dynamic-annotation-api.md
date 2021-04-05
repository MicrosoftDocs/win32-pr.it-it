---
title: API di annotazione dinamica
description: L'API di annotazione dinamica è un'estensione di Microsoft Active Accessibility che consente agli sviluppatori di personalizzare il supporto di IAccessible esistente senza dover utilizzare tecniche di sottoclasse o di wrapping soggette a errori.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955844"
---
# <a name="dynamic-annotation-api"></a><span data-ttu-id="92ed6-103">API di annotazione dinamica</span><span class="sxs-lookup"><span data-stu-id="92ed6-103">Dynamic Annotation API</span></span>

<span data-ttu-id="92ed6-104">L'API di annotazione dinamica è un'estensione di Microsoft Active Accessibility che consente agli sviluppatori di personalizzare il supporto di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) esistente senza dover utilizzare tecniche di sottoclasse o di wrapping soggette a errori.</span><span class="sxs-lookup"><span data-stu-id="92ed6-104">The Dynamic Annotation API is an extension to Microsoft Active Accessibility that allows developers to customize existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support without having to use error-prone subclassing or wrapping techniques.</span></span> <span data-ttu-id="92ed6-105">Questo meccanismo consente inoltre agli sviluppatori di passare suggerimenti o altre informazioni utili ai proxy Oleacc.dll.</span><span class="sxs-lookup"><span data-stu-id="92ed6-105">This mechanism also allows developers to pass hints or other useful information to the Oleacc.dll proxies.</span></span>

<span data-ttu-id="92ed6-106">L'annotazione dinamica viene in genere usata per correggere o modificare un'istanza non corretta di un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) esposto da un proxy di Oleacc.dll esistente.</span><span class="sxs-lookup"><span data-stu-id="92ed6-106">Dynamic Annotation is typically used to correct or amend an inaccurate instance of an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object exposed by an existing Oleacc.dll proxy.</span></span> <span data-ttu-id="92ed6-107">Ad esempio, è possibile usarlo per eseguire l'override delle proprietà [**Name**](name-property.md) e [**Role**](role-property.md) fornite dal proxy predefinito e per fornire la [**Descrizione**](description-property.md) e le proprietà della [**Guida**](help-property.md) (che potrebbero non essere fornite dal proxy predefinito).</span><span class="sxs-lookup"><span data-stu-id="92ed6-107">For example, you can use it to override the [**Name**](name-property.md) and [**Role**](role-property.md) properties provided by the default proxy, and to supply [**Description**](description-property.md) and [**Help**](help-property.md) properties (which may not be provided by the default proxy).</span></span>

<span data-ttu-id="92ed6-108">Con Windows 7, gli sviluppatori possono usare l'API di annotazione dinamica per annotare le proprietà di automazione interfaccia utente Microsoft, nonché le proprietà di Microsoft Active Accessibility degli oggetti proxy creati da Oleacc.dll per i controlli Windows standard.</span><span class="sxs-lookup"><span data-stu-id="92ed6-108">With Windows 7, developers can use the Dynamic Annotation API to annotate Microsoft UI Automation properties as well as Microsoft Active Accessibility properties of the proxy objects that Oleacc.dll creates for standard Windows controls.</span></span> <span data-ttu-id="92ed6-109">Gli oggetti proxy Oleacc.dll servono sia Microsoft Active Accessibility che client di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="92ed6-109">The Oleacc.dll proxy objects serve both Microsoft Active Accessibility and UI Automation clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="92ed6-110">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="92ed6-110">In this section</span></span>

-   [<span data-ttu-id="92ed6-111">Informazioni di base</span><span class="sxs-lookup"><span data-stu-id="92ed6-111">Background Information</span></span>](background-information.md)
-   [<span data-ttu-id="92ed6-112">Alternative all'annotazione dinamica</span><span class="sxs-lookup"><span data-stu-id="92ed6-112">Alternatives to Dynamic Annotation</span></span>](alternatives-to-dynamic-annotation.md)
-   [<span data-ttu-id="92ed6-113">Tipi di annotazione dinamica</span><span class="sxs-lookup"><span data-stu-id="92ed6-113">Types of Dynamic Annotation</span></span>](types-of-dynamic-annotation.md)
-   [<span data-ttu-id="92ed6-114">Annotazione diretta</span><span class="sxs-lookup"><span data-stu-id="92ed6-114">Direct Annotation</span></span>](direct-annotation.md)
-   [<span data-ttu-id="92ed6-115">Annotazione mappa valori</span><span class="sxs-lookup"><span data-stu-id="92ed6-115">Value Map Annotation</span></span>](value-map-annotation.md)
-   [<span data-ttu-id="92ed6-116">Annotazione server</span><span class="sxs-lookup"><span data-stu-id="92ed6-116">Server Annotation</span></span>](server-annotation.md)
-   [<span data-ttu-id="92ed6-117">Problemi e limitazioni</span><span class="sxs-lookup"><span data-stu-id="92ed6-117">Issues and Limitations</span></span>](issues-and-limitations.md)

 

 




