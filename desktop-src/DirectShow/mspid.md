---
description: Nota Questa API è deprecata. Le nuove applicazioni non devono utilizzarlo. Il tipo di dati MSPID identifica lo scopo di un flusso multimediale.
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: MSPID (mmstream. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330925"
---
# <a name="mspid"></a><span data-ttu-id="a758f-105">MSPID</span><span class="sxs-lookup"><span data-stu-id="a758f-105">MSPID</span></span>

> [!Note]  
> <span data-ttu-id="a758f-106">Questa API è deprecata.</span><span class="sxs-lookup"><span data-stu-id="a758f-106">This API is deprecated.</span></span> <span data-ttu-id="a758f-107">Le nuove applicazioni non devono utilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="a758f-107">New applications should not use it.</span></span>

 

<span data-ttu-id="a758f-108">Il tipo di dati **MSPID** identifica lo scopo di un flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="a758f-108">The **MSPID** data type identifies the purpose of a media steam.</span></span>


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a><span data-ttu-id="a758f-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="a758f-109">Remarks</span></span>

<span data-ttu-id="a758f-110">**MSPID** è semplicemente un typedef per GUID.</span><span class="sxs-lookup"><span data-stu-id="a758f-110">**MSPID** is simply a typedef for GUID.</span></span> <span data-ttu-id="a758f-111">Sono definiti i seguenti MSPIDs.</span><span class="sxs-lookup"><span data-stu-id="a758f-111">The following MSPIDs are defined.</span></span>



| <span data-ttu-id="a758f-112">Valore</span><span class="sxs-lookup"><span data-stu-id="a758f-112">Value</span></span>               | <span data-ttu-id="a758f-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a758f-113">Description</span></span>           |
|---------------------|-----------------------|
| <span data-ttu-id="a758f-114">\_PRIMARYVIDEO MSPID</span><span class="sxs-lookup"><span data-stu-id="a758f-114">MSPID\_PrimaryVideo</span></span> | <span data-ttu-id="a758f-115">Flusso video primario.</span><span class="sxs-lookup"><span data-stu-id="a758f-115">Primary video stream.</span></span> |
| <span data-ttu-id="a758f-116">\_PRIMARYAUDIO MSPID</span><span class="sxs-lookup"><span data-stu-id="a758f-116">MSPID\_PrimaryAudio</span></span> | <span data-ttu-id="a758f-117">Flusso audio primario.</span><span class="sxs-lookup"><span data-stu-id="a758f-117">Primary audio stream.</span></span> |



 

<span data-ttu-id="a758f-118">Il tipo **REFMSPID** definisce un riferimento a un **MSPID**.</span><span class="sxs-lookup"><span data-stu-id="a758f-118">The **REFMSPID** type defines a reference to an **MSPID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a758f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a758f-119">Requirements</span></span>



| <span data-ttu-id="a758f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a758f-120">Requirement</span></span> | <span data-ttu-id="a758f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a758f-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a758f-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a758f-122">Header</span></span><br/> | <dl> <span data-ttu-id="a758f-123"><dt>Mmstream. h</dt></span><span class="sxs-lookup"><span data-stu-id="a758f-123"><dt>Mmstream.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a758f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a758f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a758f-125">Tipi di dati di streaming multimediali</span><span class="sxs-lookup"><span data-stu-id="a758f-125">Multimedia Streaming Data Types</span></span>](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




