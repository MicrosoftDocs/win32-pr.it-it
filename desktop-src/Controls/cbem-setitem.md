---
title: Messaggio CBEM_SETITEM (COMmctrl. h)
description: Imposta gli attributi per un elemento in un controllo ComboBoxEx.
ms.assetid: 752df8ea-fd5e-47fa-b729-d019bdde0904
keywords:
- Controlli di Windows Message CBEM_SETITEM
topic_type:
- apiref
api_name:
- CBEM_SETITEM
- CBEM_SETITEMA
- CBEM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ae19287e3e30810b1d8c558be9b6153a86ab6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743399"
---
# <a name="cbem_setitem-message"></a><span data-ttu-id="f1bd9-104">CBEM- \_ messaggio di elemento</span><span class="sxs-lookup"><span data-stu-id="f1bd9-104">CBEM\_SETITEM message</span></span>

<span data-ttu-id="f1bd9-105">Imposta gli attributi per un elemento in un controllo ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="f1bd9-105">Sets the attributes for an item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f1bd9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1bd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1bd9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1bd9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f1bd9-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f1bd9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f1bd9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1bd9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1bd9-110">Puntatore a una struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) contenente le informazioni sull'elemento da impostare.</span><span class="sxs-lookup"><span data-stu-id="f1bd9-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains the item information to be set.</span></span> <span data-ttu-id="f1bd9-111">Quando il messaggio viene inviato, il membro **mask** della struttura deve essere impostato in modo da indicare quali attributi sono validi e il membro **iItem** deve specificare l'indice in base zero dell'elemento da modificare.</span><span class="sxs-lookup"><span data-stu-id="f1bd9-111">When the message is sent, the **mask** member of the structure must be set to indicate which attributes are valid and the **iItem** member must specify the zero-based index of the item to be modified.</span></span> <span data-ttu-id="f1bd9-112">Impostando il membro **iItem** su-1, l'elemento visualizzato nel controllo di modifica verrà modificato.</span><span class="sxs-lookup"><span data-stu-id="f1bd9-112">Setting the **iItem** member to -1 will modify the item displayed in the edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1bd9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1bd9-113">Return value</span></span>

<span data-ttu-id="f1bd9-114">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f1bd9-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1bd9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1bd9-115">Requirements</span></span>



| <span data-ttu-id="f1bd9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1bd9-116">Requirement</span></span> | <span data-ttu-id="f1bd9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f1bd9-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1bd9-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1bd9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f1bd9-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1bd9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1bd9-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1bd9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f1bd9-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f1bd9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1bd9-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1bd9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1bd9-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1bd9-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f1bd9-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f1bd9-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f1bd9-125">**CBEM \_ SETITEMW** (Unicode) e **CBEM \_ setitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f1bd9-125">**CBEM\_SETITEMW** (Unicode) and **CBEM\_SETITEMA** (ANSI)</span></span><br/>                 |



 

 





