---
description: L'API Location definisce i tipi di enumerazione seguenti.
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: Strutture e tipi di enumerazione (API Location)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a73c27cb2ad6dc0dcd0c2b92f4e9ba52e98fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314798"
---
# <a name="structures-and-enumeration-types-location-api"></a><span data-ttu-id="8619e-103">Strutture e tipi di enumerazione (API Location)</span><span class="sxs-lookup"><span data-stu-id="8619e-103">Structures and Enumeration Types (Location API)</span></span>

<span data-ttu-id="8619e-104">\[L'API del percorso Win32 è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="8619e-104">\[The Win32 Location API is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8619e-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="8619e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8619e-106">Usare invece l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .</span><span class="sxs-lookup"><span data-stu-id="8619e-106">Instead, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.</span></span> <span data-ttu-id="8619e-107">\]</span><span class="sxs-lookup"><span data-stu-id="8619e-107">\]</span></span>

<span data-ttu-id="8619e-108">L'API Location definisce i tipi di enumerazione seguenti.</span><span class="sxs-lookup"><span data-stu-id="8619e-108">The Location API defines the following enumeration types.</span></span>



| <span data-ttu-id="8619e-109">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="8619e-109">Enumeration</span></span>                                                                       | <span data-ttu-id="8619e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8619e-110">Description</span></span>                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="8619e-111">[**\_ \_ accuratezza posizione desiderata**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8619e-111">[**LOCATION\_DESIRED\_ACCURACY**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span></span>                  | <span data-ttu-id="8619e-112">Definisce i possibili tipi di accuratezza desiderati.</span><span class="sxs-lookup"><span data-stu-id="8619e-112">Defines the possible desired accuracy types.</span></span>                         |
| [<span data-ttu-id="8619e-113">**\_stato rapporto \_ percorso**</span><span class="sxs-lookup"><span data-stu-id="8619e-113">**LOCATION\_REPORT\_STATUS**</span></span>](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | <span data-ttu-id="8619e-114">Definisce lo stato possibile per i nuovi report di un tipo di report specifico.</span><span class="sxs-lookup"><span data-stu-id="8619e-114">Defines possible status for new reports of a particular report type.</span></span> |



 

## <a name="location-constants-from-the-sensor-api"></a><span data-ttu-id="8619e-115">Costanti di posizione dall'API del sensore</span><span class="sxs-lookup"><span data-stu-id="8619e-115">Location Constants from the Sensor API</span></span>

<span data-ttu-id="8619e-116">L'API del sensore definisce anche le chiavi delle proprietà relative alla posizione e le costanti.</span><span class="sxs-lookup"><span data-stu-id="8619e-116">The Sensor API also defines location-related property keys and constants.</span></span> <span data-ttu-id="8619e-117">È possibile utilizzare le chiavi di proprietà definite in sensors. h per recuperare i dati del percorso da un report chiamando [**ILocationReport:: GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).</span><span class="sxs-lookup"><span data-stu-id="8619e-117">The property keys defined in sensors.h can be used to retrieve location data from a report by calling [**ILocationReport::GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).</span></span>

 

 
