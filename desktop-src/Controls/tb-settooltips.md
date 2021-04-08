---
title: Messaggio TB_SETTOOLTIPS (COMmctrl. h)
description: Associa un controllo ToolTip a una barra degli strumenti.
ms.assetid: a645f1f2-9333-4e25-985a-107cffb9b97f
keywords:
- Controlli di Windows Message TB_SETTOOLTIPS
topic_type:
- apiref
api_name:
- TB_SETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781565658d2c362ca32e36736d6e2d80c3641514
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048118"
---
# <a name="tb_settooltips-message"></a><span data-ttu-id="844c8-104">\_Messaggio di SEtooltips TB</span><span class="sxs-lookup"><span data-stu-id="844c8-104">TB\_SETTOOLTIPS message</span></span>

<span data-ttu-id="844c8-105">Associa un controllo ToolTip a una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="844c8-105">Associates a tooltip control with a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="844c8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="844c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="844c8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="844c8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="844c8-108">Handle per il controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="844c8-108">Handle to the tooltip control.</span></span>

</dd> <dt>

<span data-ttu-id="844c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="844c8-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="844c8-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="844c8-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="844c8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="844c8-111">Return value</span></span>

<span data-ttu-id="844c8-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="844c8-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="844c8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="844c8-113">Remarks</span></span>

<span data-ttu-id="844c8-114">Tutti i pulsanti aggiunti a una barra degli strumenti prima di inviare il messaggio **TB \_ setooltips** non verranno registrati con il controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="844c8-114">Any buttons added to a toolbar before sending the **TB\_SETTOOLTIPS** message will not be registered with the tooltip control.</span></span>

## <a name="requirements"></a><span data-ttu-id="844c8-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="844c8-115">Requirements</span></span>



| <span data-ttu-id="844c8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="844c8-116">Requirement</span></span> | <span data-ttu-id="844c8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="844c8-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="844c8-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="844c8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="844c8-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="844c8-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="844c8-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="844c8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="844c8-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="844c8-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="844c8-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="844c8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="844c8-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="844c8-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





