---
title: Messaggio RB_MOVEBAND (COMmctrl. h)
description: Sposta una banda da un indice a un altro.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- Controlli di Windows Message RB_MOVEBAND
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475341"
---
# <a name="rb_moveband-message"></a><span data-ttu-id="84e69-104">\_Messaggio MOVEBAND RB</span><span class="sxs-lookup"><span data-stu-id="84e69-104">RB\_MOVEBAND message</span></span>

<span data-ttu-id="84e69-105">Sposta una banda da un indice a un altro.</span><span class="sxs-lookup"><span data-stu-id="84e69-105">Moves a band from one index to another.</span></span>

## <a name="parameters"></a><span data-ttu-id="84e69-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="84e69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84e69-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="84e69-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84e69-108">Indice in base zero della banda da spostare.</span><span class="sxs-lookup"><span data-stu-id="84e69-108">Zero-based index of the band to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="84e69-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="84e69-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="84e69-110">Indice in base zero della nuova posizione della banda.</span><span class="sxs-lookup"><span data-stu-id="84e69-110">Zero-based index of the new band position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84e69-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84e69-111">Return value</span></span>

<span data-ttu-id="84e69-112">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="84e69-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="84e69-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="84e69-113">Remarks</span></span>

<span data-ttu-id="84e69-114">È probabile che questo messaggio modifichi l'indice di altre bande nel controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="84e69-114">This message will most likely change the index of other bands in the rebar control.</span></span> <span data-ttu-id="84e69-115">Se una banda viene spostata dall'indice 6 all'indice 0, per tutte le bande comprese tra l'indice viene incrementato di uno.</span><span class="sxs-lookup"><span data-stu-id="84e69-115">If a band is moved from index 6 to index 0, all of the bands in between will have their index incremented by one.</span></span>

<span data-ttu-id="84e69-116">*lParam* non deve mai essere maggiore del numero di bande meno uno.</span><span class="sxs-lookup"><span data-stu-id="84e69-116">*lParam* must never be greater than the number of bands minus one.</span></span> <span data-ttu-id="84e69-117">Il numero di bande può essere ottenuto con il messaggio [**RB \_ GETBANDCOUNT**](rb-getbandcount.md) .</span><span class="sxs-lookup"><span data-stu-id="84e69-117">The number of bands can be obtained with the [**RB\_GETBANDCOUNT**](rb-getbandcount.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="84e69-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84e69-118">Requirements</span></span>



| <span data-ttu-id="84e69-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="84e69-119">Requirement</span></span> | <span data-ttu-id="84e69-120">Valore</span><span class="sxs-lookup"><span data-stu-id="84e69-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84e69-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84e69-121">Minimum supported client</span></span><br/> | <span data-ttu-id="84e69-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84e69-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84e69-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84e69-123">Minimum supported server</span></span><br/> | <span data-ttu-id="84e69-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84e69-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84e69-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84e69-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="84e69-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="84e69-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





