---
description: Errore di altitudine, in metri.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: Proprietà LocationDisp. DispLatLongReport. AltitudeError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.AltitudeError
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92fd71b133912a57e6ed4ef034dda6fe92ef9b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883017"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a><span data-ttu-id="60804-103">Proprietà LocationDisp. DispLatLongReport. AltitudeError</span><span class="sxs-lookup"><span data-stu-id="60804-103">LocationDisp.DispLatLongReport.AltitudeError property</span></span>

<span data-ttu-id="60804-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="60804-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="60804-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="60804-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="60804-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="60804-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="60804-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="60804-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="60804-108">Errore di altitudine, in metri.</span><span class="sxs-lookup"><span data-stu-id="60804-108">Altitude error, in meters.</span></span>

<span data-ttu-id="60804-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="60804-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="60804-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60804-110">Syntax</span></span>


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a><span data-ttu-id="60804-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="60804-111">Property value</span></span>

<span data-ttu-id="60804-112">Questa proprietà è un **numero** di sola lettura (virgola mobile a precisione doppia).</span><span class="sxs-lookup"><span data-stu-id="60804-112">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="remarks"></a><span data-ttu-id="60804-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="60804-113">Remarks</span></span>

<span data-ttu-id="60804-114">Non è necessario che i sensori di posizione forniscano questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="60804-114">Location sensors are not required to provide this property.</span></span> <span data-ttu-id="60804-115">È necessario gestire le eccezioni quando si tenta di accedere a questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="60804-115">You should handle exceptions when attempting to access this property.</span></span>

## <a name="examples"></a><span data-ttu-id="60804-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="60804-116">Examples</span></span>

<span data-ttu-id="60804-117">Per un esempio di come usare questa proprietà, vedere [un semplice esempio di report LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="60804-117">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="60804-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60804-118">Requirements</span></span>



| <span data-ttu-id="60804-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="60804-119">Requirement</span></span> | <span data-ttu-id="60804-120">Valore</span><span class="sxs-lookup"><span data-stu-id="60804-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="60804-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60804-121">Minimum supported client</span></span><br/> | <span data-ttu-id="60804-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="60804-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="60804-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="60804-123">Minimum supported server</span></span><br/> | <span data-ttu-id="60804-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="60804-124">None supported</span></span><br/>                  |



 

