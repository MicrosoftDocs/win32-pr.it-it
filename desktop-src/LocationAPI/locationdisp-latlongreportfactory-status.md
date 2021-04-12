---
description: Stato corrente del report.
ms.assetid: bcdf76b5-88c4-481a-89ac-2b9558cecfc0
title: Proprietà LocationDisp. LatLongReportFactory. status
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: c32f1e58c5c519bdbdf797f81f11a449bfb3dc1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346031"
---
# <a name="locationdisplatlongreportfactorystatus-property"></a><span data-ttu-id="028fb-103">Proprietà LocationDisp. LatLongReportFactory. status</span><span class="sxs-lookup"><span data-stu-id="028fb-103">LocationDisp.LatLongReportFactory.Status property</span></span>

<span data-ttu-id="028fb-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="028fb-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="028fb-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="028fb-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="028fb-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="028fb-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="028fb-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="028fb-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="028fb-108">Stato corrente del report.</span><span class="sxs-lookup"><span data-stu-id="028fb-108">The current report status.</span></span>

<span data-ttu-id="028fb-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="028fb-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="028fb-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="028fb-110">Syntax</span></span>


```JScript
Status = LocationDisp.LatLongReportFactory.Status
```



## <a name="property-value"></a><span data-ttu-id="028fb-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="028fb-111">Property value</span></span>

<span data-ttu-id="028fb-112">Questa proprietà è un **numero** di sola lettura (unsigned long).</span><span class="sxs-lookup"><span data-stu-id="028fb-112">This property is a read-only **Number** (unsigned long).</span></span>



| <span data-ttu-id="028fb-113">Stato</span><span class="sxs-lookup"><span data-stu-id="028fb-113">Status</span></span>                                                                                               | <span data-ttu-id="028fb-114">Significato</span><span class="sxs-lookup"><span data-stu-id="028fb-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="028fb-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="028fb-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="028fb-116">Il report non è supportato.</span><span class="sxs-lookup"><span data-stu-id="028fb-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="028fb-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="028fb-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="028fb-118">Errore.</span><span class="sxs-lookup"><span data-stu-id="028fb-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="028fb-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="028fb-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="028fb-120">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="028fb-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="028fb-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="028fb-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="028fb-122">Inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="028fb-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="028fb-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="028fb-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="028fb-124">In esecuzione.</span><span class="sxs-lookup"><span data-stu-id="028fb-124">Running.</span></span><br/>              |



 

## <a name="examples"></a><span data-ttu-id="028fb-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="028fb-125">Examples</span></span>

<span data-ttu-id="028fb-126">Per un esempio di come usare questa proprietà, vedere [ascolto degli eventi del report LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="028fb-126">For an example of how to use this property, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="028fb-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="028fb-127">Requirements</span></span>



| <span data-ttu-id="028fb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="028fb-128">Requirement</span></span> | <span data-ttu-id="028fb-129">Valore</span><span class="sxs-lookup"><span data-stu-id="028fb-129">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="028fb-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="028fb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="028fb-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="028fb-131">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="028fb-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="028fb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="028fb-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="028fb-133">None supported</span></span><br/>                  |



 

