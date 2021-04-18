---
title: Messaggio TTM_ENUMTOOLS (COMmctrl. h)
description: Recupera le informazioni che un controllo ToolTip gestisce sullo strumento corrente \ 8212, ovvero lo strumento per il quale la descrizione comando sta visualizzando il testo.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- Controlli di Windows Message TTM_ENUMTOOLS
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
ms.openlocfilehash: ad1679f9740539507a57c4cba93319569add0af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476792"
---
# <a name="ttm_enumtools-message"></a><span data-ttu-id="cfb27-104">\_Messaggio TTM ENUMTOOLS</span><span class="sxs-lookup"><span data-stu-id="cfb27-104">TTM\_ENUMTOOLS message</span></span>

<span data-ttu-id="cfb27-105">Recupera le informazioni che un controllo ToolTip gestisce sullo strumento corrente, ovvero lo strumento per il quale la descrizione comando sta attualmente visualizzando il testo.</span><span class="sxs-lookup"><span data-stu-id="cfb27-105">Retrieves the information that a tooltip control maintains about the current tool that is, the tool for which the tooltip is currently displaying text.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfb27-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfb27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfb27-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfb27-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb27-108">Indice in base zero dello strumento per il quale recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="cfb27-108">Zero-based index of the tool for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="cfb27-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfb27-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfb27-110">Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) che riceve informazioni sullo strumento.</span><span class="sxs-lookup"><span data-stu-id="cfb27-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the tool.</span></span> <span data-ttu-id="cfb27-111">Impostare il membro **cbSize** della struttura su sizeof (TOOLINFO) prima di inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="cfb27-111">Set the **cbSize** member of this structure to sizeof(TOOLINFO) before sending this message.</span></span> <span data-ttu-id="cfb27-112">Allocare un buffer.</span><span class="sxs-lookup"><span data-stu-id="cfb27-112">Allocate a buffer.</span></span> <span data-ttu-id="cfb27-113">Impostare il membro **lpszText** in modo che punti al buffer per ricevere il testo dello strumento.</span><span class="sxs-lookup"><span data-stu-id="cfb27-113">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span> <span data-ttu-id="cfb27-114">Non è possibile determinare le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="cfb27-114">There is no way to determine the required buffer size.</span></span> <span data-ttu-id="cfb27-115">Tuttavia, il testo dello strumento, come restituito al membro **lpszText** della struttura **TOOLINFO** , ha una lunghezza massima di 80 **TCHARs**, incluso il **null** di terminazione.</span><span class="sxs-lookup"><span data-stu-id="cfb27-115">However, tool text, as returned at the **lpszText** member of the **TOOLINFO** structure, has a maximum length of 80 **TCHARs**, including the terminating **NULL**.</span></span> <span data-ttu-id="cfb27-116">Se il testo supera questa lunghezza, viene troncato.</span><span class="sxs-lookup"><span data-stu-id="cfb27-116">If the text exceeds this length, it is truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfb27-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfb27-117">Return value</span></span>

<span data-ttu-id="cfb27-118">Restituisce **true** se vengono enumerati gli strumenti o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cfb27-118">Returns **TRUE** if any tools are enumerated, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfb27-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfb27-119">Remarks</span></span>

<span data-ttu-id="cfb27-120">**Avviso di sicurezza:** L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="cfb27-120">**Security Warning:** Using this message might compromise the security of your program.</span></span> <span data-ttu-id="cfb27-121">Questo messaggio non consente al destinatario del messaggio di conoscerne le dimensioni o di specificare le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="cfb27-121">This message does not provide a way for the message receiver to know the size of the buffer or to specify the size of the buffer.</span></span> <span data-ttu-id="cfb27-122">Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="cfb27-122">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb27-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfb27-123">Requirements</span></span>



| <span data-ttu-id="cfb27-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfb27-124">Requirement</span></span> | <span data-ttu-id="cfb27-125">Valore</span><span class="sxs-lookup"><span data-stu-id="cfb27-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb27-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfb27-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cfb27-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cfb27-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfb27-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfb27-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cfb27-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cfb27-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfb27-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfb27-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfb27-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfb27-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cfb27-132">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="cfb27-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cfb27-133">**TTM \_ ENUMTOOLSW** (Unicode) e **TTM \_ ENUMTOOLSA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cfb27-133">**TTM\_ENUMTOOLSW** (Unicode) and **TTM\_ENUMTOOLSA** (ANSI)</span></span><br/>               |



 

 





