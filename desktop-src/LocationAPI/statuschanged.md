---
description: Si verifica in seguito alla modifica dello stato operativo di un report.
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: Evento StatusChanged
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: d1bda6645002f586eda0e2dad99a134450329d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234357"
---
# <a name="statuschanged-event"></a><span data-ttu-id="ffdc6-103">Evento StatusChanged</span><span class="sxs-lookup"><span data-stu-id="ffdc6-103">StatusChanged event</span></span>

<span data-ttu-id="ffdc6-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="ffdc6-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ffdc6-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="ffdc6-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ffdc6-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ffdc6-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="ffdc6-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="ffdc6-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="ffdc6-108">Si verifica in seguito alla modifica dello stato operativo di un report.</span><span class="sxs-lookup"><span data-stu-id="ffdc6-108">Occurs when the operational status of a report changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffdc6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffdc6-109">Syntax</span></span>


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a><span data-ttu-id="ffdc6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffdc6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffdc6-111">*Stato*</span><span class="sxs-lookup"><span data-stu-id="ffdc6-111">*status*</span></span> 
</dt> <dd>

<span data-ttu-id="ffdc6-112">Il nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="ffdc6-112">The new status.</span></span>



| <span data-ttu-id="ffdc6-113">Stato</span><span class="sxs-lookup"><span data-stu-id="ffdc6-113">Status</span></span>                                                                                               | <span data-ttu-id="ffdc6-114">Significato</span><span class="sxs-lookup"><span data-stu-id="ffdc6-114">Meaning</span></span>                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="ffdc6-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="ffdc6-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="ffdc6-116">Il report non è supportato.</span><span class="sxs-lookup"><span data-stu-id="ffdc6-116">Report not supported.</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="ffdc6-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="ffdc6-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="ffdc6-118">Errore.</span><span class="sxs-lookup"><span data-stu-id="ffdc6-118">Error.</span></span><br/>                |
| <span id="2"></span><dl> <span data-ttu-id="ffdc6-119"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="ffdc6-119"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="ffdc6-120">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="ffdc6-120">Access denied.</span></span><br/>        |
| <span id="3"></span><dl> <span data-ttu-id="ffdc6-121"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="ffdc6-121"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="ffdc6-122">Inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="ffdc6-122">Initializing.</span></span><br/>         |
| <span id="4"></span><dl> <span data-ttu-id="ffdc6-123"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="ffdc6-123"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="ffdc6-124">In esecuzione.</span><span class="sxs-lookup"><span data-stu-id="ffdc6-124">Running.</span></span><br/>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffdc6-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffdc6-125">Return value</span></span>

<span data-ttu-id="ffdc6-126">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ffdc6-126">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffdc6-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffdc6-127">Remarks</span></span>

<span data-ttu-id="ffdc6-128">È necessario implementare gestori di report di modifica dello stato distinti per i report degli indirizzi civici e i report di Latitudine/Longitudine.</span><span class="sxs-lookup"><span data-stu-id="ffdc6-128">You should implement separate status change report handlers for civic address reports and latitude/longitude reports.</span></span>

## <a name="examples"></a><span data-ttu-id="ffdc6-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="ffdc6-129">Examples</span></span>

<span data-ttu-id="ffdc6-130">Per un esempio di come usare questo evento, vedere [ascolto degli eventi del report LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="ffdc6-130">For an example of how to use this event, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffdc6-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffdc6-131">Requirements</span></span>



| <span data-ttu-id="ffdc6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffdc6-132">Requirement</span></span> | <span data-ttu-id="ffdc6-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ffdc6-133">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="ffdc6-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffdc6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ffdc6-135">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ffdc6-135">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ffdc6-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffdc6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ffdc6-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ffdc6-137">None supported</span></span><br/>                  |



 

