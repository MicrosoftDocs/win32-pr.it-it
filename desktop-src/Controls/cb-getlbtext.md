---
title: Messaggio CB_GETLBTEXT (winuser. h)
description: Ottiene una stringa dall'elenco di una casella combinata.
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- Controlli di Windows Message CB_GETLBTEXT
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048357"
---
# <a name="cb_getlbtext-message"></a><span data-ttu-id="93c88-104">\_Messaggio GETLBTEXT CB</span><span class="sxs-lookup"><span data-stu-id="93c88-104">CB\_GETLBTEXT message</span></span>

<span data-ttu-id="93c88-105">Ottiene una stringa dall'elenco di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="93c88-105">Gets a string from the list of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="93c88-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="93c88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c88-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93c88-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93c88-108">Indice in base zero della stringa da recuperare.</span><span class="sxs-lookup"><span data-stu-id="93c88-108">The zero-based index of the string to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="93c88-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93c88-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93c88-110">Puntatore al buffer che riceve la stringa.</span><span class="sxs-lookup"><span data-stu-id="93c88-110">A pointer to the buffer that receives the string.</span></span> <span data-ttu-id="93c88-111">Il buffer deve contenere spazio sufficiente per la stringa e un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="93c88-111">The buffer must have sufficient space for the string and a terminating null character.</span></span> <span data-ttu-id="93c88-112">È possibile inviare un messaggio [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) prima del messaggio **CB \_ GETLBTEXT** per recuperare la lunghezza, in **TCHAR** s, della stringa.</span><span class="sxs-lookup"><span data-stu-id="93c88-112">You can send a [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) message prior to the **CB\_GETLBTEXT** message to retrieve the length, in **TCHAR** s, of the string.</span></span> <span data-ttu-id="93c88-113">Se è una stringa ANSI, questo è il numero di byte, ma se è una stringa Unicode questo è il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="93c88-113">If it is an ANSI string this is the number of bytes, but if it is a Unicode string this is the number of characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c88-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93c88-114">Return value</span></span>

<span data-ttu-id="93c88-115">Il valore restituito è la lunghezza della stringa, in **TCHAR** s, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="93c88-115">The return value is the length of the string, in **TCHAR** s, excluding the terminating null character.</span></span> <span data-ttu-id="93c88-116">Se *wParam* non specifica un indice valido, il valore restituito è CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="93c88-116">If *wParam* does not specify a valid index, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="93c88-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="93c88-117">Remarks</span></span>

<span data-ttu-id="93c88-118">**Avviso di sicurezza:** L'uso errato di questo messaggio può compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="93c88-118">**Security Warning:** Using this message incorrectly can compromise the security of your program.</span></span> <span data-ttu-id="93c88-119">Questo messaggio non fornisce un modo per stabilire le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="93c88-119">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="93c88-120">Se si utilizza questo messaggio, chiamare prima [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) per ottenere il numero di caratteri necessari e quindi chiamare il messaggio per recuperare la stringa.</span><span class="sxs-lookup"><span data-stu-id="93c88-120">If you use this message, first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to get the number of characters that are required and then call the message to retrieve the string.</span></span> <span data-ttu-id="93c88-121">Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="93c88-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="93c88-122">Se si crea la casella combinata con uno stile disegnato dal proprietario ma senza lo stile [**CBS \_ HASSTRINGS**](combo-box-styles.md) , il buffer a cui punta *lParam* riceve i dati associati all'elemento.</span><span class="sxs-lookup"><span data-stu-id="93c88-122">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the buffer pointed to by *lParam* receives the data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c88-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93c88-123">Requirements</span></span>



| <span data-ttu-id="93c88-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="93c88-124">Requirement</span></span> | <span data-ttu-id="93c88-125">Valore</span><span class="sxs-lookup"><span data-stu-id="93c88-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93c88-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93c88-126">Minimum supported client</span></span><br/> | <span data-ttu-id="93c88-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93c88-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="93c88-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93c88-128">Minimum supported server</span></span><br/> | <span data-ttu-id="93c88-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="93c88-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="93c88-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93c88-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="93c88-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93c88-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93c88-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93c88-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c88-133">**CB \_ GETLBTEXTLEN**</span><span class="sxs-lookup"><span data-stu-id="93c88-133">**CB\_GETLBTEXTLEN**</span></span>](cb-getlbtextlen.md)
</dt> </dl>

 

 





