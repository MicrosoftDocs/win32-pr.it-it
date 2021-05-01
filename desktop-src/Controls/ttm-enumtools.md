---
title: TTM_ENUMTOOLS messaggio (Commctrl.h)
description: Recupera le informazioni mantenute da un controllo descrizione comando sullo strumento corrente \ 8212, ovvero lo strumento per cui la descrizione comando visualizza attualmente il testo.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- TTM_ENUMTOOLS di windows del messaggio
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67f23a145838aa3562c81e78fb82c3ea66320df
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327136"
---
# <a name="ttm_enumtools-message"></a><span data-ttu-id="b5165-104">Messaggio TTM \_ ENUMTOOLS</span><span class="sxs-lookup"><span data-stu-id="b5165-104">TTM\_ENUMTOOLS message</span></span>

<span data-ttu-id="b5165-105">Recupera le informazioni che un controllo descrizione comando gestisce sullo strumento corrente, ovvero lo strumento per cui la descrizione comando visualizza attualmente testo.</span><span class="sxs-lookup"><span data-stu-id="b5165-105">Retrieves the information that a tooltip control maintains about the current tool that is, the tool for which the tooltip is currently displaying text.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5165-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5165-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5165-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5165-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5165-108">Indice in base zero dello strumento per il quale recuperare informazioni.</span><span class="sxs-lookup"><span data-stu-id="b5165-108">Zero-based index of the tool for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="b5165-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5165-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5165-110">Puntatore a [**una struttura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) che riceve informazioni sullo strumento.</span><span class="sxs-lookup"><span data-stu-id="b5165-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the tool.</span></span> <span data-ttu-id="b5165-111">Impostare il **membro cbSize** di questa struttura su sizeof(TOOLINFO) prima di inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="b5165-111">Set the **cbSize** member of this structure to sizeof(TOOLINFO) before sending this message.</span></span> <span data-ttu-id="b5165-112">Allocare un buffer.</span><span class="sxs-lookup"><span data-stu-id="b5165-112">Allocate a buffer.</span></span> <span data-ttu-id="b5165-113">Impostare il **membro lpszText** in modo che punti al buffer per ricevere il testo dello strumento.</span><span class="sxs-lookup"><span data-stu-id="b5165-113">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span> <span data-ttu-id="b5165-114">Non è possibile determinare le dimensioni del buffer necessarie.</span><span class="sxs-lookup"><span data-stu-id="b5165-114">There is no way to determine the required buffer size.</span></span> <span data-ttu-id="b5165-115">Tuttavia, il testo dello strumento, come restituito nel membro **lpszText** della struttura **TOOLINFO,** ha una lunghezza massima di 80 **TCHAR,** inclusa la **terminazione NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5165-115">However, tool text, as returned at the **lpszText** member of the **TOOLINFO** structure, has a maximum length of 80 **TCHARs**, including the terminating **NULL**.</span></span> <span data-ttu-id="b5165-116">Se il testo supera questa lunghezza, viene troncato.</span><span class="sxs-lookup"><span data-stu-id="b5165-116">If the text exceeds this length, it is truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5165-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5165-117">Return value</span></span>

<span data-ttu-id="b5165-118">Restituisce **FALSE se** uno strumento è stato enumerato o meno.</span><span class="sxs-lookup"><span data-stu-id="b5165-118">Returns **FALSE** whether or not a tool was enumerated.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5165-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5165-119">Remarks</span></span>

<span data-ttu-id="b5165-120">**Avviso di sicurezza:** L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="b5165-120">**Security Warning:** Using this message might compromise the security of your program.</span></span> <span data-ttu-id="b5165-121">Questo messaggio non consente al destinatario del messaggio di conoscere le dimensioni del buffer o di specificare le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="b5165-121">This message does not provide a way for the message receiver to know the size of the buffer or to specify the size of the buffer.</span></span> <span data-ttu-id="b5165-122">Prima di continuare, [è consigliabile esaminare Considerazioni sulla sicurezza: Controlli di Microsoft Windows.](sec-comctls.md)</span><span class="sxs-lookup"><span data-stu-id="b5165-122">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5165-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5165-123">Requirements</span></span>



| <span data-ttu-id="b5165-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5165-124">Requirement</span></span> | <span data-ttu-id="b5165-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b5165-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5165-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5165-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b5165-127">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b5165-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5165-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5165-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b5165-129">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5165-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5165-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5165-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5165-131"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="b5165-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="b5165-132">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b5165-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b5165-133">**TTM \_ ENUMTOOLSW** (Unicode) e **TTM \_ ENUMTOOLSA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b5165-133">**TTM\_ENUMTOOLSW** (Unicode) and **TTM\_ENUMTOOLSA** (ANSI)</span></span><br/>               |



 

 





