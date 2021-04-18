---
description: Il modello a oggetti dell'API Location fornisce gli eventi seguenti.
ms.assetid: c7ac0d81-ce36-4991-a0fb-6d3c6cc8efe8
title: Eventi LocationDisp
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 55dae79305547bf4e41ee27c727ab9204eb561cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319026"
---
# <a name="locationdisp-events"></a><span data-ttu-id="7470e-103">Eventi LocationDisp</span><span class="sxs-lookup"><span data-stu-id="7470e-103">LocationDisp Events</span></span>

<span data-ttu-id="7470e-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="7470e-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7470e-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="7470e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7470e-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7470e-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="7470e-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="7470e-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="7470e-108">Il modello a oggetti dell'API Location fornisce gli eventi seguenti.</span><span class="sxs-lookup"><span data-stu-id="7470e-108">The Location API object model provides the following events.</span></span>



| <span data-ttu-id="7470e-109">Event</span><span class="sxs-lookup"><span data-stu-id="7470e-109">Event</span></span>                                                  | <span data-ttu-id="7470e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7470e-110">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="7470e-111">**NewCivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="7470e-111">**NewCivicAddressReport**</span></span>](newcivicaddressreport.md) | <span data-ttu-id="7470e-112">Si verifica quando viene generato un nuovo report sull'indirizzo civico.</span><span class="sxs-lookup"><span data-stu-id="7470e-112">Occurs when a new civic address report is generated.</span></span>      |
| [<span data-ttu-id="7470e-113">**NewLatLongReport**</span><span class="sxs-lookup"><span data-stu-id="7470e-113">**NewLatLongReport**</span></span>](newlatlongreport.md)           | <span data-ttu-id="7470e-114">Si verifica quando viene generato un nuovo report di Latitudine/Longitudine.</span><span class="sxs-lookup"><span data-stu-id="7470e-114">Occurs when a new latitude/longitude report is generated.</span></span> |
| [<span data-ttu-id="7470e-115">**StatusChanged**</span><span class="sxs-lookup"><span data-stu-id="7470e-115">**StatusChanged**</span></span>](statuschanged.md)                 | <span data-ttu-id="7470e-116">Si verifica in seguito alla modifica dello stato operativo di un report.</span><span class="sxs-lookup"><span data-stu-id="7470e-116">Occurs when the operational status of a report changes.</span></span>   |



 

 

 
