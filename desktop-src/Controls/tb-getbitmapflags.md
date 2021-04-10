---
title: Messaggio TB_GETBITMAPFLAGS (COMmctrl. h)
description: Recupera i flag che descrivono il tipo di bitmap da utilizzare.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- Controlli di Windows Message TB_GETBITMAPFLAGS
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e21b5b14fa57d6e454c997cbd0e80ac5716d230e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121719"
---
# <a name="tb_getbitmapflags-message"></a><span data-ttu-id="7c9d8-104">TB \_ GETBITMAPFLAGS messaggio</span><span class="sxs-lookup"><span data-stu-id="7c9d8-104">TB\_GETBITMAPFLAGS message</span></span>

<span data-ttu-id="7c9d8-105">Recupera i flag che descrivono il tipo di bitmap da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7c9d8-105">Retrieves the flags that describe the type of bitmap to be used.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c9d8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c9d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c9d8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c9d8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7c9d8-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7c9d8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7c9d8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c9d8-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7c9d8-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7c9d8-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c9d8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c9d8-111">Return value</span></span>

<span data-ttu-id="7c9d8-112">Restituisce un valore **DWORD** che descrive il tipo di bitmap da usare.</span><span class="sxs-lookup"><span data-stu-id="7c9d8-112">Returns a **DWORD** value that describes the type of bitmap that should be used.</span></span> <span data-ttu-id="7c9d8-113">Se il valore restituito è \_ impostato su TBBF large flag, le applicazioni devono usare bitmap di grandi dimensioni (24 x 24). in caso contrario, le applicazioni devono usare bitmap di piccole dimensioni (16 x 16).</span><span class="sxs-lookup"><span data-stu-id="7c9d8-113">If this return value has the TBBF\_LARGE flag set, applications should use large bitmaps (24 x 24); otherwise, applications should use small bitmaps (16 x 16).</span></span> <span data-ttu-id="7c9d8-114">Tutti gli altri bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="7c9d8-114">All other bits are reserved.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c9d8-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c9d8-115">Remarks</span></span>

<span data-ttu-id="7c9d8-116">Il valore restituito da **TB \_ GETBITMAPFLAGS** è solo consultivo.</span><span class="sxs-lookup"><span data-stu-id="7c9d8-116">The value returned by **TB\_GETBITMAPFLAGS** is only advisory.</span></span> <span data-ttu-id="7c9d8-117">Il controllo Toolbar consiglia le bitmap di grandi dimensioni o piccole in base al fatto che l'utente abbia scelto caratteri di grandi dimensioni o piccoli.</span><span class="sxs-lookup"><span data-stu-id="7c9d8-117">The toolbar control recommends large or small bitmaps based upon whether the user has chosen large or small fonts.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c9d8-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c9d8-118">Requirements</span></span>



| <span data-ttu-id="7c9d8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c9d8-119">Requirement</span></span> | <span data-ttu-id="7c9d8-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7c9d8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c9d8-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c9d8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7c9d8-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c9d8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c9d8-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c9d8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7c9d8-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c9d8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c9d8-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c9d8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c9d8-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c9d8-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





