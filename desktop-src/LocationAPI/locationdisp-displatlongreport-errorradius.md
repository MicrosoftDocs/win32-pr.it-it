---
description: Distanza tra la posizione indicata, in metri. In combinazione con la posizione indicata come origine, questo raggio descrive il cerchio in cui è probabilmente individuato il percorso effettivo.
ms.assetid: a9565bd5-d1e0-45f8-abeb-3191b16480fa
title: Proprietà LocationDisp. DispLatLongReport. ErrorRadius
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.ErrorRadius
api_type:
- COM
api_location: ''
ms.openlocfilehash: f99ff9b03451738158a98541bfae0e67a8827717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313362"
---
# <a name="locationdispdisplatlongreporterrorradius-property"></a><span data-ttu-id="725a3-104">Proprietà LocationDisp. DispLatLongReport. ErrorRadius</span><span class="sxs-lookup"><span data-stu-id="725a3-104">LocationDisp.DispLatLongReport.ErrorRadius property</span></span>

<span data-ttu-id="725a3-105">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="725a3-105">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="725a3-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="725a3-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="725a3-107">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="725a3-107">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="725a3-108">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="725a3-108">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="725a3-109">Distanza tra la posizione indicata, in metri.</span><span class="sxs-lookup"><span data-stu-id="725a3-109">A distance from the reported location, in meters.</span></span> <span data-ttu-id="725a3-110">In combinazione con la posizione indicata come origine, questo raggio descrive il cerchio in cui è probabilmente individuato il percorso effettivo.</span><span class="sxs-lookup"><span data-stu-id="725a3-110">Combined with the reported location as the origin, this radius describes the circle in which the actual location is probably located.</span></span>

<span data-ttu-id="725a3-111">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="725a3-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="725a3-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="725a3-112">Syntax</span></span>


```JScript
ErrorRadius = LocationDisp.DispLatLongReport.ErrorRadius
```



## <a name="property-value"></a><span data-ttu-id="725a3-113">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="725a3-113">Property value</span></span>

<span data-ttu-id="725a3-114">Questa proprietà è un **numero** di sola lettura (virgola mobile a precisione doppia).</span><span class="sxs-lookup"><span data-stu-id="725a3-114">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="725a3-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="725a3-115">Examples</span></span>

<span data-ttu-id="725a3-116">Per un esempio di come usare questa proprietà, vedere [un semplice esempio di report LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="725a3-116">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="725a3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="725a3-117">Requirements</span></span>



| <span data-ttu-id="725a3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="725a3-118">Requirement</span></span> | <span data-ttu-id="725a3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="725a3-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="725a3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="725a3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="725a3-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="725a3-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="725a3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="725a3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="725a3-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="725a3-123">None supported</span></span><br/>                  |



 

