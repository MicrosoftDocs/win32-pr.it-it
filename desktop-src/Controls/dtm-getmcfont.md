---
title: Messaggio DTM_GETMCFONT (COMmctrl. h)
description: Ottiene il tipo di carattere attualmente utilizzato dal controllo Calendar Month del controllo di selezione data e ora (DTP). È possibile inviare questo messaggio in modo esplicito o usare la \_ macro DateTime GetMonthCalFont.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- Controlli di Windows Message DTM_GETMCFONT
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d799d5dbbe5e3a4cdf7eede871f9aeac451d17a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874369"
---
# <a name="dtm_getmcfont-message"></a><span data-ttu-id="3d7e6-105">\_Messaggio GETMCFONT DTM</span><span class="sxs-lookup"><span data-stu-id="3d7e6-105">DTM\_GETMCFONT message</span></span>

<span data-ttu-id="3d7e6-106">Ottiene il tipo di carattere attualmente utilizzato dal controllo Calendar Month del controllo di selezione data e ora (DTP).</span><span class="sxs-lookup"><span data-stu-id="3d7e6-106">Gets the font that the date and time picker (DTP) control's child month calendar control is currently using.</span></span> <span data-ttu-id="3d7e6-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) .</span><span class="sxs-lookup"><span data-stu-id="3d7e6-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3d7e6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d7e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d7e6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3d7e6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3d7e6-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3d7e6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3d7e6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d7e6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3d7e6-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3d7e6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d7e6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d7e6-113">Return value</span></span>

<span data-ttu-id="3d7e6-114">Restituisce un valore HFONT che rappresenta l'handle per il tipo di carattere corrente.</span><span class="sxs-lookup"><span data-stu-id="3d7e6-114">Returns an HFONT value that is the handle to the current font.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d7e6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d7e6-115">Requirements</span></span>



| <span data-ttu-id="3d7e6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d7e6-116">Requirement</span></span> | <span data-ttu-id="3d7e6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3d7e6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d7e6-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d7e6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3d7e6-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3d7e6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3d7e6-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d7e6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3d7e6-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3d7e6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3d7e6-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d7e6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d7e6-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d7e6-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





