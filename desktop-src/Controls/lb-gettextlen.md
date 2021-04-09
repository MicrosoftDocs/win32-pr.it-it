---
title: Messaggio LB_GETTEXTLEN (winuser. h)
description: Ottiene la lunghezza di una stringa in una casella di riepilogo.
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- Controlli di Windows Message LB_GETTEXTLEN
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1f76bf3574b09b76d5f1010dcb59c8245555dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119590"
---
# <a name="lb_gettextlen-message"></a><span data-ttu-id="0826f-104">\_Messaggio GETTEXTLEN lb</span><span class="sxs-lookup"><span data-stu-id="0826f-104">LB\_GETTEXTLEN message</span></span>

<span data-ttu-id="0826f-105">Ottiene la lunghezza di una stringa in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="0826f-105">Gets the length of a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="0826f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0826f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0826f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0826f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0826f-108">Indice in base zero della stringa.</span><span class="sxs-lookup"><span data-stu-id="0826f-108">The zero-based index of the string.</span></span>

<span data-ttu-id="0826f-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="0826f-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="0826f-110">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="0826f-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="0826f-111">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="0826f-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="0826f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0826f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0826f-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="0826f-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0826f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0826f-114">Return value</span></span>

<span data-ttu-id="0826f-115">Il valore restituito è la lunghezza della stringa, in **TCHAR** s, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="0826f-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="0826f-116">In determinate condizioni, questo valore può essere effettivamente maggiore della lunghezza del testo.</span><span class="sxs-lookup"><span data-stu-id="0826f-116">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="0826f-117">Per ulteriori informazioni, vedere la sezione Osservazioni successiva.</span><span class="sxs-lookup"><span data-stu-id="0826f-117">For more information, see the following Remarks section.</span></span>

<span data-ttu-id="0826f-118">Se il parametro *wParam* non specifica un indice valido, il valore restituito è lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="0826f-118">If the *wParam* parameter does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="0826f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="0826f-119">Remarks</span></span>

<span data-ttu-id="0826f-120">In determinate condizioni, il valore restituito è maggiore della lunghezza effettiva del testo.</span><span class="sxs-lookup"><span data-stu-id="0826f-120">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="0826f-121">Questa situazione si verifica con determinate combinazioni di ANSI e Unicode ed è dovuta al sistema operativo che consente la possibile esistenza di caratteri DBCS (Double-byte character set) all'interno del testo.</span><span class="sxs-lookup"><span data-stu-id="0826f-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="0826f-122">Il valore restituito, tuttavia, sarà sempre almeno uguale alla lunghezza effettiva del testo; è pertanto possibile utilizzarlo sempre per guidare l'allocazione del buffer.</span><span class="sxs-lookup"><span data-stu-id="0826f-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="0826f-123">Questo comportamento può verificarsi quando un'applicazione utilizza funzioni ANSI e finestre di dialogo comuni che utilizzano Unicode.</span><span class="sxs-lookup"><span data-stu-id="0826f-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="0826f-124">Per ottenere la lunghezza esatta del testo, usare i messaggi [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)o [**CB \_ GETLBTEXT**](cb-getlbtext.md) oppure la funzione [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="0826f-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="0826f-125">Se la casella di riepilogo ha uno stile disegnato dal proprietario, ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , il valore restituito è sempre la dimensione, in byte, di un valore **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="0826f-125">If the list box has an owner-drawn style, but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the return value is always the size, in bytes, of a **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0826f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0826f-126">Requirements</span></span>



| <span data-ttu-id="0826f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0826f-127">Requirement</span></span> | <span data-ttu-id="0826f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0826f-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0826f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0826f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0826f-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0826f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0826f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0826f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0826f-132">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0826f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0826f-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0826f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0826f-134"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0826f-134"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0826f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0826f-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="0826f-136">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="0826f-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0826f-137">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="0826f-137">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="0826f-138">**GetText LB \_**</span><span class="sxs-lookup"><span data-stu-id="0826f-138">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="0826f-139">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="0826f-139">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0826f-140">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="0826f-140">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="0826f-141">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="0826f-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

