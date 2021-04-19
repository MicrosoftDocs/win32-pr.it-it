---
description: Contiene informazioni sul formato per la ricompressione intelligente.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: Struttura SCompFmt0 (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328150"
---
# <a name="scompfmt0-structure"></a><span data-ttu-id="eec7e-103">Struttura SCompFmt0</span><span class="sxs-lookup"><span data-stu-id="eec7e-103">SCompFmt0 structure</span></span>

> [!Note]  
> <span data-ttu-id="eec7e-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="eec7e-104">\[Deprecated.</span></span> <span data-ttu-id="eec7e-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eec7e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eec7e-106">Contiene informazioni sul formato per la ricompressione intelligente.</span><span class="sxs-lookup"><span data-stu-id="eec7e-106">Contains format information for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec7e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eec7e-107">Syntax</span></span>


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a><span data-ttu-id="eec7e-108">Members</span><span class="sxs-lookup"><span data-stu-id="eec7e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="eec7e-109">**nFormatId**</span><span class="sxs-lookup"><span data-stu-id="eec7e-109">**nFormatId**</span></span>
</dt> <dd>

<span data-ttu-id="eec7e-110">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="eec7e-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="eec7e-111">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="eec7e-111">**MediaType**</span></span>
</dt> <dd>

<span data-ttu-id="eec7e-112">[**Am \_ Struttura del \_ tipo di supporto**](/windows/win32/api/strmif/ns-strmif-am_media_type) che descrive il formato di compressione.</span><span class="sxs-lookup"><span data-stu-id="eec7e-112">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that describes the compression format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eec7e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eec7e-113">Requirements</span></span>



| <span data-ttu-id="eec7e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eec7e-114">Requirement</span></span> | <span data-ttu-id="eec7e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="eec7e-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eec7e-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eec7e-116">Header</span></span><br/> | <dl> <span data-ttu-id="eec7e-117"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="eec7e-117"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eec7e-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eec7e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eec7e-119">**IAMTimelineGroup::GetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="eec7e-119">**IAMTimelineGroup::GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[<span data-ttu-id="eec7e-120">**IAMTimelineGroup::SetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="eec7e-120">**IAMTimelineGroup::SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




