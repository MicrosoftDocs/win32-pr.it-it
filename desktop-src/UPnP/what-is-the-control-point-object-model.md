---
title: Informazioni sul modello a oggetti del punto di controllo
description: Nella figura seguente viene illustrato il modello a oggetti del punto di controllo di base.
ms.assetid: 6c5a32a1-932e-4868-b4c6-8701e90a7c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e491d3ec89b1074fb09a9f7632a886fb67b59863
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332444"
---
# <a name="what-is-the-control-point-object-model"></a><span data-ttu-id="350a9-103">Che cos'è il modello a oggetti del punto di controllo?</span><span class="sxs-lookup"><span data-stu-id="350a9-103">What is the Control Point Object Model?</span></span>

<span data-ttu-id="350a9-104">Nella figura seguente viene illustrato il modello a oggetti del punto di controllo di base.</span><span class="sxs-lookup"><span data-stu-id="350a9-104">The following illustration shows the basic Control Point object model.</span></span>

![modello a oggetti del punto di controllo](images/upnp-object-model.png)

<span data-ttu-id="350a9-106">La ricerca di dispositivi con l'interfaccia di ricerca dispositivi crea una raccolta di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="350a9-106">Searching for devices with the Device Finder interface creates a Devices collection.</span></span> <span data-ttu-id="350a9-107">Una raccolta dispositivi contiene zero o più oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="350a9-107">A Devices collection contains zero or more Device objects.</span></span> <span data-ttu-id="350a9-108">Le applicazioni possono usare i vari metodi di raccolta di dispositivi per accedere ai singoli oggetti dispositivo.</span><span class="sxs-lookup"><span data-stu-id="350a9-108">Applications can use the various Devices collection methods to access individual Device objects.</span></span>

<span data-ttu-id="350a9-109">Gli oggetti dispositivo contengono sempre una raccolta di servizi che contiene uno o più oggetti servizio.</span><span class="sxs-lookup"><span data-stu-id="350a9-109">Device objects always contain a Services collection that contains one or more Service objects.</span></span> <span data-ttu-id="350a9-110">Questi oggetti servizio vengono usati dalle applicazioni per comunicare con i dispositivi e controllarli.</span><span class="sxs-lookup"><span data-stu-id="350a9-110">These service objects are used by applications to communicate with and control devices.</span></span>

 

 




