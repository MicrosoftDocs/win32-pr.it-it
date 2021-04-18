---
description: Arresta gli eventi del report degli indirizzi civici.
ms.assetid: 6efe26bc-842d-49fc-aec2-e0dfa7f1eb0a
title: Metodo LocationDisp. CivicAddressReportFactory. StopListeningForReports (LocationApi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.StopListeningForReports
api_type:
- COM
api_location:
- locationapi.h
ms.openlocfilehash: 36c58e9db0edb66735dcbd58c8e1968cfa8b1fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319036"
---
# <a name="locationdispcivicaddressreportfactorystoplisteningforreports-method"></a><span data-ttu-id="7b4b2-103">LocationDisp. CivicAddressReportFactory. StopListeningForReports, metodo</span><span class="sxs-lookup"><span data-stu-id="7b4b2-103">LocationDisp.CivicAddressReportFactory.StopListeningForReports method</span></span>

<span data-ttu-id="7b4b2-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="7b4b2-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7b4b2-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="7b4b2-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="7b4b2-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7b4b2-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="7b4b2-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="7b4b2-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="7b4b2-108">Arresta gli eventi del report degli indirizzi civici.</span><span class="sxs-lookup"><span data-stu-id="7b4b2-108">Stops civic address report events.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4b2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b4b2-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.StopListeningForReports()
```



## <a name="parameters"></a><span data-ttu-id="7b4b2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b4b2-110">Parameters</span></span>

<span data-ttu-id="7b4b2-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7b4b2-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b4b2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b4b2-112">Return value</span></span>

<span data-ttu-id="7b4b2-113">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7b4b2-113">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="7b4b2-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="7b4b2-114">Examples</span></span>

<span data-ttu-id="7b4b2-115">Per un esempio di come usare questo metodo, vedere [ascolto di eventi di report di indirizzi civici](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="7b4b2-115">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b4b2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b4b2-116">Requirements</span></span>



| <span data-ttu-id="7b4b2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b4b2-117">Requirement</span></span> | <span data-ttu-id="7b4b2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7b4b2-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4b2-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b4b2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7b4b2-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7b4b2-120">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7b4b2-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b4b2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7b4b2-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7b4b2-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7b4b2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b4b2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b4b2-124"><dt>LocationApi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b4b2-124"><dt>Locationapi.h</dt></span></span> </dl> |



 

