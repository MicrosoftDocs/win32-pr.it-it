---
description: Valore di accuratezza desiderata corrente.
ms.assetid: dfad833b-bb0c-4c66-9942-da10abee5381
title: Proprietà LocationDisp. LatLongReportFactory. DesiredAccuracy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: e17e415d9503660d873ae4df67d2469c646dd80e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319025"
---
# <a name="locationdisplatlongreportfactorydesiredaccuracy-property"></a><span data-ttu-id="a951b-103">Proprietà LocationDisp. LatLongReportFactory. DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="a951b-103">LocationDisp.LatLongReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="a951b-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="a951b-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a951b-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="a951b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a951b-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a951b-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="a951b-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="a951b-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="a951b-108">Valore di accuratezza desiderata corrente.</span><span class="sxs-lookup"><span data-stu-id="a951b-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="a951b-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a951b-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a951b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a951b-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.LatLongReportFactory.DesiredAccuracy
LocationDisp.LatLongReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="a951b-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a951b-111">Property value</span></span>

<span data-ttu-id="a951b-112">Questa proprietà è un **ULONG** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a951b-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="a951b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a951b-113">Value</span></span>                                                                        | <span data-ttu-id="a951b-114">Significato</span><span class="sxs-lookup"><span data-stu-id="a951b-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a951b-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a951b-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="a951b-116">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a951b-116">Default.</span></span> <span data-ttu-id="a951b-117">Il sensore deve usare l'accuratezza per cui può ottimizzare l'uso del risparmio energia e altre considerazioni sui costi.</span><span class="sxs-lookup"><span data-stu-id="a951b-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="a951b-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a951b-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="a951b-119">Il sensore deve fornire il report più accurato possibile.</span><span class="sxs-lookup"><span data-stu-id="a951b-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="a951b-120">È incluso l'utilizzo di servizi a pagamento o il consumo maggiore della batteria o della larghezza di banda della connessione.</span><span class="sxs-lookup"><span data-stu-id="a951b-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a951b-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="a951b-121">Remarks</span></span>

<span data-ttu-id="a951b-122">Questo valore è una richiesta al provider di posizione.</span><span class="sxs-lookup"><span data-stu-id="a951b-122">This value is a request to the location provider.</span></span> <span data-ttu-id="a951b-123">Non è necessario che il provider di località fornisca report nell'intervallo richiesto.</span><span class="sxs-lookup"><span data-stu-id="a951b-123">The location provider is not required to provide reports at the interval you requested.</span></span> <span data-ttu-id="a951b-124">Leggere il valore di questa proprietà per individuare l'impostazione dell'intervallo di report true.</span><span class="sxs-lookup"><span data-stu-id="a951b-124">Read the value of this property to discover the true report interval setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="a951b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a951b-125">Requirements</span></span>



| <span data-ttu-id="a951b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a951b-126">Requirement</span></span> | <span data-ttu-id="a951b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a951b-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="a951b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a951b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a951b-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a951b-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a951b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a951b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a951b-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a951b-131">None supported</span></span><br/>                  |



 

