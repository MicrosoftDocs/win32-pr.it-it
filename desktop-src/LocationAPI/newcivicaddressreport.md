---
description: Si verifica quando viene generato un nuovo report sull'indirizzo civico.
ms.assetid: a8df870e-6744-4e8a-a103-56b446da135f
title: Evento NewCivicAddressReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewCivicAddressReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: fa786ecee4ce4223cdb7ec0c8400c5c11bf6e192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885534"
---
# <a name="newcivicaddressreport-event"></a><span data-ttu-id="06fae-103">Evento NewCivicAddressReport</span><span class="sxs-lookup"><span data-stu-id="06fae-103">NewCivicAddressReport event</span></span>

<span data-ttu-id="06fae-104">\[Il modello a oggetti dell'API location è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="06fae-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="06fae-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="06fae-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="06fae-106">Per accedere al percorso da un sito Web, usare invece l' [API di georilevazione W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="06fae-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="06fae-107">Per accedere alla posizione da un'applicazione desktop, usare l'API [**Windows. Devices. Geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="06fae-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="06fae-108">Si verifica quando viene generato un nuovo report sull'indirizzo civico.</span><span class="sxs-lookup"><span data-stu-id="06fae-108">Occurs when a new civic address report is generated.</span></span>

## <a name="syntax"></a><span data-ttu-id="06fae-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06fae-109">Syntax</span></span>


```JScript
.NewCivicAddressReport(
  newReport
)
```



## <a name="parameters"></a><span data-ttu-id="06fae-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="06fae-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06fae-111">*newReport*</span><span class="sxs-lookup"><span data-stu-id="06fae-111">*newReport*</span></span> 
</dt> <dd>

<span data-ttu-id="06fae-112">Nuovo oggetto [**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md) .</span><span class="sxs-lookup"><span data-stu-id="06fae-112">The new [**LocationDisp.DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06fae-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06fae-113">Return value</span></span>

<span data-ttu-id="06fae-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="06fae-114">This event does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="06fae-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="06fae-115">Examples</span></span>

<span data-ttu-id="06fae-116">Per un esempio di come usare questo evento, vedere [ascolto di eventi di report di indirizzi civici](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="06fae-116">For an example of how to use this event, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="06fae-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06fae-117">Requirements</span></span>



| <span data-ttu-id="06fae-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="06fae-118">Requirement</span></span> | <span data-ttu-id="06fae-119">Valore</span><span class="sxs-lookup"><span data-stu-id="06fae-119">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="06fae-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06fae-120">Minimum supported client</span></span><br/> | <span data-ttu-id="06fae-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="06fae-121">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="06fae-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06fae-122">Minimum supported server</span></span><br/> | <span data-ttu-id="06fae-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="06fae-123">None supported</span></span><br/>                  |



 

