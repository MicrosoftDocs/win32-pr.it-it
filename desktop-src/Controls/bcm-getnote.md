---
title: Messaggio BCM_GETNOTE (COMmctrl. h)
description: Ottiene il testo della nota associata a un pulsante di collegamento al comando. È possibile inviare questo messaggio in modo esplicito o usare la macro del pulsante \_ getnote.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- Controlli di Windows Message BCM_GETNOTE
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 758dac90ba4c0f3087a6df90d9acf2c1321b1d73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301707"
---
# <a name="bcm_getnote-message"></a><span data-ttu-id="61714-105">\_Messaggio GETNOTE BCM</span><span class="sxs-lookup"><span data-stu-id="61714-105">BCM\_GETNOTE message</span></span>

<span data-ttu-id="61714-106">Ottiene il testo della nota associata a un pulsante di collegamento al comando.</span><span class="sxs-lookup"><span data-stu-id="61714-106">Gets the text of the note associated with a command link button.</span></span> <span data-ttu-id="61714-107">È possibile inviare questo messaggio in modo esplicito o usare la macro del [**pulsante \_ getnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) .</span><span class="sxs-lookup"><span data-stu-id="61714-107">You can send this message explicitly or use the [**Button\_GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="61714-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="61714-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61714-109">*wParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="61714-109">*wParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="61714-110">**Valore DWORD** che specifica la dimensione del buffer a cui punta *lParam*, in caratteri.</span><span class="sxs-lookup"><span data-stu-id="61714-110">A **DWORD** that specifies the size of the buffer pointed to by *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="61714-111">*lParam* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="61714-111">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61714-112">Buffer di stringa per ricevere il testo.</span><span class="sxs-lookup"><span data-stu-id="61714-112">The string buffer to receive the text.</span></span> <span data-ttu-id="61714-113">Il buffer deve essere sufficientemente grande da contenere il carattere NULL di terminazione.</span><span class="sxs-lookup"><span data-stu-id="61714-113">The buffer must be large enough to accommodate the terminating NULL character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61714-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61714-114">Return value</span></span>

<span data-ttu-id="61714-115">Se il messaggio ha esito positivo, restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="61714-115">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="61714-116">In caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="61714-116">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="61714-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="61714-117">Remarks</span></span>

<span data-ttu-id="61714-118">Il messaggio **BCM \_ getnote** funziona solo con i pulsanti con lo stile del pulsante [**BS \_ COMMANDLINK**](button-styles.md) o [**BS \_ DEFCOMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="61714-118">The **BCM\_GETNOTE** message works only with buttons that have the [**BS\_COMMANDLINK**](button-styles.md) or [**BS\_DEFCOMMANDLINK**](button-styles.md) button style.</span></span>

<span data-ttu-id="61714-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) conterrà:</span><span class="sxs-lookup"><span data-stu-id="61714-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will contain:</span></span>

-   <span data-ttu-id="61714-120">ERRORE \_ non \_ supportato, se il pulsante non ha lo stile [**BS \_ DEFCOMMANDLINK**](button-styles.md) o [**BS \_ COMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="61714-120">ERROR\_NOT\_SUPPORTED, if the button does not have the [**BS\_DEFCOMMANDLINK**](button-styles.md) or [**BS\_COMMANDLINK**](button-styles.md) style.</span></span>
-   <span data-ttu-id="61714-121">ERRORE \_ nel \_ buffer insufficiente, se il buffer *lParam* è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="61714-121">ERROR\_INSUFFICIENT\_BUFFER, if the *lParam* buffer is too small.</span></span> <span data-ttu-id="61714-122">Il parametro *wParam* conterrà le dimensioni del buffer richieste in caratteri.</span><span class="sxs-lookup"><span data-stu-id="61714-122">The *wParam* parameter will contain the required buffer size, in characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="61714-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61714-123">Requirements</span></span>



| <span data-ttu-id="61714-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="61714-124">Requirement</span></span> | <span data-ttu-id="61714-125">Valore</span><span class="sxs-lookup"><span data-stu-id="61714-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61714-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61714-126">Minimum supported client</span></span><br/> | <span data-ttu-id="61714-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61714-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61714-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61714-128">Minimum supported server</span></span><br/> | <span data-ttu-id="61714-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61714-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61714-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61714-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="61714-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61714-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61714-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61714-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="61714-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="61714-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="61714-134">Stili dei pulsanti</span><span class="sxs-lookup"><span data-stu-id="61714-134">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="61714-135">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="61714-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="61714-136">Tipi di pulsante</span><span class="sxs-lookup"><span data-stu-id="61714-136">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

