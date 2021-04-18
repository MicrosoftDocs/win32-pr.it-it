---
description: Valore di accuratezza desiderata corrente.
ms.assetid: 296164cf-a8ed-4277-bb4c-83ac09e63291
title: Proprietà LocationDisp. CivicAddressReportFactory. DesiredAccuracy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.DesiredAccuracy
api_type:
- COM
api_location: ''
ms.openlocfilehash: eb05aeb6a69bfe978682d418cf1e71aed2184bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319039"
---
# <a name="locationdispcivicaddressreportfactorydesiredaccuracy-property"></a><span data-ttu-id="db579-103">Proprietà LocationDisp. CivicAddressReportFactory. DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="db579-103">LocationDisp.CivicAddressReportFactory.DesiredAccuracy property</span></span>

<span data-ttu-id="db579-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="db579-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="db579-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="db579-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="db579-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="db579-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="db579-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="db579-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="db579-108">Valore di accuratezza desiderata corrente.</span><span class="sxs-lookup"><span data-stu-id="db579-108">The current desired-accuracy value.</span></span>

<span data-ttu-id="db579-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="db579-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="db579-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db579-110">Syntax</span></span>


```JScript
DesiredAccuracy = LocationDisp.CivicAddressReportFactory.DesiredAccuracy
LocationDisp.CivicAddressReportFactory.DesiredAccuracy = DesiredAccuracy
```



## <a name="property-value"></a><span data-ttu-id="db579-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="db579-111">Property value</span></span>

<span data-ttu-id="db579-112">Questa proprietà è un **ULONG** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="db579-112">This property is a read/write **ULONG**.</span></span>



| <span data-ttu-id="db579-113">Valore</span><span class="sxs-lookup"><span data-stu-id="db579-113">Value</span></span>                                                                        | <span data-ttu-id="db579-114">Significato</span><span class="sxs-lookup"><span data-stu-id="db579-114">Meaning</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db579-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="db579-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="db579-116">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="db579-116">Default.</span></span> <span data-ttu-id="db579-117">Il sensore deve usare l'accuratezza per cui può ottimizzare l'uso del risparmio energia e altre considerazioni sui costi.</span><span class="sxs-lookup"><span data-stu-id="db579-117">The sensor should use the accuracy for which it can optimize power use and other cost considerations.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="db579-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="db579-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="db579-119">Il sensore deve fornire il report più accurato possibile.</span><span class="sxs-lookup"><span data-stu-id="db579-119">The sensor should deliver the most accurate report possible.</span></span> <span data-ttu-id="db579-120">È incluso l'utilizzo di servizi a pagamento o il consumo maggiore della batteria o della larghezza di banda della connessione.</span><span class="sxs-lookup"><span data-stu-id="db579-120">This includes using services that might charge money, or consuming higher levels of battery power or connection bandwidth.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db579-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="db579-121">Remarks</span></span>

<span data-ttu-id="db579-122">Questo valore è una richiesta al provider di posizione.</span><span class="sxs-lookup"><span data-stu-id="db579-122">This value is a request to the location provider.</span></span> <span data-ttu-id="db579-123">Il provider di posizione non è necessario per fornire l'accuratezza richiesta.</span><span class="sxs-lookup"><span data-stu-id="db579-123">The location provider is not required to provide the accuracy that you request.</span></span> <span data-ttu-id="db579-124">Leggere il valore di questa proprietà per individuare l'impostazione di accuratezza effettiva.</span><span class="sxs-lookup"><span data-stu-id="db579-124">Read the value of this property to discover the true accuracy setting.</span></span>

## <a name="requirements"></a><span data-ttu-id="db579-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db579-125">Requirements</span></span>



| <span data-ttu-id="db579-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="db579-126">Requirement</span></span> | <span data-ttu-id="db579-127">Valore</span><span class="sxs-lookup"><span data-stu-id="db579-127">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="db579-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db579-128">Minimum supported client</span></span><br/> | <span data-ttu-id="db579-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="db579-129">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="db579-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="db579-130">Minimum supported server</span></span><br/> | <span data-ttu-id="db579-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="db579-131">None supported</span></span><br/>                  |



 

