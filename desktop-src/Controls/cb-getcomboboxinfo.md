---
title: Messaggio CB_GETCOMBOBOXINFO (winuser. h)
description: Ottiene informazioni sulla casella combinata specificata.
ms.assetid: 3239dfa8-7301-48e3-ba8e-29c5d5f43b39
keywords:
- Controlli di Windows Message CB_GETCOMBOBOXINFO
topic_type:
- apiref
api_name:
- CB_GETCOMBOBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd7052ef4feca8a8704258c7c34d6516c7cd6cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475407"
---
# <a name="cb_getcomboboxinfo-message"></a><span data-ttu-id="710d6-104">\_Messaggio GETCOMBOBOXINFO CB</span><span class="sxs-lookup"><span data-stu-id="710d6-104">CB\_GETCOMBOBOXINFO message</span></span>

<span data-ttu-id="710d6-105">Ottiene informazioni sulla casella combinata specificata.</span><span class="sxs-lookup"><span data-stu-id="710d6-105">Gets information about the specified combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="710d6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="710d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="710d6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="710d6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="710d6-108">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="710d6-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="710d6-109">*lParam* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="710d6-109">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="710d6-110">Puntatore a una struttura [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) che riceve le informazioni.</span><span class="sxs-lookup"><span data-stu-id="710d6-110">A pointer to a [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="710d6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="710d6-111">Return value</span></span>

<span data-ttu-id="710d6-112">Se la funzione ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="710d6-112">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="710d6-113">Se la funzione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="710d6-113">If the function fails, the return value is zero.</span></span> <span data-ttu-id="710d6-114">Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="710d6-114">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="710d6-115">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="710d6-115">Remarks</span></span>

<span data-ttu-id="710d6-116">Questo messaggio è equivalente a [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span><span class="sxs-lookup"><span data-stu-id="710d6-116">This message is equivalent to [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).</span></span>

## <a name="requirements"></a><span data-ttu-id="710d6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="710d6-117">Requirements</span></span>



| <span data-ttu-id="710d6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="710d6-118">Requirement</span></span> | <span data-ttu-id="710d6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="710d6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="710d6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="710d6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="710d6-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="710d6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="710d6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="710d6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="710d6-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="710d6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="710d6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="710d6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="710d6-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="710d6-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="710d6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="710d6-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="710d6-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="710d6-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="710d6-128">**COMBOBOXINFO**</span><span class="sxs-lookup"><span data-stu-id="710d6-128">**COMBOBOXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-comboboxinfo)
</dt> <dt>

[<span data-ttu-id="710d6-129">**GetComboBoxInfo**</span><span class="sxs-lookup"><span data-stu-id="710d6-129">**GetComboBoxInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)
</dt> </dl>

 

