---
description: Rappresenta un rapporto di Latitudine/Longitudine.
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: Oggetto LocationDisp. DispLatLongReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319027"
---
# <a name="locationdispdisplatlongreport-object"></a><span data-ttu-id="87881-103">Oggetto LocationDisp. DispLatLongReport</span><span class="sxs-lookup"><span data-stu-id="87881-103">LocationDisp.DispLatLongReport object</span></span>

<span data-ttu-id="87881-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="87881-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="87881-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="87881-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="87881-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="87881-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="87881-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="87881-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="87881-108">Rappresenta un rapporto di Latitudine/Longitudine.</span><span class="sxs-lookup"><span data-stu-id="87881-108">Represents a latitude/longitude report.</span></span>

## <a name="members"></a><span data-ttu-id="87881-109">Membri</span><span class="sxs-lookup"><span data-stu-id="87881-109">Members</span></span>

<span data-ttu-id="87881-110">L'oggetto **LocationDisp. DispLatLongReport** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="87881-110">The **LocationDisp.DispLatLongReport** object has these types of members:</span></span>

-   [<span data-ttu-id="87881-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87881-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87881-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87881-112">Properties</span></span>

<span data-ttu-id="87881-113">Le proprietà dell'oggetto **LocationDisp. DispLatLongReport** sono queste.</span><span class="sxs-lookup"><span data-stu-id="87881-113">The **LocationDisp.DispLatLongReport** object has these properties.</span></span>



| <span data-ttu-id="87881-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87881-114">Property</span></span>                                                                         | <span data-ttu-id="87881-115">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="87881-115">Access type</span></span>          | <span data-ttu-id="87881-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87881-116">Description</span></span>                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87881-117">**Altitudine**</span><span class="sxs-lookup"><span data-stu-id="87881-117">**Altitude**</span></span>](locationdisp-displatlongreport-altitude.md)<br/>           | <span data-ttu-id="87881-118">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="87881-118">Read-only</span></span><br/> | <span data-ttu-id="87881-119">Altitudine corrente, in metri.</span><span class="sxs-lookup"><span data-stu-id="87881-119">Current altitude, in meters.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="87881-120">**AltitudeError**</span><span class="sxs-lookup"><span data-stu-id="87881-120">**AltitudeError**</span></span>](locationdisp-displatlongreport-altitudeerror.md)<br/> | <span data-ttu-id="87881-121">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="87881-121">Read-only</span></span><br/> | <span data-ttu-id="87881-122">Errore di altitudine, in metri.</span><span class="sxs-lookup"><span data-stu-id="87881-122">Altitude error, in meters.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="87881-123">**ErrorRadius**</span><span class="sxs-lookup"><span data-stu-id="87881-123">**ErrorRadius**</span></span>](locationdisp-displatlongreport-errorradius.md)<br/>     | <span data-ttu-id="87881-124">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="87881-124">Read-only</span></span><br/> | <span data-ttu-id="87881-125">Distanza tra la posizione indicata, in metri.</span><span class="sxs-lookup"><span data-stu-id="87881-125">A distance from the reported location, in meters.</span></span> <span data-ttu-id="87881-126">In combinazione con la posizione segnalata come origine, questo raggio descrive il cerchio in cui si trova il percorso effettivo proably.</span><span class="sxs-lookup"><span data-stu-id="87881-126">Combined with the reported location as the origin, this radius describes the circle in which the actual location is proably located.</span></span><br/> |
| [<span data-ttu-id="87881-127">**Latitudine**</span><span class="sxs-lookup"><span data-stu-id="87881-127">**Latitude**</span></span>](locationdisp-displatlongreport-latitude.md)<br/>           | <span data-ttu-id="87881-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="87881-128">Read-only</span></span><br/> | <span data-ttu-id="87881-129">Latitudine corrente, in gradi.</span><span class="sxs-lookup"><span data-stu-id="87881-129">Current latitude, in degrees.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="87881-130">**Longitudine**</span><span class="sxs-lookup"><span data-stu-id="87881-130">**Longitude**</span></span>](locationdisp-displatlongreport-longitude.md)<br/>         | <span data-ttu-id="87881-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="87881-131">Read-only</span></span><br/> | <span data-ttu-id="87881-132">Longitudine corrente, in gradi.</span><span class="sxs-lookup"><span data-stu-id="87881-132">Current longitude, in degrees.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="87881-133">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="87881-133">**Timestamp**</span></span>](locationdisp-displatlongreport-timestamp.md)<br/>         | <span data-ttu-id="87881-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="87881-134">Read-only</span></span><br/> | <span data-ttu-id="87881-135">Data e ora in cui è stato generato il report.</span><span class="sxs-lookup"><span data-stu-id="87881-135">The date and time when the report was generated.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="87881-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="87881-136">Remarks</span></span>

<span data-ttu-id="87881-137">È possibile recuperare questo oggetto tramite la proprietà [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) dell'oggetto [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="87881-137">You can retrieve this object through the [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) property of the [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) object.</span></span> <span data-ttu-id="87881-138">È possibile ricevere questo oggetto tramite l'evento [**NewLatLongReport**](newlatlongreport.md) .</span><span class="sxs-lookup"><span data-stu-id="87881-138">You can receive this object through the [**NewLatLongReport**](newlatlongreport.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="87881-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87881-139">Requirements</span></span>



| <span data-ttu-id="87881-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="87881-140">Requirement</span></span> | <span data-ttu-id="87881-141">Valore</span><span class="sxs-lookup"><span data-stu-id="87881-141">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="87881-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87881-142">Minimum supported client</span></span><br/> | <span data-ttu-id="87881-143">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="87881-143">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="87881-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87881-144">Minimum supported server</span></span><br/> | <span data-ttu-id="87881-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="87881-145">None supported</span></span><br/>                  |



 

