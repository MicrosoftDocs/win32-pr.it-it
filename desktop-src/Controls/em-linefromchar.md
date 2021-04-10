---
title: Messaggio EM_LINEFROMCHAR (winuser. h)
description: Ottiene l'indice della riga che contiene l'indice del carattere specificato in un controllo di modifica su più righe.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Controlli di Windows Message EM_LINEFROMCHAR
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0dfe0c6c2ed0f9d77817fddde75fa18b64d485f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119479"
---
# <a name="em_linefromchar-message"></a><span data-ttu-id="c274c-104">\_Messaggio LINEFROMCHAR em</span><span class="sxs-lookup"><span data-stu-id="c274c-104">EM\_LINEFROMCHAR message</span></span>

<span data-ttu-id="c274c-105">Ottiene l'indice della riga che contiene l'indice del carattere specificato in un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="c274c-105">Gets the index of the line that contains the specified character index in a multiline edit control.</span></span> <span data-ttu-id="c274c-106">Un indice dei caratteri è l'indice in base zero del carattere a partire dall'inizio del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="c274c-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span> <span data-ttu-id="c274c-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c274c-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c274c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c274c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c274c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c274c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c274c-110">Indice dei caratteri del carattere contenuto nella riga di cui è necessario recuperare il numero.</span><span class="sxs-lookup"><span data-stu-id="c274c-110">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="c274c-111">Se questo parametro è-1, **em \_ LINEFROMCHAR** Recupera il numero di riga della riga corrente (la riga contenente il punto di inserimento) o, se è presente una selezione, il numero di riga della riga contenente l'inizio della selezione.</span><span class="sxs-lookup"><span data-stu-id="c274c-111">If this parameter is -1, **EM\_LINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="c274c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c274c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c274c-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="c274c-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c274c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c274c-114">Return value</span></span>

<span data-ttu-id="c274c-115">Il valore restituito è il numero di riga in base zero della riga che contiene l'indice dei caratteri specificato da *wParam*.</span><span class="sxs-lookup"><span data-stu-id="c274c-115">The return value is the zero-based line number of the line containing the character index specified by *wParam*.</span></span>

## <a name="remarks"></a><span data-ttu-id="c274c-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c274c-116">Remarks</span></span>

<span data-ttu-id="c274c-117">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c274c-117">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="c274c-118">Se l'indice dei caratteri è maggiore di 64.000, utilizzare il messaggio [**\_ EXLINEFROMCHAR em**](em-exlinefromchar.md) .</span><span class="sxs-lookup"><span data-stu-id="c274c-118">If the character index is greater than 64,000, use the [**EM\_EXLINEFROMCHAR**](em-exlinefromchar.md) message.</span></span> <span data-ttu-id="c274c-119">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c274c-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c274c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c274c-120">Requirements</span></span>



| <span data-ttu-id="c274c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c274c-121">Requirement</span></span> | <span data-ttu-id="c274c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c274c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c274c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c274c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c274c-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c274c-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c274c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c274c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c274c-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c274c-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c274c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c274c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c274c-128"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c274c-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c274c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c274c-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="c274c-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c274c-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c274c-131">**\_EXLINEFROMCHAR em**</span><span class="sxs-lookup"><span data-stu-id="c274c-131">**EM\_EXLINEFROMCHAR**</span></span>](em-exlinefromchar.md)
</dt> <dt>

[<span data-ttu-id="c274c-132">**\_LINEINDEX em**</span><span class="sxs-lookup"><span data-stu-id="c274c-132">**EM\_LINEINDEX**</span></span>](em-lineindex.md)
</dt> </dl>

 

 





