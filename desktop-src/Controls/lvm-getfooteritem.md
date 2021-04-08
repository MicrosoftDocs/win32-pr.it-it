---
title: Messaggio LVM_GETFOOTERITEM (COMmctrl. h)
description: Ottiene informazioni su un elemento del piè di pagina in un controllo visualizzazione elenco. Inviare questo messaggio in modo esplicito o utilizzando la \_ macro GetFooterItem di ListView.
ms.assetid: 92f55719-c265-433f-84fc-a673680c7ad9
keywords:
- Controlli di Windows Message LVM_GETFOOTERITEM
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e642c9d853ae11edcd9199e48de61592de4883c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047856"
---
# <a name="lvm_getfooteritem-message"></a><span data-ttu-id="6b9a3-105">\_Messaggio GETFOOTERITEM LVM</span><span class="sxs-lookup"><span data-stu-id="6b9a3-105">LVM\_GETFOOTERITEM message</span></span>

<span data-ttu-id="6b9a3-106">Ottiene informazioni su un elemento del piè di pagina in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="6b9a3-106">Gets information on a footer item in a list-view control.</span></span> <span data-ttu-id="6b9a3-107">Inviare questo messaggio in modo esplicito o utilizzando la macro [**\_ GetFooterItem di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) .</span><span class="sxs-lookup"><span data-stu-id="6b9a3-107">Send this message explicitly or by using the [**ListView\_GetFooterItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b9a3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b9a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b9a3-109">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b9a3-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b9a3-110">Indice dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="6b9a3-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="6b9a3-111">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6b9a3-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b9a3-112">Puntatore a una struttura [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) per ricevere un valore per i membri **state** e/o **pszText** in base al valore del membro **mask** .</span><span class="sxs-lookup"><span data-stu-id="6b9a3-112">A pointer to a [**LVFOOTERITEM**](/windows/win32/api/commctrl/ns-commctrl-lvfooteritem) structure to receive a value for the **state** and/or **pszText** members according to the value of the **mask** member.</span></span> <span data-ttu-id="6b9a3-113">Il processo chiamante è responsabile dell'allocazione di questa struttura e dell'impostazione dei relativi membri per indicare al destinatario le informazioni da restituire.</span><span class="sxs-lookup"><span data-stu-id="6b9a3-113">The calling process is responsible for allocating this structure and setting its members to indicate to the receiver what information to return.</span></span> <span data-ttu-id="6b9a3-114">Per ulteriori informazioni, vedere **LVFOOTERITEM**.</span><span class="sxs-lookup"><span data-stu-id="6b9a3-114">For more information, see **LVFOOTERITEM**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b9a3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b9a3-115">Return value</span></span>

<span data-ttu-id="6b9a3-116">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6b9a3-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b9a3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b9a3-117">Requirements</span></span>



| <span data-ttu-id="6b9a3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b9a3-118">Requirement</span></span> | <span data-ttu-id="6b9a3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6b9a3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b9a3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b9a3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6b9a3-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6b9a3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b9a3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b9a3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6b9a3-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6b9a3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b9a3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b9a3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b9a3-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b9a3-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





