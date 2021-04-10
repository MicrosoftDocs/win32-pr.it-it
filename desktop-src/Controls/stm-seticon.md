---
title: Messaggio STM_SETICON (winuser. h)
description: Un'applicazione invia il \_ messaggio dell'icona STM per associare un'icona a un controllo icona.
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- Controlli di Windows Message STM_SETICON
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047916"
---
# <a name="stm_seticon-message"></a><span data-ttu-id="fd1c8-104">\_Messaggio di icona STM</span><span class="sxs-lookup"><span data-stu-id="fd1c8-104">STM\_SETICON message</span></span>

<span data-ttu-id="fd1c8-105">Un'applicazione invia il messaggio dell' **\_ icona STM** per associare un'icona a un controllo icona.</span><span class="sxs-lookup"><span data-stu-id="fd1c8-105">An application sends the **STM\_SETICON** message to associate an icon with an icon control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fd1c8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd1c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd1c8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fd1c8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd1c8-108">Handle per l'icona da associare al controllo icona.</span><span class="sxs-lookup"><span data-stu-id="fd1c8-108">Handle to the icon to associate with the icon control.</span></span>

</dd> <dt>

<span data-ttu-id="fd1c8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fd1c8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fd1c8-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="fd1c8-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd1c8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd1c8-111">Return value</span></span>

<span data-ttu-id="fd1c8-112">Il valore restituito è un handle per l'icona associata in precedenza al controllo icona oppure zero se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="fd1c8-112">The return value is a handle to the icon previously associated with the icon control, or zero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd1c8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd1c8-113">Requirements</span></span>



| <span data-ttu-id="fd1c8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd1c8-114">Requirement</span></span> | <span data-ttu-id="fd1c8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fd1c8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd1c8-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd1c8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fd1c8-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd1c8-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fd1c8-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd1c8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fd1c8-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd1c8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fd1c8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd1c8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd1c8-121"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd1c8-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd1c8-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd1c8-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd1c8-123">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="fd1c8-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fd1c8-124">**\_icona GetIcon STM**</span><span class="sxs-lookup"><span data-stu-id="fd1c8-124">**STM\_GETICON**</span></span>](stm-geticon.md)
</dt> <dt>

<span data-ttu-id="fd1c8-125">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="fd1c8-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="fd1c8-126">**LoadIcon**</span><span class="sxs-lookup"><span data-stu-id="fd1c8-126">**LoadIcon**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

