---
description: Longitudine corrente, in gradi.
ms.assetid: f4fa1cbb-d682-42ab-9dd8-dff636ea4c8a
title: LocationDisp. DispLatLongReport. Longitudine (proprietà)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Longitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: c705ebd9476582f05b6dc87233dcc8e8990c5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319035"
---
# <a name="locationdispdisplatlongreportlongitude-property"></a><span data-ttu-id="768a8-103">LocationDisp. DispLatLongReport. Longitudine (proprietà)</span><span class="sxs-lookup"><span data-stu-id="768a8-103">LocationDisp.DispLatLongReport.Longitude property</span></span>

<span data-ttu-id="768a8-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="768a8-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="768a8-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="768a8-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="768a8-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="768a8-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="768a8-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="768a8-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="768a8-108">Longitudine corrente, in gradi.</span><span class="sxs-lookup"><span data-stu-id="768a8-108">Current longitude, in degrees.</span></span> <span data-ttu-id="768a8-109">La longitudine è compresa tra-180 e 180, dove East è un valore positivo.</span><span class="sxs-lookup"><span data-stu-id="768a8-109">The longitude is between -180 and 180, where east is positive.</span></span>

<span data-ttu-id="768a8-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="768a8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="768a8-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="768a8-111">Syntax</span></span>


```JScript
Longitude = LocationDisp.DispLatLongReport.Longitude
```



## <a name="property-value"></a><span data-ttu-id="768a8-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="768a8-112">Property value</span></span>

<span data-ttu-id="768a8-113">Questa proprietà è un **numero** di sola lettura (virgola mobile a precisione doppia).</span><span class="sxs-lookup"><span data-stu-id="768a8-113">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="768a8-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="768a8-114">Examples</span></span>

<span data-ttu-id="768a8-115">Per un esempio di come usare questa proprietà, vedere [un semplice esempio di report LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="768a8-115">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="768a8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="768a8-116">Requirements</span></span>



| <span data-ttu-id="768a8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="768a8-117">Requirement</span></span> | <span data-ttu-id="768a8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="768a8-118">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="768a8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="768a8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="768a8-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="768a8-120">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="768a8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="768a8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="768a8-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="768a8-122">None supported</span></span><br/>                  |



 

