---
title: Messaggio TVM_GETISEARCHSTRING (COMmctrl. h)
description: Recupera la stringa di ricerca incrementale per un controllo di visualizzazione albero.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- Controlli di Windows Message TVM_GETISEARCHSTRING
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa968d78a1a99dd3b1eb90055cf2c1d2de51db86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121290"
---
# <a name="tvm_getisearchstring-message"></a><span data-ttu-id="5cd44-104">\_Messaggio GETISEARCHSTRING TVM</span><span class="sxs-lookup"><span data-stu-id="5cd44-104">TVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="5cd44-105">Recupera la stringa di ricerca incrementale per un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="5cd44-105">Retrieves the incremental search string for a tree-view control.</span></span> <span data-ttu-id="5cd44-106">Il controllo di visualizzazione albero utilizza la stringa di ricerca incrementale per selezionare un elemento in base ai caratteri digitati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="5cd44-106">The tree-view control uses the incremental search string to select an item based on characters typed by the user.</span></span> <span data-ttu-id="5cd44-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetISearchString di TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) .</span><span class="sxs-lookup"><span data-stu-id="5cd44-107">You can send this message explicitly or by using the [**TreeView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5cd44-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cd44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cd44-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5cd44-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5cd44-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5cd44-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5cd44-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5cd44-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5cd44-112">Puntatore al buffer che riceve la stringa di ricerca incrementale.</span><span class="sxs-lookup"><span data-stu-id="5cd44-112">Pointer to the buffer that receives the incremental search string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cd44-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5cd44-113">Return value</span></span>

<span data-ttu-id="5cd44-114">Restituisce il numero di caratteri nella stringa di ricerca incrementale.</span><span class="sxs-lookup"><span data-stu-id="5cd44-114">Returns the number of characters in the incremental search string.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cd44-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5cd44-115">Remarks</span></span>

<span data-ttu-id="5cd44-116">**Avviso di sicurezza:** L'utilizzo errato di questo messaggio potrebbe compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="5cd44-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="5cd44-117">È necessario allocare un buffer sufficientemente grande per conservare la stringa.</span><span class="sxs-lookup"><span data-stu-id="5cd44-117">You must allocate a large enough buffer to hold the string.</span></span> <span data-ttu-id="5cd44-118">Chiamare prima il messaggio passando **null** in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="5cd44-118">First call the message passing **NULL** in *lParam*.</span></span> <span data-ttu-id="5cd44-119">Viene restituito il numero di caratteri, esclusi i **valori null**, che sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="5cd44-119">This returns the number of characters, excluding **NULL**, that are required.</span></span> <span data-ttu-id="5cd44-120">Chiamare quindi il messaggio una seconda volta per recuperare la stringa.</span><span class="sxs-lookup"><span data-stu-id="5cd44-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="5cd44-121">Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="5cd44-121">You should review [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="5cd44-122">Se il controllo di visualizzazione albero non è in modalità di ricerca incrementale, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="5cd44-122">If the tree-view control is not in incremental search mode, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cd44-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cd44-123">Requirements</span></span>



| <span data-ttu-id="5cd44-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cd44-124">Requirement</span></span> | <span data-ttu-id="5cd44-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5cd44-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5cd44-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cd44-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5cd44-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5cd44-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5cd44-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cd44-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5cd44-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5cd44-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5cd44-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cd44-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cd44-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cd44-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5cd44-132">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5cd44-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5cd44-133">**TVM \_ GETISEARCHSTRINGW** (Unicode) e **TVM \_ GETISEARCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5cd44-133">**TVM\_GETISEARCHSTRINGW** (Unicode) and **TVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





