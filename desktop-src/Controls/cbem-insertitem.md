---
title: Messaggio CBEM_INSERTITEM (COMmctrl. h)
description: Inserisce un nuovo elemento in un controllo ComboBoxEx.
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- Controlli di Windows Message CBEM_INSERTITEM
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302646"
---
# <a name="cbem_insertitem-message"></a><span data-ttu-id="aa0ab-104">\_Messaggio CBEM INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="aa0ab-104">CBEM\_INSERTITEM message</span></span>

<span data-ttu-id="aa0ab-105">Inserisce un nuovo elemento in un controllo ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-105">Inserts a new item in a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa0ab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa0ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa0ab-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa0ab-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="aa0ab-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="aa0ab-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa0ab-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa0ab-110">Puntatore a una struttura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) che contiene informazioni sull'elemento da inserire.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-110">A pointer to a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure that contains information about the item to be inserted.</span></span> <span data-ttu-id="aa0ab-111">Quando il messaggio viene inviato, è necessario impostare il membro **iItem** per indicare l'indice in base zero in corrispondenza del quale inserire l'elemento.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-111">When the message is sent, the **iItem** member must be set to indicate the zero-based index at which to insert the item.</span></span> <span data-ttu-id="aa0ab-112">Per inserire un elemento alla fine dell'elenco, impostare il membro **iItem** su-1.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-112">To insert an item at the end of the list, set the **iItem** member to -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa0ab-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa0ab-113">Return value</span></span>

<span data-ttu-id="aa0ab-114">Restituisce l'indice in corrispondenza del quale è stato inserito il nuovo elemento in caso di esito positivo; in caso contrario,-1.</span><span class="sxs-lookup"><span data-stu-id="aa0ab-114">Returns the index at which the new item was inserted if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa0ab-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa0ab-115">Requirements</span></span>



| <span data-ttu-id="aa0ab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa0ab-116">Requirement</span></span> | <span data-ttu-id="aa0ab-117">Valore</span><span class="sxs-lookup"><span data-stu-id="aa0ab-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0ab-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa0ab-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aa0ab-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa0ab-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa0ab-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa0ab-120">Minimum supported server</span></span><br/> | <span data-ttu-id="aa0ab-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa0ab-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa0ab-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa0ab-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa0ab-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa0ab-123"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="aa0ab-124">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="aa0ab-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="aa0ab-125">**CBEM \_ INSERTITEMW** (Unicode) e **CBEM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="aa0ab-125">**CBEM\_INSERTITEMW** (Unicode) and **CBEM\_INSERTITEMA** (ANSI)</span></span><br/>           |



 

 





