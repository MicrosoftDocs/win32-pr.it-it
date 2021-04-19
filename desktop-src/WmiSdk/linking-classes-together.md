---
description: I provider WMI sono in genere progettati per fornire informazioni su un oggetto gestito specifico in un singolo computer.
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: Collegamento di classi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317551"
---
# <a name="linking-classes-together"></a><span data-ttu-id="2bc76-103">Collegamento di classi</span><span class="sxs-lookup"><span data-stu-id="2bc76-103">Linking Classes Together</span></span>

<span data-ttu-id="2bc76-104">I provider WMI sono in genere progettati per fornire informazioni su un oggetto gestito specifico in un singolo computer.</span><span class="sxs-lookup"><span data-stu-id="2bc76-104">WMI providers are usually designed to provide information about a specific managed object on a single computer.</span></span> <span data-ttu-id="2bc76-105">Se è presente una proprietà comune che può fungere da chiave per identificare in modo univoco tutte le istanze di origine diverse, utilizzare il [provider di visualizzazione](view-provider.md) per combinare le proprietà di classi, spazi dei nomi o computer diversi in una singola classe.</span><span class="sxs-lookup"><span data-stu-id="2bc76-105">If there is a common property that can serve as a key to uniquely identify all the different source instances, then use the [View Provider](view-provider.md) to combine properties from different classes, namespaces, or computers into a single class.</span></span>

<span data-ttu-id="2bc76-106">È necessario prima [registrare il provider di visualizzazione](registering-the-view-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2bc76-106">You must first [register the View Provider](registering-the-view-provider.md).</span></span> <span data-ttu-id="2bc76-107">Dopo la registrazione, è possibile creare i seguenti tipi di classi di visualizzazione:</span><span class="sxs-lookup"><span data-stu-id="2bc76-107">After registration, you can create the following types of view classes:</span></span>

-   [<span data-ttu-id="2bc76-108">Visualizzazione join</span><span class="sxs-lookup"><span data-stu-id="2bc76-108">Join view</span></span>](creating-a-new-instance-from-old-properties.md)

    <span data-ttu-id="2bc76-109">Istanze di classi diverse connesse da un valore di proprietà comune.</span><span class="sxs-lookup"><span data-stu-id="2bc76-109">Instances of different classes connected by a common property value.</span></span>

-   [<span data-ttu-id="2bc76-110">Visualizzazione associazione</span><span class="sxs-lookup"><span data-stu-id="2bc76-110">Association view</span></span>](associating-instances-between-namespaces.md)

    <span data-ttu-id="2bc76-111">Viste delle classi di associazione esistenti attraverso il limite dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="2bc76-111">Views of existing association classes across the namespace boundary.</span></span>

-   [<span data-ttu-id="2bc76-112">Visualizzazione Unione</span><span class="sxs-lookup"><span data-stu-id="2bc76-112">Union view</span></span>](creating-a-union-view-class.md)

    <span data-ttu-id="2bc76-113">Unione di una o più istanze.</span><span class="sxs-lookup"><span data-stu-id="2bc76-113">Union of one or more instances.</span></span>

 

 



