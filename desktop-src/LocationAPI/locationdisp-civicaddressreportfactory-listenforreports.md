---
description: Richiede eventi di report relativi all'indirizzo civico.
ms.assetid: cb02f611-7cda-405f-aeee-833b7385a4be
title: Metodo LocationDisp. CivicAddressReportFactory. ListenForReports (LocationApi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ListenForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 02315f8b2f7fced76c3d0d1330df246af6bad4b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968591"
---
# <a name="locationdispcivicaddressreportfactorylistenforreports-method"></a><span data-ttu-id="66fe0-103">LocationDisp. CivicAddressReportFactory. ListenForReports, metodo</span><span class="sxs-lookup"><span data-stu-id="66fe0-103">LocationDisp.CivicAddressReportFactory.ListenForReports method</span></span>

<span data-ttu-id="66fe0-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="66fe0-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="66fe0-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="66fe0-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="66fe0-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="66fe0-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="66fe0-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="66fe0-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="66fe0-108">Richiede eventi di report relativi all'indirizzo civico.</span><span class="sxs-lookup"><span data-stu-id="66fe0-108">Requests civic address report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="66fe0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66fe0-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.ListenForReports(
  requestedReportInterval
)
```



## <a name="parameters"></a><span data-ttu-id="66fe0-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="66fe0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66fe0-111">*requestedReportInterval*</span><span class="sxs-lookup"><span data-stu-id="66fe0-111">*requestedReportInterval*</span></span> 
</dt> <dd> <span data-ttu-id="66fe0-112">Numero (**doppia parola**) che rappresenta il tempo richiesto tra gli eventi del rapporto di indirizzo civico, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="66fe0-112">Number (**double word**) representing the requested time between civic address report events, in milliseconds.</span></span> <span data-ttu-id="66fe0-113">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="66fe0-113">See Remarks.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66fe0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66fe0-114">Return value</span></span>

<span data-ttu-id="66fe0-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="66fe0-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66fe0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="66fe0-116">Remarks</span></span>

<span data-ttu-id="66fe0-117">Il provider di posizione non è necessario per fornire l'accuratezza richiesta.</span><span class="sxs-lookup"><span data-stu-id="66fe0-117">The location provider is not required to provide the accuracy that you request.</span></span> <span data-ttu-id="66fe0-118">Leggere il valore della proprietà [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) per individuare l'impostazione dell'intervallo di report true.</span><span class="sxs-lookup"><span data-stu-id="66fe0-118">Read the value of the [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md) property to discover the true report interval setting.</span></span>

## <a name="examples"></a><span data-ttu-id="66fe0-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="66fe0-119">Examples</span></span>

<span data-ttu-id="66fe0-120">Per un esempio di come usare questo metodo, vedere [ascolto di eventi di report di indirizzi civici](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="66fe0-120">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="66fe0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66fe0-121">Requirements</span></span>



| <span data-ttu-id="66fe0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="66fe0-122">Requirement</span></span> | <span data-ttu-id="66fe0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="66fe0-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66fe0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66fe0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="66fe0-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="66fe0-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="66fe0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66fe0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="66fe0-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="66fe0-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="66fe0-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66fe0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="66fe0-129"><dt>LocationApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="66fe0-129"><dt>Locationapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66fe0-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66fe0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66fe0-131">**Evento NewCivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="66fe0-131">**NewCivicAddressReport Event**</span></span>](newcivicaddressreport.md)
</dt> </dl>

 

