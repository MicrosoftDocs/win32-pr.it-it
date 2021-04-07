---
title: Messaggio CB_GETLBTEXTLEN (winuser. h)
description: Ottiene la lunghezza, in caratteri, di una stringa nell'elenco di una casella combinata.
ms.assetid: f0fe0eef-f9db-4d9f-9a42-5bb2aeae30a0
keywords:
- Controlli di Windows Message CB_GETLBTEXTLEN
topic_type:
- apiref
api_name:
- CB_GETLBTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e42dc19b13b22f577fcc21bb32cb8810bab29be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964205"
---
# <a name="cb_getlbtextlen-message"></a><span data-ttu-id="50f72-104">\_Messaggio GETLBTEXTLEN CB</span><span class="sxs-lookup"><span data-stu-id="50f72-104">CB\_GETLBTEXTLEN message</span></span>

<span data-ttu-id="50f72-105">Ottiene la lunghezza, in caratteri, di una stringa nell'elenco di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="50f72-105">Gets the length, in characters, of a string in the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="50f72-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="50f72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50f72-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50f72-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50f72-108">Indice in base zero della stringa.</span><span class="sxs-lookup"><span data-stu-id="50f72-108">The zero-based index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="50f72-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50f72-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50f72-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="50f72-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50f72-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50f72-111">Return value</span></span>

<span data-ttu-id="50f72-112">Il valore restituito è la lunghezza della stringa, in **TCHAR** s, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="50f72-112">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="50f72-113">Se una stringa ANSI è il numero di byte e se si tratta di una stringa Unicode, si tratta del numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="50f72-113">If an ANSI string this is the number of bytes, and if it is a Unicode string this is the number of characters.</span></span> <span data-ttu-id="50f72-114">In determinate condizioni, questo valore può essere effettivamente maggiore della lunghezza del testo.</span><span class="sxs-lookup"><span data-stu-id="50f72-114">Under certain conditions, this value may actually be greater than the length of the text.</span></span> <span data-ttu-id="50f72-115">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="50f72-115">For more information, see the Remarks section.</span></span>

<span data-ttu-id="50f72-116">Se il parametro *wParam* non specifica un indice valido, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="50f72-116">If the *wParam* parameter does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="50f72-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="50f72-117">Remarks</span></span>

<span data-ttu-id="50f72-118">In determinate condizioni, il valore restituito è maggiore della lunghezza effettiva del testo.</span><span class="sxs-lookup"><span data-stu-id="50f72-118">Under certain conditions, the return value is larger than the actual length of the text.</span></span> <span data-ttu-id="50f72-119">Questa situazione si verifica con determinate combinazioni di ANSI e Unicode ed è dovuta al sistema operativo che consente la possibile esistenza di caratteri DBCS (Double-byte character set) all'interno del testo.</span><span class="sxs-lookup"><span data-stu-id="50f72-119">This occurs with certain mixtures of ANSI and Unicode, and is due to the operating system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="50f72-120">Il valore restituito, tuttavia, sarà sempre almeno uguale alla lunghezza effettiva del testo; quindi, è sempre possibile usarlo per guidare l'allocazione del buffer.</span><span class="sxs-lookup"><span data-stu-id="50f72-120">The return value, however, will always be at least as large as the actual length of the text; so you can always use it to guide buffer allocation.</span></span> <span data-ttu-id="50f72-121">Questo comportamento può verificarsi quando un'applicazione utilizza funzioni ANSI e finestre di dialogo comuni che utilizzano Unicode.</span><span class="sxs-lookup"><span data-stu-id="50f72-121">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="50f72-122">Per ottenere la lunghezza esatta del testo, usare i messaggi [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)o [**CB \_ GETLBTEXT**](cb-getlbtext.md) oppure la funzione [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="50f72-122">To obtain the exact length of the text, use the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext), [**LB\_GETTEXT**](lb-gettext.md), or [**CB\_GETLBTEXT**](cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="50f72-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50f72-123">Requirements</span></span>



| <span data-ttu-id="50f72-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="50f72-124">Requirement</span></span> | <span data-ttu-id="50f72-125">Valore</span><span class="sxs-lookup"><span data-stu-id="50f72-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50f72-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50f72-126">Minimum supported client</span></span><br/> | <span data-ttu-id="50f72-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50f72-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="50f72-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50f72-128">Minimum supported server</span></span><br/> | <span data-ttu-id="50f72-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50f72-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="50f72-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50f72-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="50f72-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50f72-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50f72-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50f72-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="50f72-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="50f72-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="50f72-134">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="50f72-134">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="50f72-135">**GetText LB \_**</span><span class="sxs-lookup"><span data-stu-id="50f72-135">**LB\_GETTEXT**</span></span>](lb-gettext.md)
</dt> <dt>

<span data-ttu-id="50f72-136">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="50f72-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="50f72-137">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="50f72-137">**GetWindowText**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="50f72-138">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="50f72-138">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

