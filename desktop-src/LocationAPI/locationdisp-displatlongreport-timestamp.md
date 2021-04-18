---
description: Data e ora in cui è stato generato il report.
ms.assetid: 3b8036aa-499c-4baf-bcc4-5b6c3f54eb7b
title: Proprietà LocationDisp. DispLatLongReport. timestamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.Timestamp
api_type:
- COM
api_location: ''
ms.openlocfilehash: 5ec179c5958b1be73a5fd5f74e48d0063edb6696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319034"
---
# <a name="locationdispdisplatlongreporttimestamp-property"></a><span data-ttu-id="9c84a-103">Proprietà LocationDisp. DispLatLongReport. timestamp</span><span class="sxs-lookup"><span data-stu-id="9c84a-103">LocationDisp.DispLatLongReport.Timestamp property</span></span>

<span data-ttu-id="9c84a-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="9c84a-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9c84a-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="9c84a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="9c84a-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9c84a-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="9c84a-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="9c84a-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="9c84a-108">Data e ora in cui è stato generato il report.</span><span class="sxs-lookup"><span data-stu-id="9c84a-108">The date and time when the report was generated.</span></span>

<span data-ttu-id="9c84a-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9c84a-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c84a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c84a-110">Syntax</span></span>


```JScript
Timestamp = LocationDisp.DispLatLongReport.Timestamp
```



## <a name="property-value"></a><span data-ttu-id="9c84a-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9c84a-111">Property value</span></span>

<span data-ttu-id="9c84a-112">Questa proprietà è una **Data** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9c84a-112">This property is a read-only **Date**.</span></span> <span data-ttu-id="9c84a-113">I timestamp vengono forniti come ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="9c84a-113">Time stamps are provided as Coordinated Universal Time (UTC).</span></span>

## <a name="remarks"></a><span data-ttu-id="9c84a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c84a-114">Remarks</span></span>

<span data-ttu-id="9c84a-115">Si noti che per i linguaggi di scripting, ad esempio Microsoft JScript, potrebbe essere necessario eseguire conversioni in altri formati di tempo quando si visualizzano i timestamp come stringhe.</span><span class="sxs-lookup"><span data-stu-id="9c84a-115">Note that scripting languages, such as Microsoft JScript, might require you to perform conversions to other time formats when you display time stamps as strings.</span></span>

## <a name="examples"></a><span data-ttu-id="9c84a-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="9c84a-116">Examples</span></span>

<span data-ttu-id="9c84a-117">Per un esempio di come usare questa proprietà, vedere [un semplice esempio di report LatLong](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="9c84a-117">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c84a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c84a-118">Requirements</span></span>



| <span data-ttu-id="9c84a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c84a-119">Requirement</span></span> | <span data-ttu-id="9c84a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9c84a-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="9c84a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c84a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9c84a-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9c84a-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9c84a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c84a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9c84a-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9c84a-124">None supported</span></span><br/>                  |



 

