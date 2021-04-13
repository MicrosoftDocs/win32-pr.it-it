---
title: Messaggio EM_GETFIRSTVISIBLELINE (winuser. h)
description: Ottiene l'indice in base zero della riga visibile in alto in un controllo di modifica su più righe. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- Controlli di Windows Message EM_GETFIRSTVISIBLELINE
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518303"
---
# <a name="em_getfirstvisibleline-message"></a><span data-ttu-id="bf03b-105">\_Messaggio GETFIRSTVISIBLELINE em</span><span class="sxs-lookup"><span data-stu-id="bf03b-105">EM\_GETFIRSTVISIBLELINE message</span></span>

<span data-ttu-id="bf03b-106">Ottiene l'indice in base zero della riga visibile in alto in un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="bf03b-106">Gets the zero-based index of the uppermost visible line in a multiline edit control.</span></span> <span data-ttu-id="bf03b-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="bf03b-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bf03b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf03b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf03b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bf03b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf03b-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bf03b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="bf03b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf03b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf03b-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bf03b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf03b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf03b-113">Return value</span></span>

<span data-ttu-id="bf03b-114">Il valore restituito è l'indice in base zero della riga visibile in alto in un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="bf03b-114">The return value is the zero-based index of the uppermost visible line in a multiline edit control.</span></span>

<span data-ttu-id="bf03b-115">**Controlli di modifica:** Per i controlli di modifica a riga singola, il valore restituito è l'indice in base zero del primo carattere visibile.</span><span class="sxs-lookup"><span data-stu-id="bf03b-115">**Edit controls:** For single-line edit controls, the return value is the zero-based index of the first visible character.</span></span>

<span data-ttu-id="bf03b-116">**Controlli Rich Edit:** Per i controlli Rich Edit a riga singola, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="bf03b-116">**Rich edit controls:** For single-line rich edit controls, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf03b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf03b-117">Remarks</span></span>

<span data-ttu-id="bf03b-118">Il numero di righe e la lunghezza delle righe in un controllo di modifica dipendono dalla larghezza del controllo e dall'impostazione corrente di WordWrap.</span><span class="sxs-lookup"><span data-stu-id="bf03b-118">The number of lines and the length of the lines in an edit control depend on the width of the control and the current Wordwrap setting.</span></span>

<span data-ttu-id="bf03b-119">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="bf03b-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="bf03b-120">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="bf03b-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf03b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf03b-121">Requirements</span></span>



| <span data-ttu-id="bf03b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf03b-122">Requirement</span></span> | <span data-ttu-id="bf03b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="bf03b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf03b-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf03b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bf03b-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf03b-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bf03b-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf03b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bf03b-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bf03b-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bf03b-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf03b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf03b-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf03b-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





