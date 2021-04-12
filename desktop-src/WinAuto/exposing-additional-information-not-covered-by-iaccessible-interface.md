---
title: Esposizione di informazioni aggiuntive non coperte dall'interfaccia IAccessible
description: A seconda dei prodotti, gli sviluppatori di server potrebbero dover esporre informazioni o funzionalità oltre al supporto di Microsoft Active Accessibility.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338663"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a><span data-ttu-id="55325-103">Esposizione di informazioni aggiuntive non coperte dall'interfaccia IAccessible</span><span class="sxs-lookup"><span data-stu-id="55325-103">Exposing Additional Information Not Covered by IAccessible Interface</span></span>

<span data-ttu-id="55325-104">A seconda dei prodotti, gli sviluppatori di server potrebbero dover esporre informazioni o funzionalità oltre al supporto di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="55325-104">Depending on their products, server developers might need to expose information or functionality in addition to Microsoft Active Accessibility support.</span></span> <span data-ttu-id="55325-105">In tal caso, collaborare con i fornitori di Assistive Technology (client) per assicurarsi che aggiungano il supporto per le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="55325-105">If this is the case, work with assistive technology vendors (clients) to ensure that they add support for the features.</span></span>

<span data-ttu-id="55325-106">Non tentare di estendere l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="55325-106">Do not attempt to extend the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="55325-107">Non è possibile modificare le interfacce una volta pubblicate.</span><span class="sxs-lookup"><span data-stu-id="55325-107">Interfaces cannot be changed once they are published.</span></span> <span data-ttu-id="55325-108">Per esporre informazioni aggiuntive, utilizzare un'interfaccia personalizzata ed esporla utilizzando una delle tecniche seguenti:</span><span class="sxs-lookup"><span data-stu-id="55325-108">To expose additional information, use a custom interface and expose it by using one of the following techniques:</span></span>

-   [<span data-ttu-id="55325-109">Uso \_ di ObjID NATIVEOM per esporre un'interfaccia del modello a oggetti nativa per una finestra</span><span class="sxs-lookup"><span data-stu-id="55325-109">Using OBJID\_NATIVEOM to expose a native object model interface for a window</span></span>](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [<span data-ttu-id="55325-110">Utilizzo di QueryService per esporre un'interfaccia del modello a oggetti nativo per un oggetto IAccessible</span><span class="sxs-lookup"><span data-stu-id="55325-110">Using QueryService to expose a native object model interface for an IAccessible object</span></span>](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

<span data-ttu-id="55325-111">Si noti che l'obiettivo dell'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) è disporre di un'interfaccia ben definita utilizzata da server e client.</span><span class="sxs-lookup"><span data-stu-id="55325-111">Note that the goal of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is to have a well-defined interface that is used by servers and clients.</span></span> <span data-ttu-id="55325-112">Prima di esporre interfacce personalizzate, assicurarsi di esporre quante più informazioni possibile tramite **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="55325-112">Before exposing custom interfaces, be sure to expose as much information as possible through **IAccessible**.</span></span>

<span data-ttu-id="55325-113">Non è possibile utilizzare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per esporre interfacce personalizzate.</span><span class="sxs-lookup"><span data-stu-id="55325-113">You cannot use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to expose custom interfaces.</span></span> <span data-ttu-id="55325-114">Usare **IServiceProvider:: QueryService** come descritto nelle procedure seguenti.</span><span class="sxs-lookup"><span data-stu-id="55325-114">Use **IServiceProvider::QueryService** as outlined in the following procedures.</span></span>

 

 