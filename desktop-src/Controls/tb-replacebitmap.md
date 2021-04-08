---
title: Messaggio TB_REPLACEBITMAP (COMmctrl. h)
description: Sostituisce una bitmap esistente con una nuova bitmap.
ms.assetid: abad5c7a-ebdd-46b5-a465-fe64ff8eb127
keywords:
- Controlli di Windows Message TB_REPLACEBITMAP
topic_type:
- apiref
api_name:
- TB_REPLACEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0216d73f70f9bef8230d7e725834d63d60012798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874210"
---
# <a name="tb_replacebitmap-message"></a><span data-ttu-id="145f8-104">TB \_ REPLACEBITMAP messaggio</span><span class="sxs-lookup"><span data-stu-id="145f8-104">TB\_REPLACEBITMAP message</span></span>

<span data-ttu-id="145f8-105">Sostituisce una bitmap esistente con una nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="145f8-105">Replaces an existing bitmap with a new bitmap.</span></span>

## <a name="parameters"></a><span data-ttu-id="145f8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="145f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="145f8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="145f8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="145f8-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="145f8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="145f8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="145f8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="145f8-110">Puntatore a una struttura [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) che contiene le informazioni della bitmap da sostituire e la nuova bitmap.</span><span class="sxs-lookup"><span data-stu-id="145f8-110">Pointer to a [**TBREPLACEBITMAP**](/windows/desktop/api/Commctrl/ns-commctrl-tbreplacebitmap) structure that contains the information of the bitmap to be replaced and the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="145f8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="145f8-111">Return value</span></span>

<span data-ttu-id="145f8-112">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="145f8-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="145f8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="145f8-113">Requirements</span></span>



| <span data-ttu-id="145f8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="145f8-114">Requirement</span></span> | <span data-ttu-id="145f8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="145f8-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="145f8-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="145f8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="145f8-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="145f8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="145f8-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="145f8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="145f8-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="145f8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="145f8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="145f8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="145f8-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="145f8-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





