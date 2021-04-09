---
title: Messaggio TB_ISBUTTONPRESSED (COMmctrl. h)
description: Determina se viene premuto il pulsante specificato in una barra degli strumenti.
ms.assetid: b8e2434c-24c2-47eb-b243-ffdaf31d5b8f
keywords:
- Controlli di Windows Message TB_ISBUTTONPRESSED
topic_type:
- apiref
api_name:
- TB_ISBUTTONPRESSED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc2e6ec7b56ce205f3d89bc22a7c9dbbee90b1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119331"
---
# <a name="tb_isbuttonpressed-message"></a><span data-ttu-id="6b79c-104">TB \_ ISBUTTONPRESSED messaggio</span><span class="sxs-lookup"><span data-stu-id="6b79c-104">TB\_ISBUTTONPRESSED message</span></span>

<span data-ttu-id="6b79c-105">Determina se viene premuto il pulsante specificato in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="6b79c-105">Determines whether the specified button in a toolbar is pressed.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b79c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b79c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b79c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b79c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b79c-108">Identificatore del comando del pulsante.</span><span class="sxs-lookup"><span data-stu-id="6b79c-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="6b79c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b79c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6b79c-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6b79c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b79c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b79c-111">Return value</span></span>

<span data-ttu-id="6b79c-112">Restituisce un valore diverso da zero se il pulsante è premuto oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6b79c-112">Returns nonzero if the button is pressed, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b79c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b79c-113">Requirements</span></span>



| <span data-ttu-id="6b79c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b79c-114">Requirement</span></span> | <span data-ttu-id="6b79c-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6b79c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b79c-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b79c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6b79c-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b79c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b79c-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b79c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6b79c-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b79c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b79c-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b79c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b79c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b79c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





