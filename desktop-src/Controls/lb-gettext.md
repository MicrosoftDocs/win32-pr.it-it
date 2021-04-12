---
title: Messaggio LB_GETTEXT (winuser. h)
description: Ottiene una stringa da una casella di riepilogo.
ms.assetid: 6bf7ec3b-237b-4668-9493-40c098a32428
keywords:
- Controlli di Windows Message LB_GETTEXT
topic_type:
- apiref
api_name:
- LB_GETTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dd5e2c7a9e6c1c1aa1b847592555a013766134
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478257"
---
# <a name="lb_gettext-message"></a><span data-ttu-id="08156-104">\_Messaggio lb GETtext</span><span class="sxs-lookup"><span data-stu-id="08156-104">LB\_GETTEXT message</span></span>

<span data-ttu-id="08156-105">Ottiene una stringa da una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="08156-105">Gets a string from a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="08156-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="08156-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08156-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08156-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08156-108">Indice in base zero della stringa da recuperare.</span><span class="sxs-lookup"><span data-stu-id="08156-108">The zero-based index of the string to retrieve.</span></span>

<span data-ttu-id="08156-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): il parametro *wParam* è limitato ai valori a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="08156-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="08156-110">Ciò significa che le caselle di riepilogo non possono contenere più di 32.767 elementi.</span><span class="sxs-lookup"><span data-stu-id="08156-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="08156-111">Sebbene il numero di elementi sia limitato, le dimensioni totali in byte degli elementi in una casella di riepilogo sono limitate solo dalla memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="08156-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="08156-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08156-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08156-113">Puntatore al buffer che riceverà la stringa. è di tipo **LPTSTR** che viene successivamente eseguito il cast a un **lParam**.</span><span class="sxs-lookup"><span data-stu-id="08156-113">A pointer to the buffer that will receive the string; it is type **LPTSTR** which is subsequently cast to an **LPARAM**.</span></span> <span data-ttu-id="08156-114">Il buffer deve contenere spazio sufficiente per la stringa e un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="08156-114">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="08156-115">Un messaggio [**lb \_ GETTEXTLEN**](lb-gettextlen.md) può essere inviato prima del messaggio **lb \_ gettext** per recuperare la lunghezza, in **TCHAR** s, della stringa.</span><span class="sxs-lookup"><span data-stu-id="08156-115">An [**LB\_GETTEXTLEN**](lb-gettextlen.md) message can be sent before the **LB\_GETTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08156-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08156-116">Return value</span></span>

<span data-ttu-id="08156-117">Il valore restituito è la lunghezza della stringa, in **TCHAR** s, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="08156-117">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="08156-118">Se *wParam* non specifica un indice valido, il valore restituito è lb \_ Err.</span><span class="sxs-lookup"><span data-stu-id="08156-118">If *wParam* does not specify a valid index, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="08156-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="08156-119">Remarks</span></span>

<span data-ttu-id="08156-120">Se la casella di riepilogo ha uno stile disegnato dal proprietario ma non lo stile [**\_ HASSTRINGS lbs**](list-box-styles.md) , il buffer a cui punta il parametro *lParam* riceve il valore associato all'elemento (i dati dell'elemento).</span><span class="sxs-lookup"><span data-stu-id="08156-120">If the list box has an owner-drawn style but not the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the buffer pointed to by the *lParam* parameter receives the value associated with the item (the item data).</span></span>

## <a name="requirements"></a><span data-ttu-id="08156-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08156-121">Requirements</span></span>



| <span data-ttu-id="08156-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="08156-122">Requirement</span></span> | <span data-ttu-id="08156-123">Valore</span><span class="sxs-lookup"><span data-stu-id="08156-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08156-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08156-124">Minimum supported client</span></span><br/> | <span data-ttu-id="08156-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08156-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="08156-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08156-126">Minimum supported server</span></span><br/> | <span data-ttu-id="08156-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08156-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08156-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08156-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="08156-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08156-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08156-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08156-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08156-131">**\_GETTEXTLEN lb**</span><span class="sxs-lookup"><span data-stu-id="08156-131">**LB\_GETTEXTLEN**</span></span>](lb-gettextlen.md)
</dt> </dl>

 

 





