---
description: Rapporto Latitudine/Longitudine corrente.
ms.assetid: d2bb305f-911e-46f7-abde-56e9fba9182b
title: Proprietà LocationDisp. LatLongReportFactory. LatLongReport (LocationApi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.LatLongReport
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: c44582c01685431e9b5dfa4820735728dd2a9cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231886"
---
# <a name="locationdisplatlongreportfactorylatlongreport-property"></a><span data-ttu-id="78386-103">Proprietà LocationDisp. LatLongReportFactory. LatLongReport</span><span class="sxs-lookup"><span data-stu-id="78386-103">LocationDisp.LatLongReportFactory.LatLongReport property</span></span>

<span data-ttu-id="78386-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="78386-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="78386-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="78386-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="78386-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="78386-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="78386-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="78386-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="78386-108">Rapporto Latitudine/Longitudine corrente.</span><span class="sxs-lookup"><span data-stu-id="78386-108">The current latitude/longitude report.</span></span>

<span data-ttu-id="78386-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="78386-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="78386-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78386-110">Syntax</span></span>


```JScript
objLatLongReport = LocationDisp.LatLongReportFactory.LatLongReport
```



## <a name="property-value"></a><span data-ttu-id="78386-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="78386-111">Property value</span></span>

<span data-ttu-id="78386-112">Questa proprietà è di sola lettura [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md).</span><span class="sxs-lookup"><span data-stu-id="78386-112">This property is a read-only [**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md).</span></span>

## <a name="examples"></a><span data-ttu-id="78386-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="78386-113">Examples</span></span>

<span data-ttu-id="78386-114">Per un esempio di come usare questa proprietà, vedere [un semplice esempio di report LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="78386-114">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="78386-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78386-115">Requirements</span></span>



| <span data-ttu-id="78386-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="78386-116">Requirement</span></span> | <span data-ttu-id="78386-117">Valore</span><span class="sxs-lookup"><span data-stu-id="78386-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="78386-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78386-118">Minimum supported client</span></span><br/> | <span data-ttu-id="78386-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="78386-119">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="78386-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78386-120">Minimum supported server</span></span><br/> | <span data-ttu-id="78386-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="78386-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="78386-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78386-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="78386-123"><dt>LocationApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="78386-123"><dt>Locationapi.h</dt></span></span> </dl> |



 

