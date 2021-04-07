---
title: Messaggio EM_LINESCROLL (winuser. h)
description: Scorre il testo in un controllo di modifica su più righe.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- Controlli di Windows Message EM_LINESCROLL
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646e225ef269ccddca2cdc29caf635d94c1671e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048559"
---
# <a name="em_linescroll-message"></a><span data-ttu-id="f0240-104">\_Messaggio LINESCROLL em</span><span class="sxs-lookup"><span data-stu-id="f0240-104">EM\_LINESCROLL message</span></span>

<span data-ttu-id="f0240-105">Scorre il testo in un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="f0240-105">Scrolls the text in a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0240-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0240-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0240-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0240-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0240-108">**Controlli di modifica:** Numero di caratteri da scorrere orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="f0240-108">**Edit controls:** The number of characters to scroll horizontally.</span></span>

<span data-ttu-id="f0240-109">**Controlli Rich Edit:** Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f0240-109">**Rich edit controls:** This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f0240-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0240-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0240-111">Numero di righe da scorrere verticalmente.</span><span class="sxs-lookup"><span data-stu-id="f0240-111">The number of lines to scroll vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0240-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0240-112">Return value</span></span>

<span data-ttu-id="f0240-113">Se il messaggio viene inviato a un controllo di modifica su più righe, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="f0240-113">If the message is sent to a multiline edit control, the return value is **TRUE**.</span></span>

<span data-ttu-id="f0240-114">Se il messaggio viene inviato a un controllo di modifica a riga singola, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="f0240-114">If the message is sent to a single-line edit control, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0240-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0240-115">Remarks</span></span>

<span data-ttu-id="f0240-116">Il controllo non scorre verticalmente oltre l'ultima riga di testo nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="f0240-116">The control does not scroll vertically past the last line of text in the edit control.</span></span> <span data-ttu-id="f0240-117">Se la riga corrente più il numero di righe specificato dal parametro *lParam* supera il numero totale di righe nel controllo di modifica, il valore viene regolato in modo che l'ultima riga del controllo di modifica venga spostata all'inizio della finestra di modifica del controllo.</span><span class="sxs-lookup"><span data-stu-id="f0240-117">If the current line plus the number of lines specified by the *lParam* parameter exceeds the total number of lines in the edit control, the value is adjusted so that the last line of the edit control is scrolled to the top of the edit-control window.</span></span>

<span data-ttu-id="f0240-118">**Controlli di modifica:** Il **messaggio \_ LINESCROLL em** scorre il testo verticalmente o orizzontalmente in un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="f0240-118">**Edit controls:** The **EM\_LINESCROLL** message scrolls the text vertically or horizontally in a multiline edit control.</span></span> <span data-ttu-id="f0240-119">Il **messaggio \_ LINESCROLL em** può essere usato per scorrere orizzontalmente oltre l'ultimo carattere di una riga.</span><span class="sxs-lookup"><span data-stu-id="f0240-119">The **EM\_LINESCROLL** message can be used to scroll horizontally past the last character of any line.</span></span>

<span data-ttu-id="f0240-120">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f0240-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="f0240-121">Il **messaggio \_ LINESCROLL em** scorre verticalmente il testo in un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="f0240-121">The **EM\_LINESCROLL** message scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="f0240-122">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="f0240-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0240-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0240-123">Requirements</span></span>



| <span data-ttu-id="f0240-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0240-124">Requirement</span></span> | <span data-ttu-id="f0240-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f0240-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0240-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0240-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f0240-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0240-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f0240-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0240-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f0240-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f0240-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f0240-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0240-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0240-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0240-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





