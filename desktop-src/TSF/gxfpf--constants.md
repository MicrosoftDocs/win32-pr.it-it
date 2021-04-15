---
title: Costanti GXFPF_ (Textstor. h)
description: GXFPF \_ \ Constants consente di specificare la posizione del carattere da restituire in base alle coordinate dello schermo del punto rispetto a un rettangolo delimitatore di caratteri.
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475814"
---
# <a name="gxfpf_-constants"></a><span data-ttu-id="f16e0-103">\_ \* Costanti GXFPF</span><span class="sxs-lookup"><span data-stu-id="f16e0-103">GXFPF\_\* Constants</span></span>

<span data-ttu-id="f16e0-104">Le \_ \* costanti GXFPF specificano la posizione del carattere da restituire in base alle coordinate dello schermo del punto rispetto a un rettangolo delimitatore di caratteri.</span><span class="sxs-lookup"><span data-stu-id="f16e0-104">GXFPF\_\* constants specify the character position to return based on the screen coordinates of the point relative to a character bounding box.</span></span>



| <span data-ttu-id="f16e0-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="f16e0-105">Constant/value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="f16e0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f16e0-106">Description</span></span>                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <span data-ttu-id="f16e0-107"><dt>**GXFPF \_ ROUND \_ più vicino**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="f16e0-107"><dt>**GXFPF\_ROUND\_NEAREST**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="f16e0-108">Se le coordinate dello schermo del punto sono contenute in un rettangolo delimitatore di caratteri, la posizione del carattere restituita è il bordo delimitatore più vicino alle coordinate dello schermo del punto.</span><span class="sxs-lookup"><span data-stu-id="f16e0-108">If the screen coordinates of the point are contained in a character bounding box, the character position returned is the bounding edge closest to the screen coordinates of the point.</span></span><br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <span data-ttu-id="f16e0-109"><dt>**GXFPF \_ PIÙ vicino**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="f16e0-109"><dt>**GXFPF\_NEAREST**</dt> <dt>( 0x2 )</dt></span></span> </dl>                    | <span data-ttu-id="f16e0-110">Se le coordinate dello schermo del punto non sono contenute in un rettangolo delimitatore di caratteri, viene restituita la posizione del carattere più vicina.</span><span class="sxs-lookup"><span data-stu-id="f16e0-110">If the screen coordinates of the point are not contained in a character bounding box, the closest character position is returned.</span></span><br/>                                                      |



## <a name="remarks"></a><span data-ttu-id="f16e0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f16e0-111">Remarks</span></span>

<span data-ttu-id="f16e0-112">I parametri *dwFlags* dei metodi [ITextStoreACP:: GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) e [ITfContextOwner:: GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) usano queste costanti.</span><span class="sxs-lookup"><span data-stu-id="f16e0-112">The *dwflags* parameters of the [ITextStoreACP::GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) and [ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) methods use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="f16e0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f16e0-113">Requirements</span></span>



| <span data-ttu-id="f16e0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f16e0-114">Requirement</span></span> | <span data-ttu-id="f16e0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f16e0-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f16e0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f16e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f16e0-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f16e0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f16e0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f16e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f16e0-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f16e0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f16e0-120">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f16e0-120">Redistributable</span></span><br/>          | <span data-ttu-id="f16e0-121">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f16e0-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="f16e0-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f16e0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f16e0-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="f16e0-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="f16e0-124">IDL</span><span class="sxs-lookup"><span data-stu-id="f16e0-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f16e0-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f16e0-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16e0-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f16e0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16e0-127">ITextStoreACP:: GetACPFromPoint</span><span class="sxs-lookup"><span data-stu-id="f16e0-127">ITextStoreACP::GetACPFromPoint</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[<span data-ttu-id="f16e0-128">ITfContextOwner::GetACPFromPoint</span><span class="sxs-lookup"><span data-stu-id="f16e0-128">ITfContextOwner::GetACPFromPoint</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





