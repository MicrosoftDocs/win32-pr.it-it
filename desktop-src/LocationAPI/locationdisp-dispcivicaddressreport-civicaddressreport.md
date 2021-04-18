---
description: Report dell'indirizzo civico corrente.
ms.assetid: a58dd612-bc54-42d1-9960-8c3de1c4fa83
title: Proprietà LocationDisp. CivicAddressReportFactory. CivicAddressReport (LocationApi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.CivicAddressReport
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: c8be6e03861f1c5b2abffcb4b23d4845defa494e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315912"
---
# <a name="locationdispcivicaddressreportfactorycivicaddressreport-property"></a><span data-ttu-id="72a1e-103">Proprietà LocationDisp. CivicAddressReportFactory. CivicAddressReport</span><span class="sxs-lookup"><span data-stu-id="72a1e-103">LocationDisp.CivicAddressReportFactory.CivicAddressReport property</span></span>

<span data-ttu-id="72a1e-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="72a1e-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="72a1e-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="72a1e-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="72a1e-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="72a1e-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="72a1e-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="72a1e-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="72a1e-108">Report dell'indirizzo civico corrente.</span><span class="sxs-lookup"><span data-stu-id="72a1e-108">The current civic address report.</span></span>

<span data-ttu-id="72a1e-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="72a1e-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="72a1e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="72a1e-110">Syntax</span></span>


```JScript
objCivicAddressReport = LocationDisp.CivicAddressReportFactory.CivicAddressReport
```



## <a name="property-value"></a><span data-ttu-id="72a1e-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="72a1e-111">Property value</span></span>

<span data-ttu-id="72a1e-112">Questa proprietà è di sola lettura [**LocationDisp. CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md).</span><span class="sxs-lookup"><span data-stu-id="72a1e-112">This property is a read-only [**LocationDisp.CivicAddressReportFactory**](locationdisp-civicaddressreportfactory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="72a1e-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="72a1e-113">Examples</span></span>

<span data-ttu-id="72a1e-114">Per un esempio di come usare questa proprietà, vedere [un semplice esempio di report sull'indirizzo civico](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="72a1e-114">For an example of how to use this property, see [A Simple Civic Address Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="72a1e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72a1e-115">Requirements</span></span>



| <span data-ttu-id="72a1e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="72a1e-116">Requirement</span></span> | <span data-ttu-id="72a1e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="72a1e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="72a1e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72a1e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="72a1e-119">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="72a1e-119">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="72a1e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72a1e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="72a1e-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="72a1e-121">None supported</span></span><br/>                                                                |
| <span data-ttu-id="72a1e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72a1e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="72a1e-123"><dt>LocationApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="72a1e-123"><dt>Locationapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72a1e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72a1e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72a1e-125">**LocationDisp.CivicAddressReportFactory**</span><span class="sxs-lookup"><span data-stu-id="72a1e-125">**LocationDisp.CivicAddressReportFactory**</span></span>](locationdisp-civicaddressreportfactory.md)
</dt> </dl>

 

