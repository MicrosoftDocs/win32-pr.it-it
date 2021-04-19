---
description: Latitudine corrente, in gradi.
ms.assetid: 24a4e75c-5162-406a-bf34-471387bff5d9
title: Proprietà LocationDisp. DispLatLongReport. Latitude
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Latitude
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7f1bb6e7441b4e007c972f43bb45f59236ebe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317133"
---
# <a name="locationdispdisplatlongreportlatitude-property"></a><span data-ttu-id="73865-103">Proprietà LocationDisp. DispLatLongReport. Latitude</span><span class="sxs-lookup"><span data-stu-id="73865-103">LocationDisp.DispLatLongReport.Latitude property</span></span>

<span data-ttu-id="73865-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="73865-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="73865-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="73865-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="73865-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="73865-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="73865-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="73865-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="73865-108">Latitudine corrente, in gradi.</span><span class="sxs-lookup"><span data-stu-id="73865-108">Current latitude, in degrees.</span></span> <span data-ttu-id="73865-109">La latitudine è compresa tra-90 e 90, dove il Nord è positivo.</span><span class="sxs-lookup"><span data-stu-id="73865-109">The latitude is between -90 and 90, where north is positive.</span></span>

<span data-ttu-id="73865-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="73865-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="73865-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73865-111">Syntax</span></span>


```JScript
Latitude = LocationDisp.DispLatLongReport.Latitude
```



## <a name="property-value"></a><span data-ttu-id="73865-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="73865-112">Property value</span></span>

<span data-ttu-id="73865-113">Questa proprietà è un **numero** di sola lettura (virgola mobile a precisione doppia).</span><span class="sxs-lookup"><span data-stu-id="73865-113">This property is a read-only **Number** (double precision floating point).</span></span>

## <a name="examples"></a><span data-ttu-id="73865-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="73865-114">Examples</span></span>

<span data-ttu-id="73865-115">Per un esempio di come usare questa proprietà, vedere [un semplice esempio di report LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="73865-115">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="73865-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73865-116">Requirements</span></span>



| <span data-ttu-id="73865-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="73865-117">Requirement</span></span> | <span data-ttu-id="73865-118">Valore</span><span class="sxs-lookup"><span data-stu-id="73865-118">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="73865-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73865-119">Minimum supported client</span></span><br/> | <span data-ttu-id="73865-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="73865-120">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="73865-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73865-121">Minimum supported server</span></span><br/> | <span data-ttu-id="73865-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="73865-122">None supported</span></span><br/>                  |



 

