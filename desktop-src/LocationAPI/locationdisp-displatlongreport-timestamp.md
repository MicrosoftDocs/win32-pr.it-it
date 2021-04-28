---
description: 'Proprietà LocationDisp.DispLatLongReport.Timestamp: data e ora di generazione del report.'
ms.assetid: 3b8036aa-499c-4baf-bcc4-5b6c3f54eb7b
title: Proprietà LocationDisp.DispLatLongReport.Timestamp
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
ms.openlocfilehash: fd505f967bad31afa908609a72d108b17552fce8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105689"
---
# <a name="locationdispdisplatlongreporttimestamp-property"></a><span data-ttu-id="fb336-103">Proprietà LocationDisp.DispLatLongReport.Timestamp</span><span class="sxs-lookup"><span data-stu-id="fb336-103">LocationDisp.DispLatLongReport.Timestamp property</span></span>

<span data-ttu-id="fb336-104">\[Il modello a oggetti dell'API Location è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti.</span><span class="sxs-lookup"><span data-stu-id="fb336-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fb336-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="fb336-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="fb336-106">Per accedere invece alla posizione da un sito Web, usare [l'API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fb336-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="fb336-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]</span><span class="sxs-lookup"><span data-stu-id="fb336-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="fb336-108">Data e ora di generazione del report.</span><span class="sxs-lookup"><span data-stu-id="fb336-108">The date and time when the report was generated.</span></span>

<span data-ttu-id="fb336-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fb336-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb336-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb336-110">Syntax</span></span>


```JScript
Timestamp = LocationDisp.DispLatLongReport.Timestamp
```



## <a name="property-value"></a><span data-ttu-id="fb336-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fb336-111">Property value</span></span>

<span data-ttu-id="fb336-112">Questa proprietà è una data di sola **lettura.**</span><span class="sxs-lookup"><span data-stu-id="fb336-112">This property is a read-only **Date**.</span></span> <span data-ttu-id="fb336-113">I timestamp vengono forniti come Coordinated Universal Time (UTC).</span><span class="sxs-lookup"><span data-stu-id="fb336-113">Time stamps are provided as Coordinated Universal Time (UTC).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb336-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb336-114">Remarks</span></span>

<span data-ttu-id="fb336-115">Si noti che i linguaggi di scripting, ad esempio Microsoft JScript, potrebbero richiedere l'esecuzione di conversioni in altri formati di ora quando si visualizzano timestamp come stringhe.</span><span class="sxs-lookup"><span data-stu-id="fb336-115">Note that scripting languages, such as Microsoft JScript, might require you to perform conversions to other time formats when you display time stamps as strings.</span></span>

## <a name="examples"></a><span data-ttu-id="fb336-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="fb336-116">Examples</span></span>

<span data-ttu-id="fb336-117">Per un esempio di come usare questa proprietà, vedere [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="fb336-117">For an example of how to use this property, see [A Simple LatLong Report Example](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb336-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb336-118">Requirements</span></span>



| <span data-ttu-id="fb336-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb336-119">Requirement</span></span> | <span data-ttu-id="fb336-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fb336-120">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="fb336-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb336-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fb336-122">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="fb336-122">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fb336-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb336-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fb336-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fb336-124">None supported</span></span><br/>                  |



 

