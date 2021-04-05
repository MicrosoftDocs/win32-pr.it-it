---
description: Richiede gli eventi del rapporto Latitudine/Longitudine.
ms.assetid: c26a388b-e042-43da-a220-e3ecfcbd03a8
title: Metodo LocationDisp. LatLongReportFactory. ListenForReports (LocationApi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 7e822595339fa499aaf469336ca3580acb2815bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757337"
---
# <a name="locationdisplatlongreportfactorylistenforreports-method"></a><span data-ttu-id="899c9-103">LocationDisp. LatLongReportFactory. ListenForReports, metodo</span><span class="sxs-lookup"><span data-stu-id="899c9-103">LocationDisp.LatLongReportFactory.ListenForReports method</span></span>

<span data-ttu-id="899c9-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="899c9-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="899c9-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="899c9-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="899c9-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="899c9-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="899c9-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="899c9-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="899c9-108">Richiede gli eventi del rapporto Latitudine/Longitudine.</span><span class="sxs-lookup"><span data-stu-id="899c9-108">Requests latitude/longitude report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="899c9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="899c9-109">Syntax</span></span>


```JScript
LocationDisp.LatLongReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a><span data-ttu-id="899c9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="899c9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="899c9-111">*requestedReportInterval*</span><span class="sxs-lookup"><span data-stu-id="899c9-111">*requestedReportInterval*</span></span> 
</dt> <dd> <span data-ttu-id="899c9-112">Numero (**doppia parola**) che rappresenta il tempo richiesto tra gli eventi del rapporto di Latitudine/Longitudine, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="899c9-112">Number (**double word**) representing the requested time between latitude/longitude report events, in milliseconds.</span></span> <span data-ttu-id="899c9-113">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="899c9-113">See Remarks.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="899c9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="899c9-114">Return value</span></span>

<span data-ttu-id="899c9-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="899c9-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="899c9-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="899c9-116">Remarks</span></span>

<span data-ttu-id="899c9-117">Non è necessario che il provider di località fornisca report nell'intervallo richiesto.</span><span class="sxs-lookup"><span data-stu-id="899c9-117">The location provider is not required to provide reports at the interval that you request.</span></span> <span data-ttu-id="899c9-118">Leggere il valore della proprietà [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) per individuare l'impostazione dell'intervallo di report true.</span><span class="sxs-lookup"><span data-stu-id="899c9-118">Read the value of the [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md) property to discover the true report interval setting.</span></span>

## <a name="examples"></a><span data-ttu-id="899c9-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="899c9-119">Examples</span></span>

<span data-ttu-id="899c9-120">Per un esempio di come usare questo metodo, vedere [ascolto degli eventi del report LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="899c9-120">For an example of how to use this method, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="899c9-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="899c9-121">Requirements</span></span>



| <span data-ttu-id="899c9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="899c9-122">Requirement</span></span> | <span data-ttu-id="899c9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="899c9-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="899c9-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="899c9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="899c9-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="899c9-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="899c9-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="899c9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="899c9-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="899c9-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="899c9-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="899c9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="899c9-129"><dt>LocationApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="899c9-129"><dt>Locationapi.h</dt></span></span> </dl> |



 

