---
description: Specifica un riferimento a una superficie non compressa.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: Struttura DXVA_PicEntry_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305392"
---
# <a name="dxva_picentry_hevc-structure"></a><span data-ttu-id="0174c-103">\_Struttura DXVA PicEntry \_ HEVC</span><span class="sxs-lookup"><span data-stu-id="0174c-103">DXVA\_PicEntry\_HEVC structure</span></span>

<span data-ttu-id="0174c-104">Specifica un riferimento a una superficie non compressa.</span><span class="sxs-lookup"><span data-stu-id="0174c-104">Specifies a reference to an uncompressed surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0174c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0174c-105">Syntax</span></span>


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a><span data-ttu-id="0174c-106">Members</span><span class="sxs-lookup"><span data-stu-id="0174c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0174c-107">**Index7Bits**</span><span class="sxs-lookup"><span data-stu-id="0174c-107">**Index7Bits**</span></span>
</dt> <dd>

<span data-ttu-id="0174c-108">Indice che identifica una superficie non compressa.</span><span class="sxs-lookup"><span data-stu-id="0174c-108">An index that identifies an uncompressed surface .</span></span>

</dd> <dt>

<span data-ttu-id="0174c-109">**AssociatedFlag**</span><span class="sxs-lookup"><span data-stu-id="0174c-109">**AssociatedFlag**</span></span> 
</dt> <dd>

<span data-ttu-id="0174c-110">Flag a 1 bit facoltativo associato alla superficie.</span><span class="sxs-lookup"><span data-stu-id="0174c-110">Optional 1-bit flag associated with the surface.</span></span> <span data-ttu-id="0174c-111">Il significato del flag dipende dal contesto.</span><span class="sxs-lookup"><span data-stu-id="0174c-111">The meaning of the flag depends on the context.</span></span> <span data-ttu-id="0174c-112">Ad esempio, è possibile specificare se il frame di riferimento è un riferimento a lungo termine o un riferimento a breve termine.</span><span class="sxs-lookup"><span data-stu-id="0174c-112">For example, it can specify whether the reference frame is a long-term reference or a short-term reference.</span></span>

</dd> <dt>

<span data-ttu-id="0174c-113">**bPicEntry**</span><span class="sxs-lookup"><span data-stu-id="0174c-113">**bPicEntry**</span></span>
</dt> <dd>

<span data-ttu-id="0174c-114">Accede a 8 bit interi dell'Unione.</span><span class="sxs-lookup"><span data-stu-id="0174c-114">Accesses the entire 8 bits of the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0174c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0174c-115">Requirements</span></span>



| <span data-ttu-id="0174c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0174c-116">Requirement</span></span> | <span data-ttu-id="0174c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0174c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0174c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0174c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0174c-119">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0174c-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0174c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0174c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0174c-121">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0174c-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0174c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0174c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0174c-123"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="0174c-123"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0174c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0174c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0174c-125">Strutture di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0174c-125">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




