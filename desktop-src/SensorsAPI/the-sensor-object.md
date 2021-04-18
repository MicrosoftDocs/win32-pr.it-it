---
description: L'oggetto Sensor rappresenta un sensore specifico.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: Oggetto Sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314666"
---
# <a name="the-sensor-object"></a><span data-ttu-id="e22cf-103">Oggetto Sensor</span><span class="sxs-lookup"><span data-stu-id="e22cf-103">The Sensor Object</span></span>

<span data-ttu-id="e22cf-104">L'oggetto Sensor rappresenta un sensore specifico.</span><span class="sxs-lookup"><span data-stu-id="e22cf-104">The sensor object represents a particular sensor.</span></span>

<span data-ttu-id="e22cf-105">L'API del sensore rappresenta ogni sensore come oggetto sensore.</span><span class="sxs-lookup"><span data-stu-id="e22cf-105">The Sensor API represents each sensor as a sensor object.</span></span> <span data-ttu-id="e22cf-106">È possibile utilizzare un determinato oggetto sensore tramite l'interfaccia [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) .</span><span class="sxs-lookup"><span data-stu-id="e22cf-106">You can work with a particular sensor object through its [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) interface.</span></span> <span data-ttu-id="e22cf-107">Questa interfaccia consente di:</span><span class="sxs-lookup"><span data-stu-id="e22cf-107">This interface enables you to:</span></span>

-   <span data-ttu-id="e22cf-108">Recuperare i metadati relativi al sensore, ad esempio l'ID, il tipo o il nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="e22cf-108">Retrieve metadata about the sensor, such as its ID, type, or friendly name.</span></span>
-   <span data-ttu-id="e22cf-109">Recuperare informazioni sui dati specifici che possono essere forniti dal sensore.</span><span class="sxs-lookup"><span data-stu-id="e22cf-109">Retrieve information about the specific data the sensor can provide.</span></span>
-   <span data-ttu-id="e22cf-110">Recuperare i dati in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="e22cf-110">Retrieve the data, synchronously.</span></span>
-   <span data-ttu-id="e22cf-111">Recuperare le informazioni sullo stato, ad esempio se il sensore è pronto.</span><span class="sxs-lookup"><span data-stu-id="e22cf-111">Retrieve state information, such as whether the sensor is ready.</span></span>
-   <span data-ttu-id="e22cf-112">Consente di specificare gli eventi che il programma riceverà.</span><span class="sxs-lookup"><span data-stu-id="e22cf-112">Specify which events your program will receive.</span></span>
-   <span data-ttu-id="e22cf-113">Specificare l'interfaccia di callback che l'API del sensore può usare per fornire al programma notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="e22cf-113">Specify the callback interface that the Sensor API can use to provide your program with event notifications.</span></span>

 

 



