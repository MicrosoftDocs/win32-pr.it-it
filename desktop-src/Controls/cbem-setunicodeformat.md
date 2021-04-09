---
title: Messaggio CBEM_SETUNICODEFORMAT (COMmctrl. h)
description: Imposta il flag di formato carattere UNICODE per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.
ms.assetid: 4811709b-1639-4468-8598-97d9dc8d9057
keywords:
- Controlli di Windows Message CBEM_SETUNICODEFORMAT
topic_type:
- apiref
api_name:
- CBEM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89540d4e942b8b705685c13addeeb17adf0b4f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121159"
---
# <a name="cbem_setunicodeformat-message"></a><span data-ttu-id="eaf24-105">\_Messaggio CBEM SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="eaf24-105">CBEM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="eaf24-106">Imposta il flag di formato carattere UNICODE per il controllo.</span><span class="sxs-lookup"><span data-stu-id="eaf24-106">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="eaf24-107">Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.</span><span class="sxs-lookup"><span data-stu-id="eaf24-107">This message enables you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="eaf24-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eaf24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaf24-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eaf24-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eaf24-110">Determina il set di caratteri utilizzato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="eaf24-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="eaf24-111">Se questo valore è diverso da zero, il controllo utilizzerà caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="eaf24-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="eaf24-112">Se questo valore è zero, il controllo utilizzerà caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="eaf24-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="eaf24-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eaf24-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eaf24-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="eaf24-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaf24-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eaf24-115">Return value</span></span>

<span data-ttu-id="eaf24-116">Restituisce il flag di formato Unicode precedente per il controllo.</span><span class="sxs-lookup"><span data-stu-id="eaf24-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaf24-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="eaf24-117">Remarks</span></span>

<span data-ttu-id="eaf24-118">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="eaf24-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf24-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eaf24-119">Requirements</span></span>



| <span data-ttu-id="eaf24-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="eaf24-120">Requirement</span></span> | <span data-ttu-id="eaf24-121">Valore</span><span class="sxs-lookup"><span data-stu-id="eaf24-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf24-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eaf24-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf24-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eaf24-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eaf24-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eaf24-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf24-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eaf24-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eaf24-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eaf24-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eaf24-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eaf24-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaf24-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eaf24-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf24-129">**\_GETUNICODEFORMAT CBEM**</span><span class="sxs-lookup"><span data-stu-id="eaf24-129">**CBEM\_GETUNICODEFORMAT**</span></span>](cbem-getunicodeformat.md)
</dt> </dl>

 

 





