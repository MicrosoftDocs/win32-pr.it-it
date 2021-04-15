---
title: Costanti TS_SHIFT_ (Textstor. h)
description: Le \_ costanti di spostamento di Servizi terminal \_ vengono utilizzate dall'interfaccia IAnchor per la manipolazione del testo nascosto e del conteggio dei caratteri.
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400642"
---
# <a name="ts_shift_-constants"></a><span data-ttu-id="681ad-103">\_Costanti di spostamento di Servizi terminal \_ \*</span><span class="sxs-lookup"><span data-stu-id="681ad-103">TS\_SHIFT\_\* Constants</span></span>

<span data-ttu-id="681ad-104">Le costanti di spostamento di Servizi terminal \_ \_ \* vengono utilizzate dall'interfaccia **IAnchor** per la manipolazione del testo nascosto e del conteggio dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="681ad-104">The TS\_Shift\_\* constants are used by the **IAnchor** interface for manipulation of hidden text and character counting.</span></span>



| <span data-ttu-id="681ad-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="681ad-105">Constant/value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="681ad-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="681ad-106">Description</span></span>                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <span data-ttu-id="681ad-107"><dt>**Servizi terminal \_ Conteggio di spostamento \_ \_ nascosto**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="681ad-107"><dt>**TS\_SHIFT\_COUNT\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="681ad-108">Specifica che l'ancoraggio verrà spostato al limite dell'area successiva, incluso il limite di un'area di testo nascosta.</span><span class="sxs-lookup"><span data-stu-id="681ad-108">Specifies that the anchor will be shifted to the next region boundary, including the boundary of a hidden text region.</span></span> <span data-ttu-id="681ad-109">Se non è impostato, l'ancoraggio verrà spostato oltre qualsiasi testo nascosto adiacente fino a quando non viene trovata un'area di testo visibile.</span><span class="sxs-lookup"><span data-stu-id="681ad-109">If not set, the anchor will be shifted past any adjacent hidden text until a region of visible text is found.</span></span><br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <span data-ttu-id="681ad-110"><dt>**Servizi terminal \_ MAIUSC \_ ALT \_ nascosto**</dt> <dt>(0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="681ad-110"><dt>**TS\_SHIFT\_HALT\_HIDDEN**</dt> <dt>( 0x2 )</dt></span></span> </dl>    | <span data-ttu-id="681ad-111">Non usato.</span><span class="sxs-lookup"><span data-stu-id="681ad-111">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <span data-ttu-id="681ad-112"><dt>**Servizi terminal \_ MAIUSC \_ ALT \_ visibile**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="681ad-112"><dt>**TS\_SHIFT\_HALT\_VISIBLE**</dt> <dt>( 0x4 )</dt></span></span> </dl> | <span data-ttu-id="681ad-113">Non usato.</span><span class="sxs-lookup"><span data-stu-id="681ad-113">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <span data-ttu-id="681ad-114"><dt>**Servizi terminal \_ \_ \_ Solo conteggio MAIUSC**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="681ad-114"><dt>**TS\_SHIFT\_COUNT\_ONLY**</dt> <dt>( 0x8 )</dt></span></span> </dl>       | <span data-ttu-id="681ad-115">L'ancoraggio non viene spostato.</span><span class="sxs-lookup"><span data-stu-id="681ad-115">The anchor is not shifted.</span></span><br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="681ad-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="681ad-116">Requirements</span></span>



| <span data-ttu-id="681ad-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="681ad-117">Requirement</span></span> | <span data-ttu-id="681ad-118">Valore</span><span class="sxs-lookup"><span data-stu-id="681ad-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="681ad-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="681ad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="681ad-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="681ad-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="681ad-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="681ad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="681ad-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="681ad-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="681ad-123">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="681ad-123">Redistributable</span></span><br/>          | <span data-ttu-id="681ad-124">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="681ad-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="681ad-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="681ad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="681ad-126"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="681ad-126"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="681ad-127">IDL</span><span class="sxs-lookup"><span data-stu-id="681ad-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="681ad-128"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="681ad-128"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="681ad-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="681ad-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="681ad-130">IAnchor::ShiftRegion</span><span class="sxs-lookup"><span data-stu-id="681ad-130">IAnchor::ShiftRegion</span></span>](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 





