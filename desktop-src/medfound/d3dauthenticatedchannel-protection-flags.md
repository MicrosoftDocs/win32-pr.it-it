---
description: Specifica il livello di protezione per il contenuto video.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: Struttura D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305450"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a><span data-ttu-id="b7ef6-103">Struttura di flag di \_ protezione D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="b7ef6-103">D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS structure</span></span>

<span data-ttu-id="b7ef6-104">Specifica il livello di protezione per il contenuto video.</span><span class="sxs-lookup"><span data-stu-id="b7ef6-104">Specifies the protection level for video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7ef6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7ef6-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a><span data-ttu-id="b7ef6-106">Members</span><span class="sxs-lookup"><span data-stu-id="b7ef6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b7ef6-107">**ProtectionEnabled**</span><span class="sxs-lookup"><span data-stu-id="b7ef6-107">**ProtectionEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="b7ef6-108">Se è 1, la protezione del contenuto video è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b7ef6-108">If 1, video content protection is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef6-109">**OverlayOrFullscreenRequired**</span><span class="sxs-lookup"><span data-stu-id="b7ef6-109">**OverlayOrFullscreenRequired**</span></span>
</dt> <dd>

<span data-ttu-id="b7ef6-110">Se è 1, l'applicazione richiede che il video venga visualizzato utilizzando una sovrapposizione hardware o una modalità esclusiva a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="b7ef6-110">If 1, the application requires video to be displayed using either a hardware overlay or full-screen exclusive mode.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef6-111">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="b7ef6-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b7ef6-112">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b7ef6-112">Reserved.</span></span> <span data-ttu-id="b7ef6-113">Impostare tutti i bit su zero.</span><span class="sxs-lookup"><span data-stu-id="b7ef6-113">Set all bits to zero.</span></span>

</dd> <dt>

<span data-ttu-id="b7ef6-114">**Valore**</span><span class="sxs-lookup"><span data-stu-id="b7ef6-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="b7ef6-115">Utilizzare questo membro per accedere a tutti i bit nell'Unione.</span><span class="sxs-lookup"><span data-stu-id="b7ef6-115">Use this member to access all of the bits in the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7ef6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7ef6-116">Requirements</span></span>



| <span data-ttu-id="b7ef6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7ef6-117">Requirement</span></span> | <span data-ttu-id="b7ef6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b7ef6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ef6-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7ef6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b7ef6-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b7ef6-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b7ef6-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7ef6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b7ef6-122">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7ef6-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b7ef6-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7ef6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7ef6-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7ef6-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7ef6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7ef6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7ef6-126">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="b7ef6-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




