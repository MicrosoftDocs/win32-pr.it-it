---
title: Messaggio LVM_HITTEST (COMmctrl. h)
description: Determina quale elemento della visualizzazione elenco, se presente, si trova in una posizione specificata. È possibile inviare questo messaggio in modo esplicito o tramite la \_ macro di ListView HitTest.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- Controlli di Windows Message LVM_HITTEST
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb770c8f5a47f1dcbbf23a11443afa581aea2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964735"
---
# <a name="lvm_hittest-message"></a><span data-ttu-id="9c14e-105">\_Messaggio HITTEST di LVM</span><span class="sxs-lookup"><span data-stu-id="9c14e-105">LVM\_HITTEST message</span></span>

<span data-ttu-id="9c14e-106">Determina quale elemento della visualizzazione elenco, se presente, si trova in una posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="9c14e-106">Determines which list-view item, if any, is at a specified position.</span></span> <span data-ttu-id="9c14e-107">È possibile inviare questo messaggio in modo esplicito o tramite la macro di [**ListView \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) .</span><span class="sxs-lookup"><span data-stu-id="9c14e-107">You can send this message explicitly or by using the [**ListView\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c14e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c14e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c14e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c14e-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9c14e-110">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="9c14e-110">Must be 0.</span></span> <span data-ttu-id="9c14e-111">**Windows Vista.**</span><span class="sxs-lookup"><span data-stu-id="9c14e-111">**Windows Vista.**</span></span> <span data-ttu-id="9c14e-112">Deve essere-1 se è necessario recuperare i membri **iGROUP** e **ISubItem** della struttura *lParam* .</span><span class="sxs-lookup"><span data-stu-id="9c14e-112">Should be -1 if the **iGroup** and **iSubItem** members of the *lParam* structure are to be retrieved.</span></span></dd> <dt>

<span data-ttu-id="9c14e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c14e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c14e-114">Puntatore a una struttura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) che contiene la posizione di hit test e riceve informazioni sui risultati dell'hit test.</span><span class="sxs-lookup"><span data-stu-id="9c14e-114">Pointer to an [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure that contains the position to hit test and receives information about the results of the hit test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c14e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c14e-115">Return value</span></span>

<span data-ttu-id="9c14e-116">Restituisce l'indice dell'elemento in corrispondenza della posizione specificata, se presente, oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9c14e-116">Returns the index of the item at the specified position, if any, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c14e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c14e-117">Requirements</span></span>



| <span data-ttu-id="9c14e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c14e-118">Requirement</span></span> | <span data-ttu-id="9c14e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9c14e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c14e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c14e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9c14e-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c14e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c14e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c14e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9c14e-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c14e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c14e-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c14e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c14e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c14e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





