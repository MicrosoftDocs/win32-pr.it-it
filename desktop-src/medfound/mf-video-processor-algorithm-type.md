---
description: Definisce gli algoritmi per il processore video usato dall' \_ algoritmo MF video \_ Processor \_ .
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: Enumerazione MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 604fee61ae4b6a34d876de8c2863ee6dddad73d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308424"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a><span data-ttu-id="35f7b-103">\_Enumerazione del \_ \_ tipo di algoritmo MF Video Processor \_</span><span class="sxs-lookup"><span data-stu-id="35f7b-103">MF\_VIDEO\_PROCESSOR\_ALGORITHM\_TYPE enumeration</span></span>

<span data-ttu-id="35f7b-104">Definisce gli algoritmi per il processore video usato dall' [ \_ \_ \_ algoritmo MF video processor](mf-video-processor-algorithm.md).</span><span class="sxs-lookup"><span data-stu-id="35f7b-104">Defines algorithms for the video processor which is use by [MF\_VIDEO\_PROCESSOR\_ALGORITHM](mf-video-processor-algorithm.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="35f7b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35f7b-105">Syntax</span></span>


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a><span data-ttu-id="35f7b-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="35f7b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="35f7b-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**\_ \_ \_ impostazione predefinita algoritmo MF Video Processor \_**</span><span class="sxs-lookup"><span data-stu-id="35f7b-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="35f7b-108">la modalità predefinita predilige un equilibrio tra qualità e velocità</span><span class="sxs-lookup"><span data-stu-id="35f7b-108">default mode favors a balance of quality and speed</span></span>

</dd> <dt>

<span data-ttu-id="35f7b-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**\_Algoritmo MF video \_ Processor \_ \_ MRF \_ CRF \_ 444**</span><span class="sxs-lookup"><span data-stu-id="35f7b-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_MRF\_CRF\_444**</span></span>
</dt> <dd>

<span data-ttu-id="35f7b-110">Il processore video viene sempre elaborato internamente in AYUV e utilizza filtri di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="35f7b-110">The video processor will always internally process in AYUV and use high quality filters.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35f7b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35f7b-111">Requirements</span></span>



| <span data-ttu-id="35f7b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="35f7b-112">Requirement</span></span> | <span data-ttu-id="35f7b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="35f7b-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35f7b-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35f7b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="35f7b-115">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="35f7b-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="35f7b-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35f7b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="35f7b-117">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="35f7b-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="35f7b-118">IDL</span><span class="sxs-lookup"><span data-stu-id="35f7b-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35f7b-119"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35f7b-119"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f7b-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35f7b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f7b-121">Enumerazioni di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="35f7b-121">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




