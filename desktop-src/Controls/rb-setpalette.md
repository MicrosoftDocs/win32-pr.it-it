---
title: Messaggio RB_SETPALETTE (COMmctrl. h)
description: Imposta la tavolozza corrente del controllo Rebar.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- Controlli di Windows Message RB_SETPALETTE
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964549"
---
# <a name="rb_setpalette-message"></a><span data-ttu-id="a73e8-104">\_Messaggio della tavolozza RB</span><span class="sxs-lookup"><span data-stu-id="a73e8-104">RB\_SETPALETTE message</span></span>

<span data-ttu-id="a73e8-105">Imposta la tavolozza corrente del controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="a73e8-105">Sets the rebar control's current palette.</span></span>

## <a name="parameters"></a><span data-ttu-id="a73e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a73e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a73e8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a73e8-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a73e8-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a73e8-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a73e8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a73e8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a73e8-110">Oggetto **HPALETTE** che specifica la nuova tavolozza che il controllo Rebar utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="a73e8-110">An **HPALETTE** that specifies the new palette that the rebar control will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a73e8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a73e8-111">Return value</span></span>

<span data-ttu-id="a73e8-112">Restituisce un **HPALETTE** che specifica la tavolozza precedente del controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="a73e8-112">Returns an **HPALETTE** that specifies the rebar control's previous palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="a73e8-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a73e8-113">Remarks</span></span>

<span data-ttu-id="a73e8-114">È responsabilità dell'applicazione che invia questo messaggio per eliminare il **HPALETTE** passato in questo messaggio (vedere [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span><span class="sxs-lookup"><span data-stu-id="a73e8-114">It is the responsibility of the application sending this message to delete the **HPALETTE** passed in this message (see [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span></span> <span data-ttu-id="a73e8-115">Il controllo Rebar non eliminerà un set di **HPALETTE** con questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a73e8-115">The rebar control will not delete an **HPALETTE** set with this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a73e8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a73e8-116">Requirements</span></span>



| <span data-ttu-id="a73e8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a73e8-117">Requirement</span></span> | <span data-ttu-id="a73e8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a73e8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a73e8-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a73e8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a73e8-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a73e8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a73e8-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a73e8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a73e8-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a73e8-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a73e8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a73e8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a73e8-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a73e8-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a73e8-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a73e8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73e8-126">**\_tavolozza RB**</span><span class="sxs-lookup"><span data-stu-id="a73e8-126">**RB\_GETPALETTE**</span></span>](rb-getpalette.md)
</dt> </dl>

 

