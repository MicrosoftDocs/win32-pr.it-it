---
description: Altitudine corrente, in metri. L'altitudine è relativa all'ellissoide di riferimento.
ms.assetid: fbe9984c-aa9d-4ce0-9f8b-d79ca06764d4
title: LocationDisp. DispLatLongReport. Altitude (proprietà)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Altitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2004c8df6c61fb890bf8f71fb3c2b5446d71d79a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882122"
---
# <a name="locationdispdisplatlongreportaltitude-property"></a><span data-ttu-id="5abfe-104">LocationDisp. DispLatLongReport. Altitude (proprietà)</span><span class="sxs-lookup"><span data-stu-id="5abfe-104">LocationDisp.DispLatLongReport.Altitude property</span></span>

<span data-ttu-id="5abfe-105">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="5abfe-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5abfe-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="5abfe-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="5abfe-107">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5abfe-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="5abfe-108">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="5abfe-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="5abfe-109">Altitudine corrente, in metri.</span><span class="sxs-lookup"><span data-stu-id="5abfe-109">Current altitude, in meters.</span></span> <span data-ttu-id="5abfe-110">L'altitudine è relativa all'ellissoide di riferimento.</span><span class="sxs-lookup"><span data-stu-id="5abfe-110">Altitude is relative to the reference ellipsoid.</span></span>

<span data-ttu-id="5abfe-111">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5abfe-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5abfe-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5abfe-112">Syntax</span></span>


```JScript
Altitude = LocationDisp.DispLatLongReport.Altitude
```



## <a name="property-value"></a><span data-ttu-id="5abfe-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5abfe-113">Property value</span></span>

<span data-ttu-id="5abfe-114">Questa proprietà è un **numero** di sola lettura (virgola mobile a precisione doppia).</span><span class="sxs-lookup"><span data-stu-id="5abfe-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="5abfe-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5abfe-115">Remarks</span></span>

<span data-ttu-id="5abfe-116">Non è necessario che i sensori di posizione forniscano questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5abfe-116">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="5abfe-117">È necessario gestire le eccezioni quando si tenta di accedere a questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5abfe-117">You should handle exceptions when attempting to access this property.</span></span>

<span data-ttu-id="5abfe-118">Il metodo **Altitude** recupera l'altitudine rispetto all'ellissoide di riferimento definito dall'ultima revisione del sistema geodetico mondiale (WGS 84), anziché dall'altitudine rispetto al livello Sea.</span><span class="sxs-lookup"><span data-stu-id="5abfe-118">The **Altitude** method retrieves the altitude relative to the reference ellipsoid that is defined by the latest revision of the World Geodetic System (WGS 84), rather than the altitude relative to sea level.</span></span>

## <a name="examples"></a><span data-ttu-id="5abfe-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="5abfe-119">Examples</span></span>

<span data-ttu-id="5abfe-120">Per un esempio di come usare questa proprietà, vedere [un semplice esempio di report LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="5abfe-120">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="5abfe-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5abfe-121">Requirements</span></span>



| <span data-ttu-id="5abfe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5abfe-122">Requirement</span></span> | <span data-ttu-id="5abfe-123">Valore</span><span class="sxs-lookup"><span data-stu-id="5abfe-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="5abfe-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5abfe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5abfe-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5abfe-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5abfe-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5abfe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5abfe-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5abfe-127">None supported</span></span><br/>                  |



 

