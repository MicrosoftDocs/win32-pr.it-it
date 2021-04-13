---
description: Contiene un vettore di inizializzazione (IV) per la crittografia a blocchi a 128 bit Advanced Encryption Standard CTR (AES-CTR).
ms.assetid: 2ee738c2-d56c-4a50-94b8-b7180918aa8c
title: Struttura D3DAES_CTR_IV (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAES_CTR_IV
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6e0d543fb0e57ae34f181e7ff0f40a1a1f8222b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342541"
---
# <a name="d3daes_ctr_iv-structure"></a><span data-ttu-id="d0eb8-103">\_Struttura D3DAES CTR \_ IV</span><span class="sxs-lookup"><span data-stu-id="d0eb8-103">D3DAES\_CTR\_IV structure</span></span>

<span data-ttu-id="d0eb8-104">Contiene un vettore di inizializzazione (IV) per la crittografia a blocchi a 128 bit Advanced Encryption Standard CTR (AES-CTR).</span><span class="sxs-lookup"><span data-stu-id="d0eb8-104">Contains an initialization vector (IV) for 128-bit Advanced Encryption Standard CTR mode (AES-CTR) block cipher encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0eb8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0eb8-105">Syntax</span></span>


```C++
typedef struct _D3DAES_CTR_IV {
  UINT64 IV;
  UINT64 Count;
} D3DAES_CTR_IV;
```



## <a name="members"></a><span data-ttu-id="d0eb8-106">Members</span><span class="sxs-lookup"><span data-stu-id="d0eb8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d0eb8-107">**IV**</span><span class="sxs-lookup"><span data-stu-id="d0eb8-107">**IV**</span></span>
</dt> <dd>

<span data-ttu-id="d0eb8-108">IV, nel formato big-endian.</span><span class="sxs-lookup"><span data-stu-id="d0eb8-108">The IV, in big-endian format.</span></span>

</dd> <dt>

<span data-ttu-id="d0eb8-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="d0eb8-109">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="d0eb8-110">Conteggio dei blocchi, nel formato big-endian.</span><span class="sxs-lookup"><span data-stu-id="d0eb8-110">The block count, in big-endian format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0eb8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0eb8-111">Remarks</span></span>

<span data-ttu-id="d0eb8-112">La struttura **D3DAES \_ CTR \_ IV** e la struttura [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) sono equivalenti.</span><span class="sxs-lookup"><span data-stu-id="d0eb8-112">The **D3DAES\_CTR\_IV** structure and the [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv) structure are equivalent.</span></span>

<span data-ttu-id="d0eb8-113">Per informazioni dettagliate, vedere [**DXVA2 \_ AES \_ CTR \_ IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span><span class="sxs-lookup"><span data-stu-id="d0eb8-113">For details, see [**DXVA2\_AES\_CTR\_IV**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_aes_ctr_iv).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0eb8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0eb8-114">Requirements</span></span>



| <span data-ttu-id="d0eb8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0eb8-115">Requirement</span></span> | <span data-ttu-id="d0eb8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d0eb8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0eb8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0eb8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d0eb8-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d0eb8-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d0eb8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0eb8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d0eb8-120">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d0eb8-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d0eb8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0eb8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0eb8-122"><dt>D3d9types. h (include d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0eb8-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0eb8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0eb8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0eb8-124">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="d0eb8-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




