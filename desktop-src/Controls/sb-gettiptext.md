---
title: Messaggio SB_GETTIPTEXT (COMmctrl. h)
description: Recupera il testo della descrizione comando per una parte in una barra di stato. La barra di stato deve essere creata con lo \_ stile della descrizione comando SBT per abilitare le descrizioni comandi.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- Controlli di Windows Message SB_GETTIPTEXT
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d492bc19f82300f460666b3213c545fe95b8db85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874229"
---
# <a name="sb_gettiptext-message"></a><span data-ttu-id="d00a1-105">\_Messaggio GETTIPTEXT SB</span><span class="sxs-lookup"><span data-stu-id="d00a1-105">SB\_GETTIPTEXT message</span></span>

<span data-ttu-id="d00a1-106">Recupera il testo della descrizione comando per una parte in una barra di stato.</span><span class="sxs-lookup"><span data-stu-id="d00a1-106">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="d00a1-107">La barra di stato deve essere creata con lo stile della [**\_ Descrizione comando SBT**](status-bar-styles.md) per abilitare le descrizioni comandi.</span><span class="sxs-lookup"><span data-stu-id="d00a1-107">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="d00a1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d00a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d00a1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d00a1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d00a1-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica l'indice in base zero della parte che riceve il testo della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="d00a1-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the part that receives the tooltip text.</span></span> <span data-ttu-id="d00a1-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica la dimensione del buffer in corrispondenza di *lParam*, in caratteri.</span><span class="sxs-lookup"><span data-stu-id="d00a1-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the size of the buffer at *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="d00a1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d00a1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d00a1-113">Puntatore a un buffer di caratteri che riceve il testo della descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="d00a1-113">Pointer to a character buffer that receives the tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d00a1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d00a1-114">Return value</span></span>

<span data-ttu-id="d00a1-115">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d00a1-115">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d00a1-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d00a1-116">Remarks</span></span>

<span data-ttu-id="d00a1-117">**Avviso di sicurezza:** L'uso errato di questo messaggio può causare problemi per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d00a1-117">**Security Warning:** Using this message incorrectly can cause problems for your application.</span></span> <span data-ttu-id="d00a1-118">Se, ad esempio, il testo è troppo grande per il buffer *lParam* , potrebbe verificarsi un overflow del buffer.</span><span class="sxs-lookup"><span data-stu-id="d00a1-118">For example, if the text is too large for the *lParam* buffer, it could cause a buffer overflow.</span></span> <span data-ttu-id="d00a1-119">Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="d00a1-119">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="d00a1-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d00a1-120">Requirements</span></span>



| <span data-ttu-id="d00a1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d00a1-121">Requirement</span></span> | <span data-ttu-id="d00a1-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d00a1-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d00a1-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d00a1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d00a1-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d00a1-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d00a1-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d00a1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d00a1-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d00a1-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d00a1-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d00a1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d00a1-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d00a1-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d00a1-129">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d00a1-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d00a1-130">**SB \_ GETTIPTEXTW** (Unicode) e **SB \_ GETTIPTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d00a1-130">**SB\_GETTIPTEXTW** (Unicode) and **SB\_GETTIPTEXTA** (ANSI)</span></span><br/>               |



 

