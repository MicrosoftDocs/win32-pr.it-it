---
title: Messaggio CB_GETEDITSEL (winuser. h)
description: Ottiene le posizioni dei caratteri iniziali e finali della selezione corrente nel controllo di modifica di una casella combinata.
ms.assetid: 72b64135-e35a-4f72-9fc7-e6bedf495f23
keywords:
- Controlli di Windows Message CB_GETEDITSEL
topic_type:
- apiref
api_name:
- CB_GETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319ce4a3c7a5a61903d4fc3bf04eed223e749787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048361"
---
# <a name="cb_geteditsel-message"></a><span data-ttu-id="8495a-104">\_Messaggio GETEDITSEL CB</span><span class="sxs-lookup"><span data-stu-id="8495a-104">CB\_GETEDITSEL message</span></span>

<span data-ttu-id="8495a-105">Ottiene le posizioni dei caratteri iniziali e finali della selezione corrente nel controllo di modifica di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="8495a-105">Gets the starting and ending character positions of the current selection in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="8495a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8495a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8495a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8495a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8495a-108">Puntatore a un valore **DWORD** che riceve la posizione iniziale della selezione.</span><span class="sxs-lookup"><span data-stu-id="8495a-108">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="8495a-109">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8495a-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8495a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8495a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8495a-111">Puntatore a un valore **DWORD** che riceve la posizione finale della selezione.</span><span class="sxs-lookup"><span data-stu-id="8495a-111">A pointer to a **DWORD** value that receives the ending position of the selection.</span></span> <span data-ttu-id="8495a-112">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8495a-112">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8495a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8495a-113">Return value</span></span>

<span data-ttu-id="8495a-114">Il valore restituito è un valore **DWORD** in base zero con la posizione iniziale della selezione in [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e con la posizione finale del primo carattere dopo l'ultimo carattere selezionato in [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8495a-114">The return value is a zero-based **DWORD** value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and with the ending position of the first character after the last selected character in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="8495a-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="8495a-115">Examples</span></span>

<span data-ttu-id="8495a-116">Nell'esempio di codice seguente vengono illustrati due modi per recuperare l'intervallo di selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="8495a-116">The following code example shows two ways of retrieving the current selection range.</span></span>


```C++
DWORD start, end;

// Get the range from [out] parameters.
// hwnd is the handle of the combo box control.
SendMessage(hwnd, CB_GETEDITSEL, (WPARAM)&start, (LPARAM)&end;

// Get the range from the return value.
DWORD range = SendMessage(hwnd, CB_GETEDITSEL, NULL, NULL);
start = LOWORD(range);
end = HIWORD(range);
```



## <a name="requirements"></a><span data-ttu-id="8495a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8495a-117">Requirements</span></span>



| <span data-ttu-id="8495a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8495a-118">Requirement</span></span> | <span data-ttu-id="8495a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8495a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8495a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8495a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8495a-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8495a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8495a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8495a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8495a-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8495a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8495a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8495a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8495a-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8495a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8495a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8495a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="8495a-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="8495a-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8495a-128">**CB \_ SETEDITSEL**</span><span class="sxs-lookup"><span data-stu-id="8495a-128">**CB\_SETEDITSEL**</span></span>](cb-seteditsel.md)
</dt> <dt>

<span data-ttu-id="8495a-129">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="8495a-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="8495a-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8495a-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="8495a-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8495a-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

