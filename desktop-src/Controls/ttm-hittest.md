---
title: Messaggio TTM_HITTEST (COMmctrl. h)
description: Verifica un punto per determinare se si trova all'interno del rettangolo di delimitazione dello strumento specificato e, in caso contrario, recupera le informazioni sullo strumento.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- Controlli di Windows Message TTM_HITTEST
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476781"
---
# <a name="ttm_hittest-message"></a><span data-ttu-id="6ab2e-104">\_Messaggio TTM HITTEST</span><span class="sxs-lookup"><span data-stu-id="6ab2e-104">TTM\_HITTEST message</span></span>

<span data-ttu-id="6ab2e-105">Verifica un punto per determinare se si trova all'interno del rettangolo di delimitazione dello strumento specificato e, in caso contrario, recupera le informazioni sullo strumento.</span><span class="sxs-lookup"><span data-stu-id="6ab2e-105">Tests a point to determine whether it is within the bounding rectangle of the specified tool and, if it is, retrieves information about the tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ab2e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ab2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ab2e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ab2e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6ab2e-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6ab2e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6ab2e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ab2e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6ab2e-110">Puntatore a una struttura [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) .</span><span class="sxs-lookup"><span data-stu-id="6ab2e-110">Pointer to a [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) structure.</span></span> <span data-ttu-id="6ab2e-111">Quando si invia il messaggio, il membro **HWND** deve specificare l'handle per uno strumento e il membro **PT** deve specificare le coordinate di un punto.</span><span class="sxs-lookup"><span data-stu-id="6ab2e-111">When sending the message, the **hwnd** member must specify the handle to a tool and the **pt** member must specify the coordinates of a point.</span></span> <span data-ttu-id="6ab2e-112">Se il valore restituito è **true**, il membro **ti** (una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ) riceve informazioni sullo strumento che occupa il punto.</span><span class="sxs-lookup"><span data-stu-id="6ab2e-112">If the return value is **TRUE**, the **ti** member (a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure) receives information about the tool that occupies the point.</span></span> <span data-ttu-id="6ab2e-113">Prima di inviare questo messaggio, è necessario compilare il membro **cbSize** della struttura **ti** .</span><span class="sxs-lookup"><span data-stu-id="6ab2e-113">The **cbSize** member of the **ti** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ab2e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ab2e-114">Return value</span></span>

<span data-ttu-id="6ab2e-115">Restituisce **true** se lo strumento occupa il punto specificato o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6ab2e-115">Returns **TRUE** if the tool occupies the specified point, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ab2e-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ab2e-116">Remarks</span></span>

<span data-ttu-id="6ab2e-117">Questo messaggio deve essere inviato quando per lo strumento è \_ impostato il flag di traccia ttf.</span><span class="sxs-lookup"><span data-stu-id="6ab2e-117">This message must be sent when the tool has the TTF\_TRACK flag set.</span></span> <span data-ttu-id="6ab2e-118">Per ulteriori informazioni su questo flag, vedere [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span><span class="sxs-lookup"><span data-stu-id="6ab2e-118">For more information on this flag, see [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span></span> <span data-ttu-id="6ab2e-119">Il TTM \_ HITTEST avrà esito negativo se \_ non è impostata la traccia ttf, indipendentemente dal fatto che il punto di hit si trovi nel rettangolo Tools.</span><span class="sxs-lookup"><span data-stu-id="6ab2e-119">TTM\_HITTEST will fail if TTF\_TRACK is not set, regardless if the hit point is in the tools rectangle or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab2e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ab2e-120">Requirements</span></span>



| <span data-ttu-id="6ab2e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ab2e-121">Requirement</span></span> | <span data-ttu-id="6ab2e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6ab2e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab2e-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ab2e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6ab2e-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ab2e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ab2e-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ab2e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6ab2e-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ab2e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ab2e-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ab2e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ab2e-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ab2e-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6ab2e-129">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6ab2e-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6ab2e-130">**TTM \_ HITTESTW** (Unicode) e **TTM \_ HITTESTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6ab2e-130">**TTM\_HITTESTW** (Unicode) and **TTM\_HITTESTA** (ANSI)</span></span><br/>                   |



 

 





