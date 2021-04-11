---
description: Intervallo di eventi del report di Latitudine/Longitudine corrente in millisecondi.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: Proprietà LocationDisp. LatLongReportFactory. ReportInterval
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: b456f69a70655b22b1eca30e02d9d5369d19f38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232076"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a><span data-ttu-id="a2bb2-103">Proprietà LocationDisp. LatLongReportFactory. ReportInterval</span><span class="sxs-lookup"><span data-stu-id="a2bb2-103">LocationDisp.LatLongReportFactory.ReportInterval property</span></span>

<span data-ttu-id="a2bb2-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a2bb2-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a2bb2-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="a2bb2-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a2bb2-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2bb2-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="a2bb2-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="a2bb2-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="a2bb2-108">Intervallo di eventi del report di Latitudine/Longitudine corrente in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="a2bb2-108">The current latitude/longitude report event interval in milliseconds.</span></span>

<span data-ttu-id="a2bb2-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a2bb2-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2bb2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2bb2-110">Syntax</span></span>


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a><span data-ttu-id="a2bb2-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a2bb2-111">Property value</span></span>

<span data-ttu-id="a2bb2-112">Questa proprietà è un **ULONG** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a2bb2-112">This property is a read/write **ULONG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2bb2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2bb2-113">Remarks</span></span>

<span data-ttu-id="a2bb2-114">Questo valore è una richiesta al provider di posizione.</span><span class="sxs-lookup"><span data-stu-id="a2bb2-114">This value is a request to the location provider.</span></span> <span data-ttu-id="a2bb2-115">Non è necessario che il provider di località fornisca report nell'intervallo richiesto.</span><span class="sxs-lookup"><span data-stu-id="a2bb2-115">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="a2bb2-116">Leggere il valore di questa proprietà per individuare l'impostazione dell'intervallo di report true.</span><span class="sxs-lookup"><span data-stu-id="a2bb2-116">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2bb2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2bb2-117">Requirements</span></span>



| <span data-ttu-id="a2bb2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2bb2-118">Requirement</span></span> | <span data-ttu-id="a2bb2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a2bb2-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="a2bb2-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2bb2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a2bb2-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a2bb2-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a2bb2-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2bb2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a2bb2-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a2bb2-123">None supported</span></span><br/>                  |



 

