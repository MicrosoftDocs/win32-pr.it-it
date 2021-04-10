---
title: Messaggio STM_GETICON (winuser. h)
description: Un'applicazione invia il \_ messaggio STM GetIcon per recuperare un handle per l'icona associata a un controllo statico con \_ stile icona SS.
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- Controlli di Windows Message STM_GETICON
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119231"
---
# <a name="stm_geticon-message"></a><span data-ttu-id="5dee6-104">\_Messaggio STM GETicon</span><span class="sxs-lookup"><span data-stu-id="5dee6-104">STM\_GETICON message</span></span>

<span data-ttu-id="5dee6-105">Un'applicazione invia il messaggio **STM \_ GetIcon** per recuperare un handle per l'icona associata a un controllo statico con \_ stile icona SS.</span><span class="sxs-lookup"><span data-stu-id="5dee6-105">An application sends the **STM\_GETICON** message to retrieve a handle to the icon associated with a static control that has the SS\_ICON style.</span></span>

## <a name="parameters"></a><span data-ttu-id="5dee6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5dee6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dee6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5dee6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5dee6-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5dee6-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5dee6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5dee6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5dee6-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5dee6-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dee6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5dee6-111">Return value</span></span>

<span data-ttu-id="5dee6-112">Il valore restituito è un handle per l'icona oppure **null** se il controllo statico non dispone di un'icona associata o se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="5dee6-112">The return value is a handle to the icon, or **NULL** if either the static control has no associated icon or if an error occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dee6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5dee6-113">Requirements</span></span>



| <span data-ttu-id="5dee6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dee6-114">Requirement</span></span> | <span data-ttu-id="5dee6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5dee6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dee6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5dee6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5dee6-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5dee6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5dee6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5dee6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5dee6-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5dee6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5dee6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5dee6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dee6-121"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5dee6-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5dee6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5dee6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dee6-123">**ICONA di STM \_**</span><span class="sxs-lookup"><span data-stu-id="5dee6-123">**STM\_SETICON**</span></span>](stm-seticon.md)
</dt> </dl>

 

 





